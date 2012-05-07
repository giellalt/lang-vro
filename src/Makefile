# This is a makefile that builds the Nenets morphological parser
# *****************************************************************


# This is a preliminary file that builds a Skolt Sami parser based upon
# xfst and not twolc.



XFST = xfst 
LEXC = lexc 
TWOLC = twolc

ifeq (victorio.uit.no, $(shell hostname))
XFST = /opt/sami/xerox/c-fsm/ix86-linux2.6-gcc3.4/bin/fst -utf8
LEXC = /opt/sami/xerox/bin/lexc -utf8
TWOLC = /opt/sami/xerox/bin/twolc -utf8
endif


SRC = vro-lex.txt \
	noun-vro-morph.txt \
	noun-vro-lex.txt \
	adj-vro-lex.txt \
	adv-vro-lex.txt \
	verb-vro-lex.txt \
	verb-vro-morph.txt \
	num-vro-lex.txt \
	num-vro-morph.txt \
	pron-vro-morph.txt \
#	punct-vro-lex.txt \
	pp-vro-lex.txt

# Here we build the final generator , an inverted transducer of the analyzer.
# It is dependent upon vro.save

ivro.fst: ../bin/ivro.fst
../bin/ivro.fst: ../bin/vro.fst ../bin/vro-num.fst
	@echo
	@echo "*** Building the inverse ivro.fst ***"
	@echo
	@printf "load ../bin/vro.save \n\
	invert net \n\
	save stack ../bin/ivro.fst \n\
	quit \n" > ../../tmp/ivro-fst-script
	$(XFST) < ../../tmp/ivro-fst-script
	@rm -f ../../tmp/ivro-fst-script


# This goal is to build the final analyser. It depends on all the files.

vro.fst: ../bin/vro.fst
../bin/vro.fst: ../bin/vro.save ../bin/caseconv.fst
	@echo
	@echo "*** Building vro.fst ***" ;
	@echo
	@printf "read regex [[@\"../bin/vro.save\"] .o. \
	[@\"../bin/caseconv.fst\"]] ; \n\
	save stack ../bin/vro.fst \n\
	quit \n" > ../../tmp/vro-fst-script
	$(XFST) < ../../tmp/vro-fst-script
	@rm -f ../../tmp/vro-fst-script


# The second goal is to build the caseconv.fst file
# This goal depends on case.regex

caseconv.fst: ../bin/caseconv.fst
../bin/caseconv.fst: case.regex
	@echo
	@echo "*** Building caseconv.fst ***" ;
	@echo
	@printf "read regex < case.regex \n\
	save stack ../bin/caseconv.fst \n\
	quit \n" > ../../tmp/caseconv-script
	$(XFST) < ../../tmp/caseconv-script
	@rm -f ../../tmp/caseconv-script





vro.save: ../bin/vro.save
../bin/vro.save: ../bin/xfst-vro.bin ../bin/vro-lex.save
	@echo
	@echo "*** Building the parser vro.save ***"
	@echo
	@printf "read regex [[@\"../bin/vro-lex.save\"] .o. \
	[@\"../bin/xfst-vro.bin\"]] ; \n\
	save stack ../bin/vro.save \n\
	quit \n" > ../../tmp/vro-save-script
	$(XFST) < ../../tmp/vro-save-script
	@rm -f ../../tmp/vro-save-script

# The first goal is to build vro-lex.save
# This goal depends on a bunch of lexicon files

vro-lex.save: ../bin/vro-lex.save
../bin/vro-lex.save: $(SRC)
	@echo
	@echo "*** Building vro-lex.save ***" ;
	@echo
	printf "compile-source $(SRC) \n\
	save-source ../bin/vro-lex.save \n\
	quit \n" > ../../tmp/vro-lex-save-script
	$(LEXC) < ../../tmp/vro-lex-save-script
	rm -f ../../tmp/vro-lex-save-script

# The second goal is to build xfst-vro.bin
# This goal depends on xfst-vro.txt

xfst-vro.bin: ../bin/xfst-vro.bin
../bin/xfst-vro.bin: xfst-vro.txt
	@echo
	@echo "*** Building xfst-vro.bin ***" ;
	@echo
	@printf "source xfst-vro.txt \n\
	save stack ../bin/xfst-vro.bin \n\
	quit \n" > ../../tmp/xfst-vro-script
	$(XFST) < ../../tmp/xfst-vro-script
	@rm -f ../../tmp/xfst-vro-script


# And yes, the number generator.

vro-num.fst: ../bin/vro-num.fst
../bin/vro-num.fst: vro-num.txt
	@echo
	@echo "*** Building $(notdir $@) ***" ;
	@echo
	$(XFST) -e "read lexc < $< " \
		-e "save stack   $@ " \
		-stop



clean:
	@rm -f ../bin/*.bin ../bin/*.fst ../bin/*.save


