## Process this file with automake to produce Makefile.in
## Copyright: Sámediggi/Divvun/UiT
## Licence: GPL v3+

# The current dir must be built first.
SUBDIRS = . fstbased listbased

#########################################
# BEGIN: Local processing
#
# Target template:
#
# analyser-speller-gt-norm.%: analyser-speller-gt-norm.tmp.%
#	build rules

generator-speller-gt-norm.hfst: analyser-speller-gt-norm.tmp.hfst \
		$(top_builddir)/src/filters/remove-combining-circumflex-accent-below.hfst \
		$(top_builddir)/src/filters/remove-combining-caron-below.hfst             \
		$(top_builddir)/src/filters/remove-modifier-letter-grave-accent.hfst
	$(AM_V_HXFST)$(PRINTF) "read regex                                                     \
			@\"$<\"                                                                        \
		.o. @\"$(top_builddir)/src/filters/remove-combining-caron-below.hfst\"             \
		.o. @\"$(top_builddir)/src/filters/remove-modifier-letter-grave-accent.hfst\"      \
		.o. @\"$(top_builddir)/src/filters/remove-combining-circumflex-accent-below.hfst\" \
		;\n\
		save stack $@\n\
		quit\n" | $(HFST_XFST) -p $(VERBOSITY)

analyser-speller-gt-norm.hfst: analyser-speller-gt-norm.tmp.hfst \
		$(top_builddir)/src/filters/remove-combining-circumflex-accent-below.hfst \
		$(top_builddir)/src/filters/remove-combining-caron-below.hfst             \
		$(top_builddir)/src/filters/remove-modifier-letter-grave-accent.hfst
	$(AM_V_HXFST)$(PRINTF) "read regex                                                     \
			@\"$<\"                                                                        \
		.o. @\"$(top_builddir)/src/filters/remove-combining-caron-below.hfst\"             \
		.o. @\"$(top_builddir)/src/filters/remove-modifier-letter-grave-accent.hfst\"      \
		.o. @\"$(top_builddir)/src/filters/remove-combining-circumflex-accent-below.hfst\" \
		;\n\
		invert\n\
		save stack $@\n\
		quit\n" | $(HFST_XFST) -p $(VERBOSITY)

generator-speller-gt-norm.xfst: analyser-speller-gt-norm.tmp.xfst \
		$(top_builddir)/src/filters/remove-combining-circumflex-accent-below.xfst \
		$(top_builddir)/src/filters/remove-combining-caron-below.xfst             \
		$(top_builddir)/src/filters/remove-modifier-letter-grave-accent.xfst
	$(AM_V_XFST)$(PRINTF) "read regex                                                      \
			@\"$<\"                                                                        \
		.o. @\"$(top_builddir)/src/filters/remove-combining-caron-below.xfst\"             \
		.o. @\"$(top_builddir)/src/filters/remove-modifier-letter-grave-accent.xfst\"      \
		.o. @\"$(top_builddir)/src/filters/remove-combining-circumflex-accent-below.xfst\" \
		    ;\n\
		invert \n\
		save stack $@\n\
		quit\n" | $(XFST) $(VERBOSITY)

analyser-speller-gt-norm.xfst: analyser-speller-gt-norm.tmp.xfst \
				$(top_builddir)/src/filters/remove-combining-circumflex-accent-below.xfst \
				$(top_builddir)/src/filters/remove-combining-caron-below.xfst             \
				$(top_builddir)/src/filters/remove-modifier-letter-grave-accent.xfst
	$(AM_V_XFST)$(PRINTF) "read regex                                                      \
			@\"$<\"                                                                        \
		.o. @\"$(top_builddir)/src/filters/remove-combining-caron-below.xfst\"             \
		.o. @\"$(top_builddir)/src/filters/remove-modifier-letter-grave-accent.xfst\"      \
		.o. @\"$(top_builddir)/src/filters/remove-combining-circumflex-accent-below.xfst\" \
		;\n\
		save stack $@\n\
		quit\n" | $(XFST) $(VERBOSITY)

generator-speller-gt-norm.foma: analyser-speller-gt-norm.tmp.foma \
				$(top_builddir)/src/filters/remove-combining-circumflex-accent-below.foma \
				$(top_builddir)/src/filters/remove-combining-caron-below.foma             \
				$(top_builddir)/src/filters/remove-modifier-letter-grave-accent.foma
	$(AM_V_FOMA)$(PRINTF) "read regex                                                      \
			@\"$<\"                                                                        \
		.o. @\"$(top_builddir)/src/filters/remove-combining-caron-below.foma\"             \
		.o. @\"$(top_builddir)/src/filters/remove-modifier-letter-grave-accent.foma\"      \
		.o. @\"$(top_builddir)/src/filters/remove-combining-circumflex-accent-below.foma\" \
		;\n\
		invert \n\
		save stack $@\n\
		quit\n" | $(FOMA) $(VERBOSITY)

analyser-speller-gt-norm.foma: analyser-speller-gt-norm.tmp.foma \
				$(top_builddir)/src/filters/remove-combining-circumflex-accent-below.foma \
				$(top_builddir)/src/filters/remove-combining-caron-below.foma             \
				$(top_builddir)/src/filters/remove-modifier-letter-grave-accent.foma
	$(AM_V_FOMA)$(PRINTF) "read regex                                                      \
			@\"$<\"                                                                        \
		.o. @\"$(top_builddir)/src/filters/remove-combining-caron-below.foma\"             \
		.o. @\"$(top_builddir)/src/filters/remove-modifier-letter-grave-accent.foma\"      \
		.o. @\"$(top_builddir)/src/filters/remove-combining-circumflex-accent-below.foma\" \
		;\n\
		save stack $@\n\
		quit\n" | $(FOMA) $(VERBOSITY)

# END: Local processing
#########################################

include $(top_srcdir)/am-shared/tools-spellcheckers-dir-include.am
