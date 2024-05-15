## Process this file with automake to produce Makefile.in
## Copyright: Sámediggi/Divvun/UiT
## Licence: GPL v3+

# always build . last here, and tagsets have to be built after morphology
SUBDIRS = morphology filters phonetics syllabification orthography transcriptions tagsets . test

####### Automake targets: ########

# Define target variables first, before assigning to them:
GT_ANALYSERS=
GT_GENERATORS=
CUSTOM_FSTS=

#### Local modifications in *fst processing: ####
####
#### Copy the fallback targets, and rename them to the desired targets. Then:
#### Replace the 'cp' command (Xerox) / Prepend the hfst-invert command (Hfst -
#### remember to move the $<) with whatever you need to complete
#### the processing to get the final target transducer.
#### Remember to add the dependencies as well.
#### Also make sure that HFST and Xerox processing are the same.
####
#### If you add new transducers to be built, you need to add them to the
#### relevant variable, e.g.:
####
#### if CAN_HFST
#### GT_GENERATORS+=generator-oahpa-gt-norm.hfst
#### endif
####
#### NB!!!! The HFST targets should get a hyphen after 'analyser'/'generator'
#### respectively, to make the local targets minimally different from and
#### slightly more specific than the fallback targets. This is to avoid warnings
#### about duplicate targets. That is, the local targets should looke like:
####
#### analyser-%.hfst: analyser-%.tmp.hfst
#### generator-%.hfst: generator-%.tmp.hfst

##################################################################
#### BEGIN: Add local processing instructions BELOW this line ####
##################################################################

#### Xerox transducers:
if CAN_XFST
GT_ANALYSERS+=
GT_GENERATORS+=

if WANT_CUSTOM_FSTS
CUSTOM_FSTS+=
endif # WANT_CUSTOM_FSTS

endif # CAN_XFST

#### HFST transducers
if CAN_HFST
GT_ANALYSERS+=
GT_GENERATORS+=generator-dict-gt-norm.hfst

if WANT_CUSTOM_FSTS
CUSTOM_FSTS+=
endif # WANT_CUSTOM_FSTS

endif # CAN_HFST

#### FOMA transducers
if CAN_FOMA
GT_ANALYSERS+=
GT_GENERATORS+=

if WANT_CUSTOM_FSTS
CUSTOM_FSTS+=
endif # WANT_CUSTOM_FSTS

endif # CAN_FOMA

#################################################
#### Add language-specific build rules here: ####


### Split multichar letters early, to avoid repetitive code. Multichar ###
### letters must be split on both sides, and then the alphabet pruned, ###
### for hfst-tokenise to work without issues.                          ###

# Hfst - add weights to compounds if using tropical-semiring fst format:
if WITH_OFST_TROPICAL
.generated/generator-raw-gt-desc.hfst: .generated/generator-raw-gt-desc.tmp.hfst \
					orthography/split-composed-chars.compose.hfst
	$(AM_V_XFST_TOOL)$(PRINTF) "read regex            \
				@\"orthography/split-composed-chars.compose.hfst\".i \
			.o. @\"$<\"                               \
			.o. @\"orthography/split-composed-chars.compose.hfst\" \
			;\n\
		 save stack $@.tmp\n\
		 quit\n" | $(XFST_TOOL)
	$(AM_V_REWEIGHT)$(HFST_PRUNE_ALPHABET) -i $@.tmp \
		$(HFST_REWEIGHT) $(MORE_VERBOSITY) $(HFST_FLAGS) \
			-S '+Cmp' -a 10 --arcs-only \
		> $@
	 $(AM_V_at)rm -f $@.tmp

else

.generated/generator-raw-gt-desc.hfst: .generated/generator-raw-gt-desc.tmp.hfst \
					orthography/split-composed-chars.compose.hfst
	$(AM_V_XFST_TOOL)$(PRINTF) "read regex            \
				@\"orthography/split-composed-chars.compose.hfst\".i \
			.o. @\"$<\"                               \
			.o. @\"orthography/split-composed-chars.compose.hfst\" \
			;\n\
		 save stack $@.tmp\n\
		 quit\n" | $(XFST_TOOL)
	 $(AM_V_HPRUNE)$(HFST_PRUNE_ALPHABET) -i $@.tmp -o $@
	 $(AM_V_at)rm -f $@.tmp

endif

.generated/analyser-raw-gt-desc.%: .generated/analyser-raw-gt-desc.tmp.% \
					orthography/split-composed-chars.compose.%
	$(AM_V_XFST_TOOL)$(PRINTF) "read regex            \
				@\"orthography/split-composed-chars.compose.$*\".i \
			.o. @\"$<\"                               \
			.o. @\"orthography/split-composed-chars.compose.$*\" \
			;\n\
		 save stack $@\n\
		 quit\n" | $(XFST_TOOL)


# Hfst:
.generated/analyser-%.hfst: .generated/analyser-%.tmp.hfst                        \
					filters/remove-combining-caron-below.hfst   \
					filters/remove-modifier-letter-grave-accent.hfst   \
					filters/remove-combining-circumflex-accent-below.hfst            
	$(AM_V_RGX2FST)$(PRINTF) "                               \
				@\"$<\"                                      \
			.o. @\"filters/remove-combining-circumflex-accent-below.hfst\" \
			.o. @\"filters/remove-combining-caron-below.hfst\"   \
			.o. @\"filters/remove-modifier-letter-grave-accent.hfst\"   \
			;" \
		| $(HFST_REGEXP2FST) $(HFST_FLAGS) $(HFST_FORMAT) \
			-S --xerox-composition=ON \
		| $(HFST_INVERT) \
		> $@

# We need to specify -gt- to avoid applying the filters to the raw fst:
.generated/generator-gt-%.hfst: .generated/generator-gt-%.tmp.hfst                \
					filters/remove-combining-caron-below.hfst   \
					filters/remove-modifier-letter-grave-accent.hfst   \
					filters/remove-combining-circumflex-accent-below.hfst            
	$(AM_V_RGX2FST)$(PRINTF) "                               \
				@\"$<\"                                      \
			.o. @\"filters/remove-combining-circumflex-accent-below.hfst\" \
			.o. @\"filters/remove-combining-caron-below.hfst\"   \
			.o. @\"filters/remove-modifier-letter-grave-accent.hfst\"   \
			;" \
		| $(HFST_REGEXP2FST) $(HFST_FLAGS) $(HFST_FORMAT) \
			-S --xerox-composition=ON \
		> $@

# Xerox:
# We need to specify -gt- to avoid applying the filters to the raw fst:
.generated/analyser-gt-%.xfst: .generated/analyser-gt-%.tmp.xfst                  \
					filters/remove-combining-caron-below.xfst   \
					filters/remove-modifier-letter-grave-accent.xfst   \
					filters/remove-combining-circumflex-accent-below.xfst            
	$(AM_V_XFST)$(PRINTF) "read regex                        \
				@\"$<\"                                      \
			.o. @\"filters/remove-combining-circumflex-accent-below.xfst\" \
			.o. @\"filters/remove-combining-caron-below.xfst\"   \
			.o. @\"filters/remove-modifier-letter-grave-accent.xfst\"   \
			;\n\
		 save stack $@\n\
		 quit\n" | $(XFST) $(VERBOSITY)

.generated/generator-%.xfst: .generated/generator-%.tmp.xfst                      \
					filters/remove-combining-caron-below.xfst   \
					filters/remove-modifier-letter-grave-accent.xfst   \
					filters/remove-combining-circumflex-accent-below.xfst            
	$(AM_V_XFST)$(PRINTF) "read regex                        \
				@\"$<\"                                      \
			.o. @\"filters/remove-combining-circumflex-accent-below.xfst\" \
			.o. @\"filters/remove-combining-caron-below.xfst\"   \
			.o. @\"filters/remove-modifier-letter-grave-accent.xfst\"   \
			;\n\
		 invert net\n\
		 save stack $@\n\
		 quit\n" | $(XFST) $(VERBOSITY)

# Special case for the disamb analyser, since it follows the same filename
# pattern as the raw fst:
.generated/analyser-disamb-gt-%.xfst: .generated/analyser-disamb-gt-%.tmp.xfst    \
					filters/remove-combining-caron-below.xfst   \
					filters/remove-modifier-letter-grave-accent.xfst   \
					filters/remove-combining-circumflex-accent-below.xfst            
	$(AM_V_XFST)$(PRINTF) "read regex                        \
				@\"$<\"                                      \
			.o. @\"filters/remove-combining-circumflex-accent-below.xfst\" \
			.o. @\"filters/remove-combining-caron-below.xfst\"   \
			.o. @\"filters/remove-modifier-letter-grave-accent.xfst\"   \
			;\n\
		 save stack $@\n\
		 quit\n" | $(XFST) $(VERBOSITY)

# Foma, for completeness:
# We need to specify -gt- to avoid applying the filters to the raw fst:
.generated/analyser-gt-%.foma: .generated/analyser-gt-%.tmp.foma                  \
					filters/remove-combining-caron-below.foma   \
					filters/remove-modifier-letter-grave-accent.foma   \
					filters/remove-combining-circumflex-accent-below.foma            
	$(AM_V_XFST)$(PRINTF) "read regex                        \
				@\"$<\"                                      \
			.o. @\"filters/remove-combining-circumflex-accent-below.foma\" \
			.o. @\"filters/remove-combining-caron-below.foma\"   \
			.o. @\"filters/remove-modifier-letter-grave-accent.foma\"   \
			;\n\
		 save stack $@\n\
		 quit\n" | $(XFST) $(VERBOSITY)

.generated/generator-%.foma: .generated/generator-%.tmp.foma                      \
					filters/remove-combining-caron-below.foma   \
					filters/remove-modifier-letter-grave-accent.foma   \
					filters/remove-combining-circumflex-accent-below.foma            
	$(AM_V_XFST)$(PRINTF) "read regex                        \
				@\"$<\"                                      \
			.o. @\"filters/remove-combining-circumflex-accent-below.foma\" \
			.o. @\"filters/remove-combining-caron-below.foma\"   \
			.o. @\"filters/remove-modifier-letter-grave-accent.foma\"   \
			;\n\
		 invert net\n\
		 save stack $@\n\
		 quit\n" | $(XFST) $(VERBOSITY)

# Special case for the disamb analyser, since it follows the same filename
# pattern as the raw fst:
.generated/analyser-disamb-gt-%.foma: .generated/analyser-disamb-gt-%.tmp.foma    \
					filters/remove-combining-caron-below.foma   \
					filters/remove-modifier-letter-grave-accent.foma   \
					filters/remove-combining-circumflex-accent-below.foma            
	$(AM_V_XFST)$(PRINTF) "read regex                        \
				@\"$<\"                                      \
			.o. @\"filters/remove-combining-circumflex-accent-below.foma\" \
			.o. @\"filters/remove-combining-caron-below.foma\"   \
			.o. @\"filters/remove-modifier-letter-grave-accent.foma\"   \
			;\n\
		 save stack $@\n\
		 quit\n" | $(XFST) $(VERBOSITY)

# Do NOT apply the accent removal filters to the normative
# dictionary generator (both hfst and xfst/foma):
.generated/generator-dict-gt-norm.hfst: .generated/generator-dict-gt-norm.tmp.hfst
	$(AM_V_CP)cp -f $< $@

.generated/generator-dict-gt-norm.%: .generated/generator-dict-gt-norm.tmp.%
	$(AM_V_XFST)$(PRINTF) "\
		 load stack $<\n\
		 invert net\n\
		 save stack $@\n\
		 quit\n" | $(XFST) $(VERBOSITY)


##################################################################
#### END: Add local processing instructions ABOVE this line ######
##################################################################


include $(top_srcdir)/../giella-core/am-shared/src-fst-dir-include.am
