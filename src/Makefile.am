## Process this file with automake to produce Makefile.in
## Copyright: Sámediggi/Divvun/UiT
## Licence: GPL v3+

SUBDIRS = fst cg3

#################################################
#### Add language-specific build rules here: ####


### Split multichar letters early, to avoid repetitive code. Multichar ###
### letters must be split on both sides, and then the alphabet pruned, ###
### for hfst-tokenise to work without issues.                          ###

# Hfst - add weights to compounds if using tropical-semiring fst format:
if WITH_OFST_TROPICAL
generator-raw-gt-desc.hfst: generator-raw-gt-desc.tmp.hfst \
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

generator-raw-gt-desc.hfst: generator-raw-gt-desc.tmp.hfst \
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

analyser-raw-gt-desc.%: analyser-raw-gt-desc.tmp.% \
					orthography/split-composed-chars.compose.%
	$(AM_V_XFST_TOOL)$(PRINTF) "read regex            \
				@\"orthography/split-composed-chars.compose.$*\".i \
			.o. @\"$<\"                               \
			.o. @\"orthography/split-composed-chars.compose.$*\" \
			;\n\
		 save stack $@\n\
		 quit\n" | $(XFST_TOOL)


# Hfst:
analyser-%.hfst: analyser-%.tmp.hfst                        \
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
generator-gt-%.hfst: generator-gt-%.tmp.hfst                \
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
analyser-gt-%.xfst: analyser-gt-%.tmp.xfst                  \
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

generator-%.xfst: generator-%.tmp.xfst                      \
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
analyser-disamb-gt-%.xfst: analyser-disamb-gt-%.tmp.xfst    \
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
analyser-gt-%.foma: analyser-gt-%.tmp.foma                  \
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

generator-%.foma: generator-%.tmp.foma                      \
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
analyser-disamb-gt-%.foma: analyser-disamb-gt-%.tmp.foma    \
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
generator-dict-gt-norm.hfst: generator-dict-gt-norm.tmp.hfst
	$(AM_V_CP)cp -f $< $@

generator-dict-gt-norm.%: generator-dict-gt-norm.tmp.%
	$(AM_V_XFST)$(PRINTF) "\
		 load stack $<\n\
		 invert net\n\
		 save stack $@\n\
		 quit\n" | $(XFST) $(VERBOSITY)


##################################################################
#### END: Add local processing instructions ABOVE this line ######
##################################################################

include $(top_srcdir)/../giella-core/am-shared/src-dir-include.am
