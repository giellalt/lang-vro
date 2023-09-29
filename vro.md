# Võro description 

All documents in one file


# C O M M O N  S Á M I  D E P E N D E N C Y   G R A M M A R

This dep file is for sma, sme, smj, sje.

# DELIMITERS

Sentence delimiters are the following: <.> <!> <?> <...> <¶>

# TAGS AND SETS

N
V
A
Adv
CC
CS
Inf
Sup
Neg
Num
Po
Pr

Pcle
Prop

Pron
IV
TV
COMMA
DASH
CITATION to keep colouring we add a "
HYPHEN
QMARK
PUNCT
LEFT
RIGHT
CLB
Ind
Pot
Impr
ImprtII
Cond
ConNeg
Caus causative eus
VGen
Interj
ABBR
ACR
Prs
Prt
Cmpnd
RCmpnd
PrfPrc
PrsPrc
Actor
Actio
Ger
Indef
Nom
Acc
Ill
Com
Gen
Ess

IM For fao

## POS sub-categories

## Syntactic tags and sets

### Syntactic tags in input to this file

### Syntactic tags added in this file

* @FMV : finite main verb
- oaidná: Son oaidná ollislaš gova. - She sees the whole picture
* infinite main verb
* @FAUX : finite auxiliary verb
- ferte: Son ferte oaidnit ollislaš gova. - She must see the whole picture. 
* @FMVdic : finite main verb introducing direct speech
* @IMVdic : infinite main verb introducing direct speech
* @FS-IMV : infinite main verb of subclause 
* @FS-IAUX : infinite auxiliary verb in subclause
* @FS-N<IAUX : infinite auxiliary verb of a relative subclause
* @FS-N<IMV : infinite main verb of a relative subclause
* @FS-OBJ : finite verb in subclause functioning as object
* @FS-OBJ> : finite verb in subclause functioning as object
* @FS-<OBJ : finite verb in subclause functioning as object
* @FS-SUBJ : finite verb in subclause functioning as subject
* @FS-SUBJ> : finite verb in subclause functioning as subject
* @FS-<SUBJ : finite verb in subclause functioning as subject
* @FS-ADVL> : finite verb in subclause functioning as adverbial to the left of the main clause
* @FS-<ADVL : finite verb in subclause functioning as adverbial to the right of the main clause
* @S< : a clause modifying a sentence to the right of it
* @FS-ADVL : finite verb in subclause ...
* @-FS-<ADVL : infinite subclause - eus
* @-FS-ADVL> : infinite subclause - eus
* @FS-N< : relative clause to N
* @FS->N : relative clause to N to the left side of it - eus
* @FS-VFIN< : finite verb in sentence, statement
- eai: Idja ii leat šat, eai ge sii dárbbaš lámppá dahje beaivváža čuovgga, dasgo Hearrá Ipmil lea sin čuovga. - The night is not anymore, they do not need the lamp- or day- light either, because God the Lord is their light.
* @FS-<APP : finite subclause functioning as an apposition
* @ICL-ADVL : non-finite subclause ...
* @ICL-AUX< : "right" argument of auxiliary (?)
* @ICL-OBJ : infinitival clause object
* @ICL-SUBJ : infinitival clause subject
* @ICL-P< : infinitival clause complement of preprosition
* @IAUX : non-finite auxiliary
* <mv> : main verb. A temporarily tag omitted in the end of the file.
* <aux> : auxilary verb. A temporarily tag omitted in the end of the file.

### fao syntags

* @>V

### kal syntags

* @INS :
* @<INS :
* @INS> :

### eus syntags

* @FS-SPRED : finite verb in subclause functioning as a subject predicate - eus, but not sure if in use

### Syntactic set definitions

# Dep grammar

Correction rules

* **muitalit**

* **XX**

* **XX**

* **XX**

* **faoSumId=Rel**

## The finite verb

# Mapping rules

**lgRemove** removes the language tags <sma>, <sme>,  etc, before proceeding to the dep file.

* * *
<small>This (part of) documentation was generated from [src/cg3/dependency.cg3](https://github.com/giellalt/lang-vro/blob/main/src/cg3/dependency.cg3)</small>

Disambiguator for Võro

## Sets

Sentence delimiters are the following: "<.>" "<...>" "<!>" "<?>" "<¶>"

### Part-of-Speech
* N = noun
* A = adjective
* Num = numeral
* V = verb
* Adv = adverb
* Pcle = particle
* Pr = preposition
* Po = postposition
* Pron = pronoun
* Interj = interjection

### Numerus

* Sg = Singular
* Pl = Plural
* Sg1 = Singular 1.p.
* Sg2 = Singular 2.p.
* Sg3 = Singular 3.p.
* Pl1 = Plural 1.p.
* Pl2 = Plural 2.p.
* Pl3 = Plural 3.p.

### Cases
* Nom
* Gen
* Acc
* Par
* Ine
* Ill
* Ela
* Ade
* Abe
* All
* Abl
* Ess
* Tra
* Ins
* Com
* SUBJ-CASE = Nom Par

### Types
* Prop = Proper noun
* Interr = Interrogative
* Dem = demonstrative pron
* Rel = Relative pron
Relpronpl "mikkä ja "jokka"
Relpronsg "mikä" ja "joka"
Interrpronpl "kuka" ja "mikä"
* Pers = Personal pron
* Indef = Indef pron

* Inf = Infinitive
* ConNeg = Conjugated as Negative form
* PrfPrc = Perfectum Particip
* Imprt = Imperative
* Act = Active
* Neg = Negation verb

* COMMA = comma

* Foc/kaan = focus clitic -kaan
* Foc/kaan = focus clitic -kaan

## Sets with more members

* WORD = all PoS

* NPMOD = these can modify a noun
* NPMODADV = NPMOD plus adverb

* NOT-NPMOD = these cannot modify a noun

* NOT-NPMODADV = these cannot modify a noun, and is not adverb

* QVANT-ADV = e.g. paljon, vähän
* KUNKA = e.g. kunka missä (adverbs that start a sentence)

Boundaries

* S-BOUNDARY = words that start a sentence

Verbs

* SV-BOUNDARY = words that start a sentence and finite verb

## Disambiguation rules

### Dialects

### Early rules

* __person_test__ selects finite verb if there is a Pron Pers to the left

* __adv_after_V__ selects adverb if there is a verb to the right

* __prop_infrontof_kieli__ removes propernoun in fron of kieli, if it kan be something else, e.g. Kainun kieli

* **PropInit** removes  propernoun in the beginning of a sentence if it kan be a CC or a Pr (e.g. Mutta)

* **PropNotInit** selects  propernoun if it is not in the beginning of a sentence

Possessive suffixes

Numeral phrases

### Preposition/postposition/adverb rules

* **Prifgenpar** selects  preposition to the left of Gen or Par

* **Poifgenpar** selects  postposition to the right of Gen or Par

* **vasthaan**

## Rules for mapping @CVP and @CNP on the CC and CS

* **CVP** maps @CVP to CS and mutta

* **CNPifN** maps @CNP to CC between two N

* **CNPifInf** maps @CNP to CC between two Inf

## Case rules

### Partitive

Genitive

### Illative

## Number rules

## More disambiguation rules
* **SgNotPl**

### Elative

## Propernouns

## Verbs

### Specific verbs	

ei negation verb

eli

## Adverbs

### paljon

### kerran

### jälkhiin

## Adjectives

Conjunctions

## Subjunctions

että

jos

ko	

sillä	

## Pronouns

## Verb rules, Verbs

### Infinitive

## Present Sg3

## Present Pl3 or PrsPrc

## Present Pl3 or Passive

Imperative

## Past tense

### Prt Pl3 or Prt Sg2

## Negative verb

Relative pronouns

* **Pl3ollaifplrelpronandplinterrpron** selects Pl3 if olla

* **Sg3ollaifplrelpronandplinterrpron** selects Sg3 if olla

* **Sg3ollainpretandperf** selects Sg3 if COPULAS

* **Sg3ollainpretandperf** selects Sg3 if COPULAS

* **Relpronandnotintterpron** selects Rel Sg if Interr

* **Relpronandnotintterpron** selects Rel Sg if Interr

* **interrpron** selects Interr if ? in the end

* **DifferenceBetweenNiitäImprtAndNiitäDemAndPersIfSubj** selects Pron Dem Pl or Pron Pers Pl3 when finite verb to the right

* **paljonadvandnotpaljonoun** selects Adv if paljon

* **Relpronifitsanounoracommabeforeit** selects Rel Pl if N to the left

* **annaimperativeandnotannaname** removes Prop if Anna se

* **tulinounfromtuliprtsg3** selects V Sg

* **dempronandnotpronpers** selects Den if A of N to the right

* **Imperativefromconneg** selects and removes ConNeg

* **ImperativeafterNeg** removes Imprt if pronoun

* **interrel** selects Interr of Rel if CS to the right

* **+FMAINV**  to the remaining finite verbs which are not AUX    

## HNOUN MAPPING

* **@<ADVLcoor** (@<ADVL) for ADVLCASEAdv if @CNP to the left and ADVL to the left of it

* **X** maps X everywhere

* **REMOVE X** removes X whenever there is any other tag.

* WORDLEMMA = regex giving the lemma in question

* **errorth** removes Err/Orth if there is an analysis without Err/Orth with the same lemma

* * *
<small>This (part of) documentation was generated from [src/cg3/disambiguator.cg3](https://github.com/giellalt/lang-vro/blob/main/src/cg3/disambiguator.cg3)</small>
S Y N T A C T I C   F U N C T I O N S   F O R   S Á M I

Sámi language technology project 2003-2018, University of Tromsø #

This file adds syntactic functions. It is common for all the Saami

LEFT RIGHT because of apertium

* Sets for POS sub-categories

* Sets for Semantic tags

* Sets for Morphosyntactic properties

## Syntactic tags

* @+FAUXV : finite auxiliary verb 
- ferte: Son ferte oaidnit ollislaš gova. - She must see the whole picture.
* @+FMAINV : finite main verb
- oaidná: Son oaidná ollislaš gova. - She sees the whole picture	
* @-FAUXV : infinite auxiliary verb
- sáhte: In sáhte gáhku borrat. - I cannot eat cake.	
* @-FMAINV : infinite main verb
- oaidnit: Son ferte oaidnit ollislaš gova. - She must see the whole picture.
* @-FSUBJ> : Subject of infinite verb outside the verbal.
- mu: Diet dáhpáhuvai mu dieđikeahttá. - It happened without me knowing about it.
* @-F<OBJ : Subject of infinite verb outside the verbal.
- nuppi: Ulbmil lea oažžut nuppi boagustit. - The goal is to get the other one to laugh.
* @-FOBJ> : Object of infinite verb outside the verbal.
- váldovuoittuid: Sii vurde váldovuoittuid fasket. - They waited to grab the main prizes.
* @SPRED<OBJ : Object of an subsject predicative. (some adjectives are transitive)
- guliid: Mánát leat oažžulat guliid.
* @-FADVL : Adverbial complement of infinite verb outside the verbal.
- várrogasat: Dihkkadeaddji rávve skohtervuddjiid várrogasat mátkkoštit. - The roadman warns snowscooter drivers to drive carefully.
* @-F<PRED : Predicative complement of infinite verb outside the verbal.
- ággan: Jáhkken kulturmáhtu leat oktan ággan.
* @>ADVL : Modifier of an adverbial to the right.
- vaikko: doppe leat vaikko man ollu studeanttat.
* @ADVL< : Komplement for adverbial.
- vahkus: Son málesta guktii vahkus.
* @<ADVL : Adverbial after the main verb.
- dás: Eanet dieđuid gávnnat dás.
* @ADVL> : Adverbial to the left of the main verb
- viimmat: Dál de viimmat asttan lohkat reivve.
* @ADVL>CS : Adverbial modifying subjunction.
- 'beare' pointing at 'danin go': Muhto dus ii leat riekti dearpat su beare danin go sáhtát.
* <hab> : Habitive, specifying an adverbial, e.g. @ADVL> <hab>
- Máhtes: Máhtes lea beana.
* <ext> : Extencial, specifying an subject, e.g. @<SUBJ <ext>
- beana: Máhtes lea beana.
* <logo> : logoforic pronouns, e.g. @>N <logo> (for MT)
* <cs> : 
* @>N : Modifier of a noun to the right.
- geavatlaš: Ráđđehussii lea geavatlaš politihkka deaŧalaš. - For the government, practical politics is important.
* @N< : Complement of noun to the left.
- vihtta: Mun boađán diibmu vihtta.
* @>A : Modifier of an adjective to the right.
- juohke: Seminára lágiduvvo juohke nuppi jagi.
* @P< : Complement of preposition.
- soađi: Dat dáhpáhuvai maŋŋel soađi.
* @>P : Complement of postposition.
- riegádeami: Seta riegádeami maŋŋel Áttán elii vel 800 jagi.
* @HNOUN : Stray noun in sentence fragment.
- muittut: Fidnokurssa muittut.
* @INTERJ : Interjection.
- Hei: Hei, boađe!
* @>Num : Attribute of numeral to the right.
- dušše: Mun ledjen dušše guokte mánu doppe.
* @Pron< : Complement of pronoun to the left.
- Birehiin: Moai Birehiin leimme doppe.
* @>Pron : Modifyer of pronoun to the right.
- vaikko: Olmmoš sáhttá bargat vaikko maid.
* @Num< : Complement of numeral to the left.
- girjjiin: Dat lea okta min buoremus girjjiin.
* @OBJ : Object, the verb is not in the sentence (ellipse)
* @<OBJ : Object, the verb is to the left.
- gávtti: Son goarru gávtti.
* @OBJ> : Object, the verb is to the right.
- filmma: Dán filmma leat Kárášjoga nuorat oaidnán.
* @OPRED : Object predicative, the verb is not in the sentence (ellipse).
* @<OPRED : Object predicative, the verb is to the left.
- buriid: Son ráhkada gáhkuid hui buriid.
* @OPRED> : Object predicative, the verb is to the right.
- dohkkemeahttumin: Son oinnii dohkkemeahttumin bargat ášši nu.
* @PCLE : Particle.
- Amma: Amma mii eat leat máksán? - We have not paid, have we?
* @COMP-CS< : Complement of subjunction.
- vejolaš: Dat šaddá nu buorre go vejolaš.
* @SPRED : Subject predicative, the verb is not in the sentence (ellipse).
* @<SPRED : Subject predicative, the verb is to the left.
- árgabivttas: Ovdal lei gákti árgabivttas.
* @SPRED> : Subject predicative, the verb is to the left.
- álbmogin: Sápmelaččaid historjá álbmogin lea duháhiid jagiid boaris.
* @SUBJ : Subject, the finite verb is not in the sentence (ellipse).
* @<SUBJ : Subject, the finite verb is to the left.
- gákti: Ovdal lei gákti árgabivttas.
* @SUBJ> : Subject, the finite verb is to the right.
- Son: Son lea mu oabbá. - Sheis my sister.
* @PPRED : Predicative for predicative.
* @APP : Apposition
* @APP-N< : Apposition to noun to the left.
- oahpaheaddji: Oidnen Ánne, min oahpaheaddji.
* @APP-Pron< : Apposition to pronoun to the left.
- boazodoalloáirasat: Ja moai boazodoalloáirasat áigguime vaikko guovttá joatkit barggu.
* @APP>Pron : Apposition to noun to the right.
* @APP-Num< : Apposition to numeral to the left.
* @APP-ADVL< : Apposition to adverbial to the left.
- bearjadaga: Mun vuolggán ihttin, bearjadaga.
* @VOC : Vocative
- Miss Turner : Bures boahtin deike, Miss Turner! - Welcome her, Miss Turner!
* @CVP : Conjunction or subjunction that conjoins finite verb phrases.
- go : Leago guhkes áigi dassá go Máreha oidnet? - Is it a long time since you saw Máret?
* @CNP : Local conjunction or subjunction.
- vai : Leago nieida vai bárdni? - Is it a girl or a boy?
* @CMPND
* @X : The function is unknown, e.g. because of that the word is unknown

## Tag sets

* Sets for verbs

- V is all readings with a V tag in them, REAL-V should
be the ones without an N tag following the V.
The REAL-V set thus awaits a fix to the preprocess V ... N bug.

* The set COPULAS is for predicative constructions

* NP sets defined according to their morphosyntactic features

* The PRE-NP-HEAD family of sets

These sets model noun phrases (NPs). The idea is to first define whatever can
occur in front of the head of the NP, and thereafter negate that with the
expression **WORD - premodifiers**.

The set **NOT-NPMOD** is used to find barriers between NPs.
Typical usage: ... (*1 N BARRIER NPT-NPMOD) ...
meaning: Scan to the first noun, ignoring anything that can be
part of the noun phrase of that noun (i.e., "scan to the next NP head")

* Miscellaneous sets

* Border sets and their complements

ADLVCASE

* Syntactic sets

These were the set types.

## Numeral outside the sentence

## HABITIVE MAPPING

* **hab1** hab aux leat

* __hab_numo1__ hab copula comma comma N+Nom

* __hab_numo2__ copula nu mo/go hab

* **leahab** copula nu mo/go hab

* **hab2** hab auxv adv leat

* **hab3** (<hab> @ADVL>) for asdf hab-actor and hab-case; if leat to the right, and Nom to the right of leat. Lots of restrictions.

* **hab3** (<hab> @ADVL>) for asdf hab-actor and hab-case; if leat to the right, and Nom to the right of leat. Lots of restrictions.

* **hab3** (<hab> @ADVL>) for asdf hab-actor and hab-case; if leat to the right, and Nom to the right of leat. Lots of restrictions.

* **hab3** (<hab> @ADVL>) for hab-actor and hab-case; if leat to the right, and Nom to the right of leat. Lots of restrictions.

* __hab_main__ (<hab> @ADVL>) for hab-actor and hab-case; if leat to the right, and Nom to the right of leat. Lots of restrictions.

* **habInf** hab lea inf

* **habNomLeft** Nom or Num + gen hab lea

* **habAdvl** Ii han ovttasge du sogas leat dat namma.

* **hab4** hab cc hab leat

* **hab6** lea go hab -- leago hab

* **hab7** lea go hab

* **hab8** This is not HAB Ellii šattai hoahppu.
* **hab5**  This is not HAB Mánás gollot gieđat.

* **hab9** prop ord-hab leat

* **hab10** prop ord-hab leat

* **habDain** (<hab> @ADVL>) for (Pron Dem Pl Loc) if leat followed by Nom to the right
* **habDain2** 

* **habRel** # before relative clause

* **habEllipse** Buot gánddain lea dreassa, nieiddain fas gákti.

* **habGen** (<hab> @<ADVL) hab for Gen; if Gen is located in the end of the sentence and Nom is sentence initial

* **habGenQst** (<hab> @<ADVL) hab for Gen; in a question sentence. Gen is located sentence initially and SUBJ is found to the right. To the right of SUBJ is copulas

* **n<titel1** (@N<) for ("jr") or ("sr"); if first one to the left is Prop

* **n<titel2** (@N<) for INITIAL; if first one to the left is a noun, or if to the left of you is a single letter which is part of a noun conjunction *bustávas e ja f gáibiduvvo*

* **n<:com** (@N<) for (Sg Com); if first one to the left is Coll

* **>nAttr** (@>N) for Attr; if there is a noun to your right

* **n>Indef** (Pron Indef Attr); if eará is to the right

* **n>Indef** (Pron Indef Com); if eará is to the right

* **>nNum** (@>N) for numerals if; there is a noun to your right. You are not allowed to be (Sg Nom), (Sg Acc) or (Sem/Date)

* **noun>n** (@>N) for Gen; if there is a noun to your right. Restrictions: Not if you are: a time related word. Not if you are OKTA with Pl Loc to your right. Not if CC is to your right followed by another Gen and then Po. Not if you are HUMAN and to your right is Actio Nom folloed by a noun.

* **>nTime** (@>N) for Gen TIME-N; if timenoun to your right. Restrictions: Not if you are a OKTA Nom with Pl Loc to your right. Not if CC followed by Gen, followed by Po to your right. Not if COMMA to your right

* **>ntittel** (@>N) for (Sg Nom TIME-N) or (Nom Der/NomAg); if to your right is Sem/Mal, Sem/Fem, Sem/Sur

* **>nplc** (@>N) for (Sg Nom Prop Sem/Plc), if to your right is Sem/Plc

* **>nALU** (@>N) for Sg Acc numerals; when a measure-noun to the right

* **>NTime** (@>N) for Gen; if you are TIME-N with BOC to your left, and PREGEN to your right

* **n<:Refl** (@N<) for (Refl Nom); if to the left is (N Nom), or if first one to the left is a finite mainverb with a (N Nom) to the left

* **>pron1** (@>Pron) for GRADE-ADV, DUSSE, BUOT if; first one to the right is Pron

* **>pron2** (@>Pron) for (Refl Nom) if; first one to the right is Refl

* **>pron3** (@>Pron) for (Pron Recipr) if; first one to the right is (Pron Recipr)

* **vaikko** (@>Pron) for vaikko if; first one to the right is Indef

* **vaikkoman** (@>ADVL) for vaikko if; first one to the right is man

* **dasmaŋŋel** (@>ADVL) for vaikko if; first one to the right is man

* **adv>advl** (@>ADVL) 

* **adv>advl** (@>ADVL) 

* **BOSvoc** (@VOC) for HUMAN Nom; if sentence initial. To the right is comma. No nom-cased HUMAN followed by comma or CC is allowed to the right. There should not be a relative clause to the right, because then you are likely to be SUBJ

* **voc** (@VOC) for Nom HUMAN; if comma to the left and an second person verb or pronoun to the left. To the right is the end of the sentence

* **Particle<subj** (@PCLE)

* **spred<obj** (@SPRED<OBJ) for Acc; the object of an SPRPED. Not to be mistaken with OPRED. If SPRED is to the left, and copulas is to the left of it. Nom or Hab are found sentence initially.

* **Hab<subj** (<ext> @<SUBJ) for Nom; if copulas, goallut or jápmit is FMAINV and habitive or human Loc is found to the left. OR: if Ill or @Pron< followed by HAB are found to the left.

* **Hab<subj** (<ext> @<SUBJ) with relative clause in between

* **Hab>Advlcase<subj** (<ext> @<SUBJ) for Nom; it allows adverbials with Ill/Loc/Com/Ess to be found inbetween HAB and <ext>.

* **Nom>Advlcase<subj** (<ext> @<SUBJ) for Nom; it allows adverbials with Ill/Loc/Com/Ess to be found inbetween Nom and <ext> @<SUBJ.

* **<extSubj** (<ext> @<SUBJ) for Nom; if copulas to the left, and some kind of adverb, N Loc, time related word or Po to the left of it. OR: if Ill or @Pron< to the left, followed by copulas and the before mentioned to the left of copulas.

* **<extSubj** (<ext> @<SUBJ) for sma Nom; if some kind of adverb to the left, N Loc, time related word or Po to the left of it. 

* **<extSubjA** (<ext> @<SUBJ) for A - TEST WITHOUT THIS ONE

* **<extSubj** (<ext> @<SUBJ) for Nom; if leat to the left and sentenceboundary

* **<extSubj** (<ext> @<SUBJ) for Nom, but not for Pers. To the left boahtit or heaŋgát as MAINV, and futher to the left is some kind of place related word, or time related word

* **loc<extSubj** (<ext> @<SUBJ) for Nom

* **<spred** (@<SPRED) for Nom; if Nom to the left, copulas to the left of Nom, and a time related word to the left of it.

* **<extQst1** (<ext> @<SUBJ) for Nom; in an existential sentence. To your left is hab, some kind of place or time-word or Po. This is a Qst-sentence so the qst-pcle is attached to leat or following leat

* **<extQst2** (<ext> @<SUBJ) for Nom; in an existential sentence. To your left is leat and it is sentence initial. No attributes or other words are allowed inbetween (because then you are SPRED), except the attribute muhtun, muhtin

* **extQst3>** (<ext> @SUBJ>) for Nom; if habitive first one to the left, followed by copulas.

* **extQst3>** (<ext> @SUBJ>) for Nom; if habitive first one to the left, followed by copulas.

* **<extsubjcoor** (<ext> @<SUBJ) for Nom. Coordination

* Sem/Year

* **<spredQst** (@<SPRED) for Nom; in a typically question sentence; You are not allowed to be Pers or human. The special part is that Nom is not allowed to your right

* **<spredQst2** (@<SPRED) for (A Nom); in a typically question sentence; You are SPRED if (N Nom) is to your left and leat + qst is to the left

* **<spredQst3** (@<SPRED) for (A Nom); you are SPRED when you are (A Nom) and to your right is (N Nom). This is a Qst-sentence, so copulas is found to your left

* **<spredQst4** (@<SPRED) for Nom; but only in a qst-sentence where there is no chance of you beeing the subj

* **<NomBeforeSpred** (@<SPRED) for (A Nom) if; Nom to the left, and copulas is to the left of Nom. There is no Nom allowed to the right of copulas! To avoid messing with coordination: ja, dahje and comma are not allowed to your left. Comma is not allowed to your right; if so then you are likely to be coordinated

* **<spred** (@<SPRED) for A Nom or N Nom if; the subject Nom is on the same side of copulas as you: on the right side of copulas

* **<spredVeara** (@<SPRED) for veara + Nom; if genitive immediately to the right, and intransitive mainverb to the right of genitive

* **leftCop<spred** (@<SPRED) for Nom; if copulas is the main verb to the left, and there is no Ess found to the left of cop (note that Loc is allowed between target and cop). OR: if you are Coll or Sem/Group with copulas to your left.

* **<spredLocEXPERIMENT** (@<SPRED) for material Loc; if you are to the right of copulas, and the Nom to the left of copulas is not a hab-actor

* **NumTime** (@<SPRED) for A Nom

* **<spredSg** (@<SPRED) for Sg Nom

* **<spredPg** (@<SPRED) for Pl Nom

* **<spred** (@<SPRED) for Nom; if copulas to the left, and Nom or sentence boundary to the left of copulas. First one to the right is EOS.

* **COP<spredEss** (@<SPRED) for N Ess

* **spredEss>** (@SPRED>) for N Ess; if copulas to the right of you, and if an NP with nom-case first one to your left.

* **GalleSpred>** (@SPRED>) for Num Nom; if sentence initial

* **spredSgMII>** (@SPRED>)

* **spredšaddat>** (@SPRED>)

* **r492>** (@SPRED>) for Interr Gen; consisting only of negations. You are not allowed to be MII. You are not allowed to have an adjective or noun to yor right. You are not allowed to have a verb to your right; the exception beeing an aux.

* **AdjSpredSg>** (@SPRED>) for A Sg Nom; if copulas to the right, but not if A or @<SPRED are found to the right of copulas

* **Spred>SubjInf** (@SPRED>) for Nom; if copulas to the right, and the subject of copulas is an Inf to the right

* **spredCoord** (@<SPRED) coordination for Nom; only if there already is a SPRED to the left of CNP. Not if there is some kind of comparison involved.

* **subj>Sgnr1** (@SUBJ>) for Nom Sg, including Indef Nom if; VFIN + Sg3 or Pl3 to the right (VFIN not allowed to the left)

* **subj>Du** (@SUBJ>) for dual nominatives, including Coll Nom. VFIN + Du3 to the right.
* **subj>Pl** (@SUBJ>) for plural nominatives, including Coll and Sem/Group. VFIN + Pl3 to the right.

* **subj>Pl** (@SUBJ>) for plural nominatives

* **subj>Sg** (@SUBJ>) for Nom Sg; if VFIN + Sg3 to the right.

* **Sg<subj** (@<SUBJ) for Nom Sg; if VFIN Sg3 or Du2 to the left (no HAB allowed to the left).

* **Du<subj** (@<SUBJ) for Nom Coll if; a dual third person verb is found to the left

* **PlDu<subj** (@<SUBJ) for (N Nom Pl), (Sem/Group Nom), (Coll Nom), (Pron Nom Pl) if; a verb is Pl3 or Du3 to your left. The verb is not allowed to be copulas with a place, Loc or time noun to its left

* **copPl3<subj** (@<SUBJ) for Nom Pl; you don't to be a noun, only Nom Pl. To the left is copulas and first one to the right is @<SPRED

* **-fsubj>** (@-FSUBJ>) for HUMAN Gen; in a NP-clause. To your right is Actio Nom followed by a noun

* **f<advl** (@-F<ADVL) for infinite adverbials

* **f<advl** (@-F<ADVL) for infinite adverbials

* **s-boundary=advl>** (@ADVL>) for ADVL that resemble s-boundaries. Mainverb to the right.

* **diibmuadvl>** (@ADVL>) for (diibmu Nom) if first one to the right is Num

* **-fsubj** (@-FSUBJ>) for HUMAN Acc after DADJAT verbs

* **-fobj>** (@-FOBJ>) for Acc if front of abessive, gerundium, actio locative, perfectum participle or infinitive. First one to the right not allowed to be Acc though

* **-fobj>** (@-FOBJ>) for Acc if human with ADVL-case to the left and transitive infinitive OBJ to the right. First one to the right not allowed to be Acc though

* **advl>mainV** (@ADVL>) if; finite mainverb not found to the left, but the finite mainverb is found to the right.

* **V<advl** (@<ADVL) if; finite mainverb found to the left. Not if a comma is found immediately to the left and a finite mainverb is located somewhere to the right of this comma.

* **advl>v** (@ADVL>) if; you are ADVL, time-noun or Sem/Route and there is a finite verb to the right in the clause, or if to your right is: de followed by a finite verb. OR: if you are a time-nound and to your right is: go or sentenceboundary followed by a finite verb

* **<advlPoPr** (@<ADVL) for Po or Pr; if mainverb to the left.
* **advlPoPr>** (@<ADVL) for Po or Pr; if mainverb to the right.

* **BOSPo>** (@ADVL>) for Po; if trapped between BOS to the right and S-BOUNDARY OR COMMA to the left, because the main verb will then automatically be on your right side.

* **<advlComIll** (@<ADVL) only if; you are Com OR Ill. To your left is a mainverb, and to your right a sentenceboundary, because we don't want there to be another mainverb you potentially could belong to

* **<advlEOS** (@<ADVL) for Po or Pr or Loc; if you are found at the very end of a sentence. A mainverb is needed to the left though.

* **<advlGen** (@<ADVL) for (N Gen) if mainverb to the left and no noun to the right

* **<opredgohcodit** (@<OPRED) for Ess

* **advlEss>** (@<ADVL) for weather and time Ess, if FMAINV to the left.

* **comma<advlEOS** (@<ADVL) for Adv if; mainverb is to the left. Comma to the left and mainverb to the right in the same clause is not allowed

* **advl>inbetween** (@ADVL>) for Adv; if inbetween two sentenceboundaries where no mainverb is present.

* **comma<advlEOS** (@<ADVL) for Adv if; comma found to the left and the finite mainverb to the left of comma. To the right is the end of the sentence.

* **BOSadvl>** (@ADVL>) if; you are N Loc or N Ill and found sentence initially and there is a main verb somewhere to the right. No barrier for the mainverb; based on the thought that first one to your right is probably a sentenceboundary.

* **cleanupILL<advl** (@<ADVL) for N Ill if; there are no boundarysymbols to your left, if you arent already @N< OR @APP-N<, and no mainverb is to yor left.

* **cleanupPo** (@ADVL) for Po: This rule tags all Po:s as ADVL if they haven't gotten a tag somewhere along the way.

* **cleanupPr** (@ADVL) for Po: This rule tags all Pr:s as ADVL if they haven't gotten a tag somewhere along the way.

* **-fsubj>asAcc** (@-FSUBJ>) for HUMAN Acc; if there is a verb @-F<OBJ to your left

* **-f<obj** (@-F<OBJ) for Acc if there is a transitive verb + SYN-V to your left

* **-fsubj>IV** (@-FSUBJ>) for Acc; if there is an IV-verb acting as a @-F<OBJ to your right

* **-fsubj>IV** (@-FSUBJ>) for Acc; if there is an TV-verb acting as a @-F<OBJ to your right followed by an Acc

* **-fsubj>asGen** (@-FSUBJ>) for Gen;

* **f<subj** (@-F<SUBJ) for Nom if; (V @-F<OBJ) to the left.

* **<opredAAcc** (@<OPRED) for A Acc; if an other accusative to the left, and a transtive verb to the left of it. OR: if a transitive verb to the left, and an accusative to the left of it.

* **TV<obj** (@<OBJ) for Acc; if there is a transitive mainverb to the left in the clause. Not for Rel. Not if you are a numeral followed by a measure-noun

### sma object

* **<advlMeasr** (@<ADVL) for (Num Acc); if finite IV-mainverb to the left, measure-noun to the right

* **<objMeasr** (@<OBJ) for Num Acc; if finite TV-mainverb to the left, measure-noun to the right

* **<advlMeasr2** (@<ADVL) for MEASR-N + Acc; if (Num Pl) to the left and mainverb to the left of it

* **advlMeasr>** (@ADVL>) for Num Acc;

* **Obj>** (@OBJ>) for Acc; if there is a finite mainverb to the right in the clause. A really simple rule with no other restrictions..

* **s-boun<obj** (@<OBJ) for Acc; if sentenceboundary to your left and a transitive mainverb to the left futher to the left

* **<objIV** (@<OBJ) for Acc; if there is an intransitive mainverb in the clause. Not for Rel or Num. Not if you are a numeral followed by a measure-noun

* **<advlEss** (@<ADVL) for ESS-ADVL if; FMAINV to the left

* **IV<spredEss** (@<SPRED) for N Ess if; FMAINV to the left is intransitive or bargat

* **<opredEss** (@<OPRED) for (N Ess), (A Ess) if; transitive mainverb to the left in the clause. If accusative to the left or to the right, or if Inf or ahte to the right, or if there is a noun to the right followed by an Inf

* **Acc<opredEss** (@<OPRED) for (N Ess), (A Ess) if; transitive mainverb to the left in the clause, and an accusative cased Rel left to the verb

* **onlyV<opred** (@<OPRED) for (N Ess) if; there is a transitive mainverb to the left. Usually there needs to be an Acc to the left, but here it is not needed

* **onlyV<opred2** (@<OPRED) for (N Ess) if;

## SUBJ MAPPING - leftovers

* **subj>ifV** (@SUBJ>) for NP-HEAD-NOM, DUPRON or (Num Nom) if; a finite mainverb is found to the right. This is a cleanup rule for subjects

* **hnoun>ifV** (@SUBJ>) for NP-HEAD-NOM, DUPRON if. The counterpart of subj>ifV. You are HNOUN if there is a finite verb to your right, but NOT if there is a finite verb after a relative clause

## OBJ MAPPING - leftovers

## <logo> MAPPING for MT - experimental

## HNOUN MAPPING

* **@<ADVLcoor** (@<ADVL) for ADVLCASEAdv if @CNP to the left and ADVL to the left of it

###  **missingX** adds @X to all missings

###  **therestX** adds @X to all what is left, often errouneus disambiguated forms

## For Apertium:
The analysis give double analysis because of optional semtags. We go for the one with semtag.

* * *
<small>This (part of) documentation was generated from [src/cg3/functions.cg3](https://github.com/giellalt/lang-vro/blob/main/src/cg3/functions.cg3)</small>Adjective inflection
The VÕRO language adjectives compare.

LEXICON A_1HANS1A  1 hanśa:hanśa

LEXICON A_1HERRAE  1 herrä:herrä

LEXICON A_2ARTIKLI  suhvli:suhvli
* Yaml: **suhvli**

LEXICON A_2KERGE  1 kerge:

LEXICON A_3ALADU  aladu:aladu
* Yaml: **A-aladu**

LEXICON A_3PERAEDUE  perädü:perädü
* Yaml: **A-peraedue**

LEXICON A_4AINUS   ainus:ainus

* LEXICON A_8KULDNW  kuldnõ:kuld
* LEXICON A_8KIIL1NE  kiiĺne:ki̬i̬ĺ
* LEXICON A_8KOLMAS  kolmas:kolma

* LEXICON A_8VIIES  viies:viie

* LEXICON A_9ALLAS1 

* LEXICON A_9SINNEL1 

* LEXICON A_9TAHHE 

* LEXICON A_9HERRE 

* LEXICON A_9KIPWN1/ELLAEI  what is this
* Yaml: **ellaei, suhvli**

* LEXICON A_9SALLAI  what is this
* Yaml: **ellaei, suhvli**
* Yaml: **ellaei, suhvli**

* Yaml: **ellaei, suhvli**

* Yaml: **allwv1, kipwn1**

* Yaml: **villw**

* Yaml: **tukwv**

* Yaml: **verrev**

* Yaml: **sallai**

LEXICON A_11AINWQ  ainõq:ainõ

LEXICON A_11KELMEQ  kelmeq:kelme

LEXICON A_13ALONW  alonõ:alo

LEXICON A_13TAEHINE  tähine:tähi

LEXICON A_13TAEHINE_PL  tähine:tähi

LEXICON A_14RITS1KAS   ritśkas:ritśka%{sØ%}

LEXICON A_14HAMMAS   rikas:ri%{kØ%}ka%{sØ%}

LEXICON A_14IKAES   rikas:ri%{kØ%}ka%{sØ%}

LEXICON A_16ABILINW  inemine:inemi
LEXICON A_16INEMINE  inemine:inemi

LEXICON A_19ALOMANW  alomanõ:aloma

LEXICON A_19PEDAEJAENE  pedäjäne:pedäjä

LEXICON A_19PEDAEJAENE_PL  pedäjäne:pedäjä

LEXICON A_22VWROKWNW  võrokõnõ:võrokõ

LEXICON A_22VAEHAEKENE  võrokõnõ:võrokõ

gradation: no

gradation: yes

gradation: no

* LEXICON A_2KASUNUQ  kasunuq:kasunu
* LEXICON A_2ELAENUEQ  elänüq:elänü

* +Err/Dial+Pl+Com:id%{eõ%}ga K ;  no q

* * *

<small>This (part of) documentation was generated from [src/fst/affixes/adjectives.lexc](https://github.com/giellalt/lang-vro/blob/main/src/fst/affixes/adjectives.lexc)</small>

---

Adverbs 
The VÕRO language adverbs...

Spatial adverbs

adjective modifiers

What is this 2017-03-27

* * *

<small>This (part of) documentation was generated from [src/fst/affixes/adverbs.lexc](https://github.com/giellalt/lang-vro/blob/main/src/fst/affixes/adverbs.lexc)</small>

---

Noun inflection for Võro

LEXICON N_1HANS1A  1 hanśa:hanśa

LEXICON N_1VIU  1 viu:viu

LEXICON N_1HERRAE  1 herrä:herrä

LEXICON N_1PREI  1 prei:prei

* Yaml: **suhvli**

* Yaml: **kerge**

LEXICON N_3PERAEDUE  perädü:perädü
* Yaml: **peraedue**

LEXICON N_3ALADU  aladu:aladu
* Yaml: **peraedue**

* Yaml: **tervues**

* Yaml: **A-ainus**

* Yaml: **N-oppaja5**

* Yaml: **N-mängjä5**

* Yaml: **fueuesiga**

kipõń:kipõn
* Yaml:**N-kipwnj9**

allaś:allas
* Yaml:**N-kipwnj9**

sinneĺ:sinnel
* Yaml:**N-kipwnj9**

veteĺ:vetel
* Yaml:**N-kipwnj9**

tukõv:tukõv
* Yaml: **N-ellaei4, N-kipwnj9**

verrev:verrev
* Yaml: **N-ellaei4, N-kipwnj9**

sallai:sallai
* Yaml: **N-ellaei4, N-kipwnj9**

elläi:elläi
* Yaml: **N-ellaei4, N-kipwnj9**

herre:herre
* Yaml:**N-kipwnj9**

villõ:villõ
* Yaml:**N-kipwnj9**

LEXICON N_10HWRAK  hõrak:hõrak

* Noun 10 hõrak  examples:*
* *hõrak:* `hõrak+N+Sg+Nom`
* *hõraga:* `hõrak+N+Sg+Gen`
* *hõrakat:* `hõrak+N+Sg+Par`
* *hõrakahe:* `hõrak+N+Sg+Ill`
* *hõrakan:* `hõrak+N+Sg+Ine`
* *hõrakast:* `hõrak+N+Sg+Ela`
* *hõrakalõ:* `hõrak+N+Sg+All`
* *hõrakal:* `hõrak+N+Sg+Ade`
* *hõrakalt:* `hõrak+N+Sg+Abl`
* *hõrakas:* `hõrak+N+Sg+Tra`
* *hõrakaniq:* `hõrak+N+Sg+Ter`
* *hõrakaldaq:* `hõrak+N+Sg+Abe`
* *hõragagaq:* `hõrak+N+Sg+Com`
* *hõragaq:* `hõrak+N+Pl+Nom`
* *hõrakidõ:* `hõrak+N+Pl+Gen`
* *hõrakit:* `hõrak+N+Pl+Par`
* *hõrakihe:* `hõrak+N+Pl+Ill`
* *hõrakin:* `hõrak+N+Pl+Ine`
* *hõrakist:* `hõrak+N+Pl+Ela`
* *hõrakilõ:* `hõrak+N+Pl+All`
* *hõrakil:* `hõrak+N+Pl+Ade`
* *hõrakilt:* `hõrak+N+Pl+Abl`
* *hõrakis:* `hõrak+N+Pl+Tra`
* *hõrakiniq:* `hõrak+N+Pl+Ter`
* *hõrakildaq:* `hõrak+N+Pl+Abe`
* *hõrakidõgaq:* `hõrak+N+Pl+Com`

LEXICON N_10HAIDAK  haidak:haidak

LEXICON N_10ESAEK  esäk:esäk

LEXICON N_10RAAMAT  raamat:raamat

LEXICON N_10LEMBIT  esäk:esäk

LEXICON N_10AABITS  aabits:aabits

LEXICON N_10HEERITS  heerits:heerits

LEXICON N_10AADRWS1  aadrõś:aadrõs

LEXICON N_10AMMAT1  ammat́:ammat

LEXICON N_10HUEPAETS1  hüpätś:hüpä%{td%}s

LEXICON N_11LAETEQ  läteq:lä%{tØ%}te

LEXICON N_11ANNWQ  annõq:andõ

LEXICON N_11AINWQ  ainõq:ainõ
LEXICON N_11KELMEQ  kelmeq:ainõ

LEXICON N_11VAIH  vaih:vaih

LEXICON N_12NWKWS1   nõkõś:nõ%{kg%}õ%{sś%}

LEXICON N_13ALONW  alonõ:alo

LEXICON N_13TAEHINE  tähine:tähi

Gradation: No

LEXICON N_14RITS1KAS  ritśkas:ritśka%{sØ%}

Gradation: No

LEXICON N_14HAMMAS  hammas:ham%{bm%}a%{sØ%}, saabas:saapa
distinguished from 14RITS1KAS due to gradation

LEXICON N_14IKAES  ikäs:ikkä
distinguished from 14RITS1KAS due to gradation

LEXICON N_14NUMMWR1  nummõŕ:numbõr
distinguished from 14RITS1KAS due to gradation

vowel_harmony: front
gradation: yes

vowel_harmony: back
gradation: yes

kotus:kotus
* Yaml: **N-kotus15**

kotus:kotus
* Yaml: **N-ilves15**

LEXICON N_16INEMINE 
inemine:inemi
* Yaml: **N-inemine16**

LEXICON N_16ABILINW 
abilinõ:abili
* Yaml: **N-abilinw16**

LEXICON N_16TERAEKENE 
inemine:inemi
* Yaml: **N-inemine16**

LEXICON N_16TSIRGUKWNW 
tsirgukõnõ:abili
* Yaml: **N-abilinw16**

LEXICON N_19ALOMANW  alomanõ:aloma

LEXICON N_19PEDAEJAENE  pedäjäne:pedäjä

LEXICON N_20LATS1  latś:lat%{sś%}

LEXICON N_20TAEUES1  täüś:täü

LEXICON N_20VIIS1  täüś:täü

LEXICON N_20ORS1  täüś:täü

LEXICON N_20HIRS1  täüś:täü

LEXICON N_20VAEITS1  väitś:väits

LEXICON N_20KUEUEDS1  küüdś:küüds

LEXICON N_20MIIS1  miiś:m

LEXICON N_21HUEDSI  hüdsi:hü

LEXICON N_21KUSI  kusi:kus

LEXICON N_22VWROKWNW  võrokõnõ:võrokõ

LEXICON N_22NAANW  naanõ:naa

LEXICON N_22VAEHAEKENE  vähäkene:vähäke

* LEXICON N_23NUUL1  nuuĺ:n%{ou%}%{ou%}l

* LEXICON N_23SUUR1  suuŕ:suur

* LEXICON N_23KIIL1   kiiĺ:keel

* LEXICON N_23HIIR1   hiiŕ:hiir

* LEXICON N_24KAESI  käsi:kä

* LEXICON N_24SUSI  susi:su

gradation: yes

* **LEXICON N_27KUEMMEND ** kümmend:küm

* **LEXICON N_28TUETAER1 ** tütäŕ:tütär

* **LEXICON N_28PINNAER1 ** pinnäŕ:pin%{dn%}är

* **LEXICON N_28PAPWR1 ** papõŕ:papõr

* **LEXICON N_28KANNWL1 ** kannõĺ:kan%{dn%}õl

* **LEXICON N_28KINNER1 ** kinneŕ:kin%{dn%}er

* **LEXICON N_28SWSAR1 ** sõsaŕ:sõsar

* **LEXICON N_28PUNDAR ** pundar:pun%{td%}ar

* **LEXICON N_28KAEMMAEL ** kämmäl:käm%{bm%}äl

* LEXICON N_29KUU  kuu:kuu

* LEXICON N_29HAEAE  pää:pää

* Noun 33 examples:*

tarõ:tar

uma:uma

pesä:pesä

nimi:ni%{mØ%}m

lumi:lum

LEXICON N_36TUUM1  tuuḿ:t%{ou%}%{ou%}m

LEXICON N_36HANG1  hanǵ:hang

LEXICON N_36SAERG1  särǵ:sär%{gǵØ%}

LEXICON N_36LAHT1  laht́:lah%{tt́Ø%}

LEXICON N_36PAEIV  päiv:päiv

LEXICON N_36LEIB  päiv:päiv

* LEXICON N_36SILM  silm:silm
harmony: front

* LEXICON N_36RAMM  ramm:ramm
harmony: back

* LEXICON N_36TIIM  tiim:t%{ei%}%{ei%}m
harmony: front

* LEXICON N_36NJUKR  ńukr:ńu%{kg%}r
harmony: back

* LEXICON N_36LAEHK  lähk:läh%{kØ%}
harmony: front

kogõr:kogõr
* Yaml: **N-kogwr36**
derived from 36särǵ

kokr:ko%{kg%}r
* Yaml: **N-kogwr36**
derived from 36särǵ

sõbõr:sõbõr
oblique plural in o
* Yaml: **N-swbwr36**
derived from 36särǵ

kubõl:ku%{pb%}õl
oblique plural in õ
* Yaml: **N-swbwr36**
derived from 36särǵ

LEXICON N_37PINI  pini:pini

LEXICON N_37WLI  õli:õli

LEXICON N_37MUNA  muna:mu%{nØ%}na

* LEXICON N_38HUETT  hütt:hütt

* LEXICON N_39VIDO  vido:vi%{tØ%}%{tdØ%}o

* LEXICON N_39HAEBUE  häbü:hä%{pØ%}%{pbØ%}ü

LEXICON N_40TALO  talo:ta%{lØ%}lo

LEXICON N_40HELUE  helü:helü

LEXICON N_40UJA  uja:u%{jØ%}ja

LEXICON N_40IJAE  ijä:i%{jØ%}jä

LEXICON N_40SAVV  savv:savvu

LEXICON N_40TUEKK  tükk:tü%{kØ%}kü

LEXICON N_41JUHT1  juht́:juht
* Yaml: **juht́**

LEXICON N_41AIG  aig:a
* Yaml: **aig, aig**

LEXICON N_41ASK  aig:aig
* Yaml: **aig, aig**
ask:as%{kØ%}o
juusk:j%{ou%}%{ou%}s%{kØ%}u

LEXICON N_41MAENG  aig:aig
* Yaml: **aig, aig**
ask:as%{kØ%}o
juusk:j%{ou%}%{ou%}s%{kØ%}u

LEXICON N_41VIIT  aig:aig
* Yaml: **aig, aig**

LEXICON N_43KANARIK  usklik+A:%{ˋØ%}#uskli%{kØ%}%{kg%}

LEXICON N_43ELAENIK  elänik+N:eläni%{kØ%}%{kg%}

LEXICON N_43SASLWK1 

LEXICON N_43APRIL1 

LEXICON N_43SEKRETAER1 

LEXICON N_43AASTAK 

LEXICON N_44SWDA  sõda:sõ%{tØ%}%{tdØ%}a

LEXICON N_45KANA  kana:ka%{nØ%}na

LEXICON N_45RIHAE  rihä:ri%{hØ%}hä

LEXICON N_46HAIN  hain:hain
* Yaml: **N-jalg, N-hain**

LEXICON N_46TARK  tark:tark
* Yaml: **N-jalg, N-tark**

LEXICON N_47ASI  asi:asi

LEXICON N_47VELI  veli:ve%{lØ%}l

LEXICON N_47KIRI  kiri:kiri

### NOMINAL DECLENSIONS

LEXICON NMN_1HANS1A  1 hanśa:hanśa

* Noun 01 hanśa examples:*
* *hanśa* `hanśa+N+Sg+Nom:`
* *hanśat* `hanśa+N+Sg+Par:`
* *hanśahtõ* `hanśa+N+Sg+Ill:`
* *hanśast* `hanśa+N+Sg+Ela:`
* *hanśalõ* `hanśa+N+Sg+All:`
* *hanśal* `hanśa+N+Sg+Ade:`
* *hanśalt* `hanśa+N+Sg+Abl:`
* *hanśas* `hanśa+N+Sg+Tra:`
* *hanśaniq* `hanśa+N+Sg+Ter:`
* *hanśaldaq* `hanśa+N+Sg+Abe:`
* *hanśagaq* `hanśa+N+Sg+Com:`
* *hanśaq* `hanśa+N+Pl+Nom:`
* *hanśasit* `hanśa+N+Pl+Par:`
* *hanśadõhe* `hanśa+N+Pl+Ill:`
* *hanśadõst* `hanśa+N+Pl+Ela:`
* *hanśadõlõ* `hanśa+N+Pl+All:`
* *hanśadõl* `hanśa+N+Pl+Ade:`
* *hanśadõlt* `hanśa+N+Pl+Abl:`
* *hanśadõs* `hanśa+N+Pl+Tra:`
* *hanśadõniq* `hanśa+N+Pl+Ter:`
* *hanśadõldaq* `hanśa+N+Pl+Abe:`
* *hanśadõgaq* `hanśa+N+Pl+Com:`

in d

LEXICON NMN_1HERRAE  1 herrä:herrä

* Noun 01 herrä examples:*
* *herrä* `herrä+N+Sg+Nom:`
* *herrät* `herrä+N+Sg+Par:`
* *herrähte* `herrä+N+Sg+Ill:`
* *herräst* `herrä+N+Sg+Ela:`
* *herräle* `herrä+N+Sg+All:`
* *herräl* `herrä+N+Sg+Ade:`
* *herrält* `herrä+N+Sg+Abl:`
* *herräs* `herrä+N+Sg+Tra:`
* *herräniq* `herrä+N+Sg+Ter:`
* *herräldäq* `herrä+N+Sg+Abe:`
* *herrägaq* `herrä+N+Sg+Com:`
* *herräq* `herrä+N+Pl+Nom:`
* *herräsit* `herrä+N+Pl+Par:`
* *herrädehe* `herrä+N+Pl+Ill:`
* *herrädest* `herrä+N+Pl+Ela:`
* *herrädele* `herrä+N+Pl+All:`
* *herrädel* `herrä+N+Pl+Ade:`
* *herrädelt* `herrä+N+Pl+Abl:`
* *herrädes* `herrä+N+Pl+Tra:`
* *herrädeniq* `herrä+N+Pl+Ter:`
* *herrädeldäq* `herrä+N+Pl+Abe:`
* *herrädegaq* `herrä+N+Pl+Com:`

in d

* Yaml: **suhvli**

* Yaml: **kerge**

LEXICON NMN_3PERAEDUE  perädü:perädü
* Yaml: **A-peraedue3** same as aladu

LEXICON NMN_3ALADU  aladu:aladu

* Noun 03 aladu examples:*
* *aladu* `aladu+A+Sg+Nom:`
* *alatut* `aladu+A+Sg+Par:`
* *alatuhe* `aladu+A+Sg+Ill:`
* *alatuid* `aladu+A+Pl+Par:`
* *alatuihe* `aladu+A+Pl+Ill:`
* *alatuilõ* `aladu+A+Pl+All:`
* *alatumb* `aladu+A+Comp+Sg+Nom:`

* Yaml: **A-aladu3**

* Noun 04 tervüs examples:*
* *tervüs* `tervüs+N+Sg+Nom:`
* *tervüst* `tervüs+N+Sg+Par:`
* *tervüste* `tervüs+N+Sg+Ill:`
* *tervüsest* `tervüs+N+Sg+Ela:`
* *tervüsele* `tervüs+N+Sg+All:`
* *tervüsel* `tervüs+N+Sg+Ade:`
* *tervüselt* `tervüs+N+Sg+Abl:`
* *tervüses* `tervüs+N+Sg+Tra:`
* *tervüseniq* `tervüs+N+Sg+Ter:`
* *tervüseldäq* `tervüs+N+Sg+Abe:`
* *tervüsegaq* `tervüs+N+Sg+Com:`
* *tervüseq* `tervüs+N+Pl+Nom:`
* *tervüisi* `tervüs+N+Pl+Par:`
* *tervüisihe* `tervüs+N+Pl+Ill:`
* *tervüisist* `tervüs+N+Pl+Ela:`
* *tervüisile* `tervüs+N+Pl+All:`
* *tervüisil* `tervüs+N+Pl+Ade:`
* *tervüisilt* `tervüs+N+Pl+Abl:`
* *tervüisis* `tervüs+N+Pl+Tra:`
* *tervüisiniq* `tervüs+N+Pl+Ter:`
* *tervüisildäq* `tervüs+N+Pl+Abe:`
* *tervüisigaq* `tervüs+N+Pl+Com:`

* +Err/Dial:%^VowRM%^CnsRM%>i Harm_Neutr_PL_GEN_dE ;  tervide
* +Err/Dial:%^VowRM%^CnsRM%>i PL_ILL_he ;  tervihe

* **LEXICON NMN_4AINUS ** Types 4, 8, 17

* Noun 04 examples:*
* *ainus* `ainus+A+Sg+Nom:`
* *ainut* `ainus+A+Sg+Par:`
* *ainuhe* `ainus+A+Sg+Ill:`
* *ainust* `ainus+A+Sg+Ela:`
* *ainulõ* `ainus+A+Sg+All:`
* *ainul* `ainus+A+Sg+Ade:`
* *ainult* `ainus+A+Sg+Abl:`
* *ainus* `ainus+A+Sg+Tra:`
* *ainuniq* `ainus+A+Sg+Ter:`
* *ainuldaq* `ainus+A+Sg+Abe:`
* *ainugaq* `ainus+A+Sg+Com:`
* *ainuq* `ainus+A+Pl+Nom:`
* *ainuid* `ainus+A+Pl+Par:`
* *ainuihe* `ainus+A+Pl+Ill:`
* *ainuist* `ainus+A+Pl+Ela:`
* *ainuilõ* `ainus+A+Pl+All:`
* *ainuil* `ainus+A+Pl+Ade:`
* *ainuilt* `ainus+A+Pl+Abl:`
* *ainuis* `ainus+A+Pl+Tra:`
* *ainuiniq* `ainus+A+Pl+Ter:`
* *ainuildaq* `ainus+A+Pl+Abe:`
* *ainuidõgaq* `ainus+A+Pl+Com:`
* *ainumb* `ainus+A+Comp+Sg+Nom:`

ainus:ainus
* Yaml: **A-ainus4**

* LEXICON NMN_5OPPAJA/MAENGJAE  oppaja:oppaja

* Adjective 05 kerge examples:*
* *kerge* `kerge+A+Sg+Nom:`
* *kerget* `kerge+A+Sg+Par:`
* *kergehe* `kerge+A+Sg+Ill:`
* *kergest* `kerge+A+Sg+Ela:`
* *kergele* `kerge+A+Sg+All:`
* *kergel* `kerge+A+Sg+Ade:`
* *kergelt* `kerge+A+Sg+Abl:`
* *kerges* `kerge+A+Sg+Tra:`
* *kergeniq* `kerge+A+Sg+Ter:`
* *kergeldäq* `kerge+A+Sg+Abe:`
* *kergegaq* `kerge+A+Sg+Com:`
* *kergeq* `kerge+A+Pl+Nom:`
* *kergit* `kerge+A+Pl+Par:`
* *kergihe* `kerge+A+Pl+Ill:`
* *kergist* `kerge+A+Pl+Ela:`
* *kergile* `kerge+A+Pl+All:`
* *kergil* `kerge+A+Pl+Ade:`
* *kergilt* `kerge+A+Pl+Abl:`
* *kergis* `kerge+A+Pl+Tra:`
* *kerginiq* `kerge+A+Pl+Ter:`
* *kergildäq* `kerge+A+Pl+Abe:`
* *kergidegaq* `kerge+A+Pl+Com:`

* Yaml: **N-oppaja5, kerge5**

* LEXICON NMN_6MAKW/HELLE  makõ:ma%{kØ%}kõ

* Adjective (6) tikõ 'eng /est /fin' - full paradigm: Noun - tikõ examples:*
* *tikõ:* `tikõ+A+Sg+Nom`
* *tikõ:* `tikõ+A+Sg+Gen`
* *tikõt:* `tikõ+A+Sg+Par`
* *tikkõhe:* `tikõ+A+Sg+Ill`
* *tikkidõ:* `tikõ+A+Pl+Gen`
* *tikkit:* `tikõ+A+Pl+Par`
* *tikkihe:* `tikõ+A+Pl+Ill`
* *tikkilõ:* `tikõ+A+Pl+All`

* Noun 07 füüsiga examples:*
* *füüsiga* `füüsiga+N+Sg+Nom:`
* *füüsikat* `füüsiga+N+Sg+Par:`
* *füüsikahe* `füüsiga+N+Sg+Ill:`
* *füüsikast* `füüsiga+N+Sg+Ela:`
* *füüsikalõ* `füüsiga+N+Sg+All:`
* *füüsikal* `füüsiga+N+Sg+Ade:`
* *füüsikalt* `füüsiga+N+Sg+Abl:`
* *füüsikas* `füüsiga+N+Sg+Tra:`
* *füüsikaniq* `füüsiga+N+Sg+Ter:`
* *füüsikaldaq* `füüsiga+N+Sg+Abe:`
* *füüsigagaq* `füüsiga+N+Sg+Com:`
* *füüsigaq* `füüsiga+N+Pl+Nom:`
* *füüsikit* `füüsiga+N+Pl+Par:`
* *füüsikihe* `füüsiga+N+Pl+Ill:`
* *füüsikist* `füüsiga+N+Pl+Ela:`
* *füüsikilõ* `füüsiga+N+Pl+All:`
* *füüsikil* `füüsiga+N+Pl+Ade:`
* *füüsikilt* `füüsiga+N+Pl+Abl:`
* *füüsikis* `füüsiga+N+Pl+Tra:`
* *füüsikiniq* `füüsiga+N+Pl+Ter:`
* *füüsikildaq* `füüsiga+N+Pl+Abe:`
* *füüsikidõgaq* `füüsiga+N+Pl+Com:`

* Noun 08 kask examples:*
* *kask* `kask+N+Sg+Nom:`
* *kaskat* `kask+N+Sg+Par:`
* *kaskahe* `kask+N+Sg+Ill:`
* *kaskast* `kask+N+Sg+Ela:`
* *kaskalõ* `kask+N+Sg+All:`
* *kaskal* `kask+N+Sg+Ade:`
* *kaskalt* `kask+N+Sg+Abl:`
* *kaskas* `kask+N+Sg+Tra:`
* *kaskaniq* `kask+N+Sg+Ter:`
* *kaskaldaq* `kask+N+Sg+Abe:`
* *kaskagaq* `kask+N+Sg+Com:`
* *kaskaq* `kask+N+Pl+Nom:`
* *kaskit* `kask+N+Pl+Par:`
* *kaskihe* `kask+N+Pl+Ill:`
* *kaskist* `kask+N+Pl+Ela:`
* *kaskilõ* `kask+N+Pl+All:`
* *kaskil* `kask+N+Pl+Ade:`
* *kaskilt* `kask+N+Pl+Abl:`
* *kaskis* `kask+N+Pl+Tra:`
* *kaskiniq* `kask+N+Pl+Ter:`
* *kaskildaq* `kask+N+Pl+Abe:`
* *kaskidõgaq* `kask+N+Pl+Com:`

* Yaml: **N-kask**

Secondary

kuldnõ:kuld

* Adjective 08 kuldnõ examples:*
* *kuldnõ* `kuldnõ+A+Sg+Nom:`
* *kuldsõt* `kuldnõ+A+Sg+Par:`
* *kuldsõhe* `kuldnõ+A+Sg+Ill:`
* *kuldsõl* `kuldnõ+A+Sg+Ade:`
* *kuldsõlt* `kuldnõ+A+Sg+Abl:`
* *kuldsõs* `kuldnõ+A+Sg+Tra:`
* *kuldsõniq* `kuldnõ+A+Sg+Ter:`
* *kuldsõldaq* `kuldnõ+A+Sg+Abe:`
* *kuldsõgaq* `kuldnõ+A+Sg+Com:`
* *kuldsõq* `kuldnõ+A+Pl+Nom:`
* *kuldsit* `kuldnõ+A+Pl+Par:`
* *kuldsihe* `kuldnõ+A+Pl+Ill:`
* *kuldsist* `kuldnõ+A+Pl+Ela:`
* *kuldsilõ* `kuldnõ+A+Pl+All:`
* *kuldsil* `kuldnõ+A+Pl+Ade:`
* *kuldsilt* `kuldnõ+A+Pl+Abl:`
* *kuldsis* `kuldnõ+A+Pl+Tra:`
* *kuldsiniq* `kuldnõ+A+Pl+Ter:`
* *kuldsildaq* `kuldnõ+A+Pl+Abe:`
* *kuldsidõgaq* `kuldnõ+A+Pl+Com:`

* Yaml: **N-kuldnw**

Secondary

* LEXICON NMN_8KOLMAS/VIIES  kolmas:kolma

* Noun 08 kolmas examples:*
* *kolmas* `kolmas+N+Sg+Nom:`
* *kolmandat* `kolmas+N+Sg+Par:`
* *kolmandahe* `kolmas+N+Sg+Ill:`
* *kolmandast* `kolmas+N+Sg+Ela:`
* *kolmandalõ* `kolmas+N+Sg+All:`
* *kolmandal* `kolmas+N+Sg+Ade:`
* *kolmandalt* `kolmas+N+Sg+Abl:`
* *kolmandas* `kolmas+N+Sg+Tra:`
* *kolmandaniq* `kolmas+N+Sg+Ter:`
* *kolmandaldaq* `kolmas+N+Sg+Abe:`
* *kolmandagaq* `kolmas+N+Sg+Com:`
* *kolmandaq* `kolmas+N+Pl+Nom:`
* *kolmansidõ* `kolmas+N+Pl+Gen:`
* *kolmansit* `kolmas+N+Pl+Par:`
* *kolmansihe* `kolmas+N+Pl+Ill:`
* *kolmansist* `kolmas+N+Pl+Ela:`
* *kolmansilõ* `kolmas+N+Pl+All:`
* *kolmansil* `kolmas+N+Pl+Ade:`
* *kolmansilt* `kolmas+N+Pl+Abl:`
* *kolmansis* `kolmas+N+Pl+Tra:`
* *kolmansiniq* `kolmas+N+Pl+Ter:`
* *kolmansildaq* `kolmas+N+Pl+Abe:`
* *kolmansidõgaq* `kolmas+N+Pl+Com:`

* Yaml: **N-kuldnw**

* Noun 08 sadang examples:*
* *sadang* `sadang+N+Sg+Nom:`
* *sadangut* `sadang+N+Sg+Par:`
* *sadanguhe* `sadang+N+Sg+Ill:`
* *sadangust* `sadang+N+Sg+Ela:`
* *sadangulõ* `sadang+N+Sg+All:`
* *sadangul* `sadang+N+Sg+Ade:`
* *sadangult* `sadang+N+Sg+Abl:`
* *sadangus* `sadang+N+Sg+Tra:`
* *sadanguniq* `sadang+N+Sg+Ter:`
* *sadanguldaq* `sadang+N+Sg+Abe:`
* *sadangugaq* `sadang+N+Sg+Com:`
* *sadanguq* `sadang+N+Pl+Nom:`
* *sadangit* `sadang+N+Pl+Par:`
* *sadangihe* `sadang+N+Pl+Ill:`
* *sadangist* `sadang+N+Pl+Ela:`
* *sadangilõ* `sadang+N+Pl+All:`
* *sadangil* `sadang+N+Pl+Ade:`
* *sadangilt* `sadang+N+Pl+Abl:`
* *sadangis* `sadang+N+Pl+Tra:`
* *sadanginiq* `sadang+N+Pl+Ter:`
* *sadangildaq* `sadang+N+Pl+Abe:`
* *sadangidõgaq* `sadang+N+Pl+Com:`

Secondary

* Noun 08 tuhat examples:*
* *tuhat* `tuhat+N+Sg+Nom:`
* *tuhandõt* `tuhat+N+Sg+Par:`
* *tuhandõhe* `tuhat+N+Sg+Ill:`
* *tuhandõst* `tuhat+N+Sg+Ela:`
* *tuhandõlõ* `tuhat+N+Sg+All:`
* *tuhandõl* `tuhat+N+Sg+Ade:`
* *tuhandõlt* `tuhat+N+Sg+Abl:`
* *tuhandõs* `tuhat+N+Sg+Tra:`
* *tuhandõniq* `tuhat+N+Sg+Ter:`
* *tuhandõldaq* `tuhat+N+Sg+Abe:`
* *tuhandõgaq* `tuhat+N+Sg+Com:`
* *tuhandõq* `tuhat+N+Pl+Nom:`
* *tuhandidõ* `tuhat+N+Pl+Gen:`
* *tuhandit* `tuhat+N+Pl+Par:`
* *tuhandihe* `tuhat+N+Pl+Ill:`
* *tuhandist* `tuhat+N+Pl+Ela:`
* *tuhandilõ* `tuhat+N+Pl+All:`
* *tuhandil* `tuhat+N+Pl+Ade:`
* *tuhandilt* `tuhat+N+Pl+Abl:`
* *tuhandis* `tuhat+N+Pl+Tra:`
* *tuhandiniq* `tuhat+N+Pl+Ter:`
* *tuhandildaq* `tuhat+N+Pl+Abe:`
* *tuhandidõgaq* `tuhat+N+Pl+Com:`

* Noun 08 dollaŕ examples:*
* *dollaŕ* `dollaŕ+N+Sg+Nom:`
* *dollarit* `dollaŕ+N+Sg+Par:`
* *dollarihe* `dollaŕ+N+Sg+Ill:`
* *dollarist* `dollaŕ+N+Sg+Ela:`
* *dollarilõ* `dollaŕ+N+Sg+All:`
* *dollaril* `dollaŕ+N+Sg+Ade:`
* *dollarilt* `dollaŕ+N+Sg+Abl:`
* *dollaris* `dollaŕ+N+Sg+Tra:`
* *dollariniq* `dollaŕ+N+Sg+Ter:`
* *dollarildaq* `dollaŕ+N+Sg+Abe:`
* *dollarigaq* `dollaŕ+N+Sg+Com:`
* *dollariq* `dollaŕ+N+Pl+Nom:`
* *dollaridõ* `dollaŕ+N+Pl+Gen:`
* *dollarit* `dollaŕ+N+Pl+Par:`
* *dollarihe* `dollaŕ+N+Pl+Ill:`
* *dollarist* `dollaŕ+N+Pl+Ela:`
* *dollarilõ* `dollaŕ+N+Pl+All:`
* *dollaril* `dollaŕ+N+Pl+Ade:`
* *dollarilt* `dollaŕ+N+Pl+Abl:`
* *dollaris* `dollaŕ+N+Pl+Tra:`
* *dollariniq* `dollaŕ+N+Pl+Ter:`
* *dollarildaq* `dollaŕ+N+Pl+Abe:`
* *dollaridõgaq* `dollaŕ+N+Pl+Com:`

Secondary

* Noun 10 aastak  examples:*
* *aastak:* `aastak+N+Sg+Nom`
* *aastaga:* `aastak+N+Sg+Gen`
* *aastakat:* `aastak+N+Sg+Par`
* *aastakahe:* `aastak+N+Sg+Ill`
* *aastakan:* `aastak+N+Sg+Ine`
* *aastakast:* `aastak+N+Sg+Ela`
* *aastakalõ:* `aastak+N+Sg+All`
* *aastakal:* `aastak+N+Sg+Ade`
* *aastakalt:* `aastak+N+Sg+Abl`
* *aastakas:* `aastak+N+Sg+Tra`
* *aastakaniq:* `aastak+N+Sg+Ter`
* *aastakaldaq:* `aastak+N+Sg+Abe`
* *aastagagaq:* `aastak+N+Sg+Com`
* *aastagaq:* `aastak+N+Pl+Nom`
* *aastakidõ:* `aastak+N+Pl+Gen`
* *aastakit:* `aastak+N+Pl+Par`
* *aastakihe:* `aastak+N+Pl+Ill`
* *aastakin:* `aastak+N+Pl+Ine`
* *aastakist:* `aastak+N+Pl+Ela`
* *aastakilõ:* `aastak+N+Pl+All`
* *aastakil:* `aastak+N+Pl+Ade`
* *aastakilt:* `aastak+N+Pl+Abl`
* *aastakis:* `aastak+N+Pl+Tra`
* *aastakiniq:* `aastak+N+Pl+Ter`
* *aastakildaq:* `aastak+N+Pl+Abe`
* *aastakidõgaq:* `aastak+N+Pl+Com`
**N-hwrak10**

* **LEXICON NMN_36RAMM/SILM ** silm:silm

* Noun 36 silmä ämm examples:*
* *ämm* `ämm+N+Sg+Nom:`
* *ämmä* `ämm+N+Sg+Par:`
* *ämmä* `ämm+N+Sg+Ill:`
* *ämmäst* `ämm+N+Sg+Ela:`
* *ämmäle* `ämm+N+Sg+All:`
* *ämmäl* `ämm+N+Sg+Ade:`
* *ämmält* `ämm+N+Sg+Abl:`
* *ämmäs* `ämm+N+Sg+Tra:`
* *ämmäniq* `ämm+N+Sg+Ter:`
* *ämmäldäq* `ämm+N+Sg+Abe:`
* *ämmägaq* `ämm+N+Sg+Com:`
* *ämmäq* `ämm+N+Pl+Nom:`
* *ämmi* `ämm+N+Pl+Par:`
* *ämmihe* `ämm+N+Pl+Ill:`
* *ämmist* `ämm+N+Pl+Ela:`
* *ämmile* `ämm+N+Pl+All:`
* *ämmil* `ämm+N+Pl+Ade:`
* *ämmilt* `ämm+N+Pl+Abl:`
* *ämmis* `ämm+N+Pl+Tra:`
* *ämminiq* `ämm+N+Pl+Ter:`
* *ämmildäq* `ämm+N+Pl+Abe:`
* *ämmigaq* `ämm+N+Pl+Com:`

* Yaml: **N-silm36**
gradation No, vowelHarmony Front

Secondary

Secondary

* **LEXICON NMN_36NJUKR/LAEHK ** lähk:läh%{kØ%}

* Noun 36 lähk examples:*
* *lähk* `lähk+N+Sg+Nom:`
* *lähkä* `lähk+N+Sg+Par:`
* *lähkä* `lähk+N+Sg+Ill:`
* *lähäst* `lähk+N+Sg+Ela:`
* *lähäle* `lähk+N+Sg+All:`
* *lähäl* `lähk+N+Sg+Ade:`
* *lähält* `lähk+N+Sg+Abl:`
* *lähäs* `lähk+N+Sg+Tra:`
* *lähäniq* `lähk+N+Sg+Ter:`
* *lähäldäq* `lähk+N+Sg+Abe:`
* *lähägaq* `lähk+N+Sg+Com:`
* *lähäq* `lähk+N+Pl+Nom:`
* *lähki* `lähk+N+Pl+Par:`
* *lähkihe* `lähk+N+Pl+Ill:`
* *lähist* `lähk+N+Pl+Ela:`
* *lähile* `lähk+N+Pl+All:`
* *lähil* `lähk+N+Pl+Ade:`
* *lähilt* `lähk+N+Pl+Abl:`
* *lähis* `lähk+N+Pl+Tra:`
* *lähiniq* `lähk+N+Pl+Ter:`
* *lähildäq* `lähk+N+Pl+Abe:`
* *lähkigaq* `lähk+N+Pl+Com:`

* Yaml: **N-lähk36**
gradation Yes, vowelHarmony Front

Secondary

Secondary

LEXICON NMN_9KIPWN1/ELLAEI  kipõń:kipõń fixme 2016-08-27
* Yaml: **N-kipwnj**
LEXICON NMN_9KIPWN1/VETEL1  kipõń:ki%{pb%}õ%{nń%}

* Noun 09 kipõń examples:*
* *kipõń* `kipõń+N+Sg+Nom:`
* *kibõnat* `kipõń+N+Sg+Par:`
* *kibõnahe* `kipõń+N+Sg+Ill:`
* *kibõnast* `kipõń+N+Sg+Ela:`
* *kibõnalõ* `kipõń+N+Sg+All:`
* *kibõnal* `kipõń+N+Sg+Ade:`
* *kibõnalt* `kipõń+N+Sg+Abl:`
* *kibõnas* `kipõń+N+Sg+Tra:`
* *kibõnaniq* `kipõń+N+Sg+Ter:`
* *kibõnaldaq* `kipõń+N+Sg+Abe:`
* *kibõnagaq* `kipõń+N+Sg+Com:`
* *kibõnaq* `kipõń+N+Pl+Nom:`
* *kibõnit* `kipõń+N+Pl+Par:`
* *kibõnihe* `kipõń+N+Pl+Ill:`
* *kibõnist* `kipõń+N+Pl+Ela:`
* *kibõnilõ* `kipõń+N+Pl+All:`
* *kibõnil* `kipõń+N+Pl+Ade:`
* *kibõnilt* `kipõń+N+Pl+Abl:`
* *kibõnis* `kipõń+N+Pl+Tra:`
* *kibõniniq* `kipõń+N+Pl+Ter:`
* *kibõnildaq* `kipõń+N+Pl+Abe:`
* *kibõnidõgaq* `kipõń+N+Pl+Com:`

* Yaml: **N-kipwnj**

LEXICON NMN_9ALLWV1/XX  allõv́:ki%{pb%}õ%{nń%}

* Noun 09 allõv́ examples:*
* *allõv́* `allõv́+N+Sg+Nom:`
* *alõvit* `allõv́+N+Sg+Par:`
* *alõvihe* `allõv́+N+Sg+Ill:`
* *alõvist* `allõv́+N+Sg+Ela:`
* *alõvilõ* `allõv́+N+Sg+All:`
* *alõvil* `allõv́+N+Sg+Ade:`
* *alõvilt* `allõv́+N+Sg+Abl:`
* *alõvis* `allõv́+N+Sg+Tra:`
* *alõviniq* `allõv́+N+Sg+Ter:`
* *alõvildaq* `allõv́+N+Sg+Abe:`
* *alõvigaq* `allõv́+N+Sg+Com:`
* *alõviq* `allõv́+N+Pl+Nom:`
* *alõvõt* `allõv́+N+Pl+Par:`
* *alõvõhe* `allõv́+N+Pl+Ill:`
* *alõvõst* `allõv́+N+Pl+Ela:`
* *alõvõlõ* `allõv́+N+Pl+All:`
* *alõvõl* `allõv́+N+Pl+Ade:`
* *alõvõlt* `allõv́+N+Pl+Abl:`
* *alõvõs* `allõv́+N+Pl+Tra:`
* *alõvõniq* `allõv́+N+Pl+Ter:`
* *alõvõldaq* `allõv́+N+Pl+Abe:`
* *alõvõdõgaq* `allõv́+N+Pl+Com:`

* Yaml: **N-kipwnj**

LEXICON NMN_9ALLAS1/SINNEL1  allaś:allas
* Yaml: **N-kipwnj**

LEXICON NMN_9TUKWV/VERREV  tukõv:tu%{kg%}õv

* Adjective 09 tukõv examples:*
* *tukõv* `tukõv+A+Sg+Nom:`
* *tugõvat* `tukõv+A+Sg+Par:`
* *tugõvahe* `tukõv+A+Sg+Ill:`
* *tugõvast* `tukõv+A+Sg+Ela:`
* *tugõvale* `tukõv+A+Sg+All:`
* *tugõval* `tukõv+A+Sg+Ade:`
* *tugõvalt* `tukõv+A+Sg+Abl:`
* *tugõvas* `tukõv+A+Sg+Tra:`
* *tugõvaniq* `tukõv+A+Sg+Ter:`
* *tugõvaldaq* `tukõv+A+Sg+Abe:`
* *tugõvagaq* `tukõv+A+Sg+Com:`
* *tugõjaq* `tukõv+A+Pl+Nom:`
* *tugõjit* `tukõv+A+Pl+Par:`
* *tugõjihõ* `tukõv+A+Pl+Ill:`
* *tugõjist* `tukõv+A+Pl+Ela:`
* *tugõjilõ* `tukõv+A+Pl+All:`
* *tugõjil* `tukõv+A+Pl+Ade:`
* *tugõjilt* `tukõv+A+Pl+Abl:`
* *tugõjis* `tukõv+A+Pl+Tra:`
* *tugõjiniq* `tukõv+A+Pl+Ter:`
* *tugõjildaq* `tukõv+A+Pl+Abe:`
* *tugõjidegaq* `tukõv+A+Pl+Com:`

* Yaml: **N-tukwv**

LEXICON NMN_9SALLAI/ELLAEI  elläi:e%{lØ%}lä%{ij%}

* Noun 09 elläi examples:*
* *elläi* `elläi+N+Sg+Nom:`
* *eläjät* `elläi+N+Sg+Par:`
* *eläjähe* `elläi+N+Sg+Ill:`
* *eläjäst* `elläi+N+Sg+Ela:`
* *eläjäle* `elläi+N+Sg+All:`
* *eläjäl* `elläi+N+Sg+Ade:`
* *eläjält* `elläi+N+Sg+Abl:`
* *eläjäs* `elläi+N+Sg+Tra:`
* *eläjäniq* `elläi+N+Sg+Ter:`
* *eläjäldäq* `elläi+N+Sg+Abe:`
* *eläjägaq* `elläi+N+Sg+Com:`
* *eläjäq* `elläi+N+Pl+Nom:`
* *eläjit* `elläi+N+Pl+Par:`
* *eläjihe* `elläi+N+Pl+Ill:`
* *eläjist* `elläi+N+Pl+Ela:`
* *eläjile* `elläi+N+Pl+All:`
* *eläjil* `elläi+N+Pl+Ade:`
* *eläjilt* `elläi+N+Pl+Abl:`
* *eläjis* `elläi+N+Pl+Tra:`
* *eläjiniq* `elläi+N+Pl+Ter:`
* *eläjildäq* `elläi+N+Pl+Abe:`
* *eläjidegaq* `elläi+N+Pl+Com:`

* Yaml: **N-ellaei9**

SHOULD THIS BE HERE, c.f. yaml

LEXICON NMN_9TAHHE/HERRE  tahhe:ta%{hØ%}he

* Noun 09 tahhe examples:*
* *tahhe* `tahhe+N+Sg+Nom:`
* *tahehet* `tahhe+N+Sg+Par:`
* *tahehehe* `tahhe+N+Sg+Ill:`
* *tahehest* `tahhe+N+Sg+Ela:`
* *tahehelõ* `tahhe+N+Sg+All:`
* *tahehel* `tahhe+N+Sg+Ade:`
* *tahehelt* `tahhe+N+Sg+Abl:`
* *tahehes* `tahhe+N+Sg+Tra:`
* *taheheniq* `tahhe+N+Sg+Ter:`
* *taheheldaq* `tahhe+N+Sg+Abe:`
* *tahehegaq* `tahhe+N+Sg+Com:`
* *taheheq* `tahhe+N+Pl+Nom:`
* *tahehidõ* `tahhe+N+Pl+Gen:`
* *tahehit* `tahhe+N+Pl+Par:`
* *tahehihe* `tahhe+N+Pl+Ill:`
* *tahehist* `tahhe+N+Pl+Ela:`
* *tahehilõ* `tahhe+N+Pl+All:`
* *tahehil* `tahhe+N+Pl+Ade:`
* *tahehilt* `tahhe+N+Pl+Abl:`
* *tahehis* `tahhe+N+Pl+Tra:`
* *tahehiniq* `tahhe+N+Pl+Ter:`
* *tahehildaq* `tahhe+N+Pl+Abe:`
* *tahehidõgaq* `tahhe+N+Pl+Com:`
* Yaml: **N-kipwnj**

LEXICON NMN_9VILLW/XX  villõ:vi%{lØ%}lõ

* Noun 09 villõ examples:*
* *villõ* `villõ+N+Sg+Nom:`
* *vilõhõt* `villõ+N+Sg+Par:`
* *vilõhõhe* `villõ+N+Sg+Ill:`
* *vilõhõst* `villõ+N+Sg+Ela:`
* *vilõhõlõ* `villõ+N+Sg+All:`
* *vilõhõl* `villõ+N+Sg+Ade:`
* *vilõhõlt* `villõ+N+Sg+Abl:`
* *vilõhõs* `villõ+N+Sg+Tra:`
* *vilõhõniq* `villõ+N+Sg+Ter:`
* *vilõhõldaq* `villõ+N+Sg+Abe:`
* *vilõhõgaq* `villõ+N+Sg+Com:`
* *vilõhõq* `villõ+N+Pl+Nom:`
* *vilõhidõ* `villõ+N+Pl+Gen:`
* *vilõhit* `villõ+N+Pl+Par:`
* *vilõhihe* `villõ+N+Pl+Ill:`
* *vilõhist* `villõ+N+Pl+Ela:`
* *vilõhilõ* `villõ+N+Pl+All:`
* *vilõhil* `villõ+N+Pl+Ade:`
* *vilõhilt* `villõ+N+Pl+Abl:`
* *vilõhis* `villõ+N+Pl+Tra:`
* *vilõhiniq* `villõ+N+Pl+Ter:`
* *vilõhildaq* `villõ+N+Pl+Abe:`
* *vilõhidõgaq* `villõ+N+Pl+Com:`
* Yaml: **N-kipwnj**

* @OCDE@ hõrak:hõrak

* Noun 10 hõrak  examples:*
* *hõrak:* `hõrak+N+Sg+Nom`
* *hõraga:* `hõrak+N+Sg+Gen`
* *hõrakat:* `hõrak+N+Sg+Par`
* *hõrakahe:* `hõrak+N+Sg+Ill`
* *hõrakan:* `hõrak+N+Sg+Ine`
* *hõrakast:* `hõrak+N+Sg+Ela`
* *hõrakalõ:* `hõrak+N+Sg+All`
* *hõrakal:* `hõrak+N+Sg+Ade`
* *hõrakalt:* `hõrak+N+Sg+Abl`
* *hõrakas:* `hõrak+N+Sg+Tra`
* *hõrakaniq:* `hõrak+N+Sg+Ter`
* *hõrakaldaq:* `hõrak+N+Sg+Abe`
* *hõragagaq:* `hõrak+N+Sg+Com`
* *hõragaq:* `hõrak+N+Pl+Nom`
* *hõrakidõ:* `hõrak+N+Pl+Gen`
* *hõrakit:* `hõrak+N+Pl+Par`
* *hõrakihe:* `hõrak+N+Pl+Ill`
* *hõrakin:* `hõrak+N+Pl+Ine`
* *hõrakist:* `hõrak+N+Pl+Ela`
* *hõrakilõ:* `hõrak+N+Pl+All`
* *hõrakil:* `hõrak+N+Pl+Ade`
* *hõrakilt:* `hõrak+N+Pl+Abl`
* *hõrakis:* `hõrak+N+Pl+Tra`
* *hõrakiniq:* `hõrak+N+Pl+Ter`
* *hõrakildaq:* `hõrak+N+Pl+Abe`
* *hõrakidõgaq:* `hõrak+N+Pl+Com`
**N-hwrak10**

* Noun 10 ameeriga  examples:*
* *ameeriga:* `ameeriga+N+Sg+Nom`
* *ameeriga:* `ameeriga+N+Sg+Gen`
* *ameerikat:* `ameeriga+N+Sg+Par`
* *ameerikahe:* `ameeriga+N+Sg+Ill`
* *ameerikan:* `ameeriga+N+Sg+Ine`
* *ameerikast:* `ameeriga+N+Sg+Ela`
* *ameerikalõ:* `ameeriga+N+Sg+All`
* *ameerikal:* `ameeriga+N+Sg+Ade`
* *ameerikalt:* `ameeriga+N+Sg+Abl`
* *ameerikas:* `ameeriga+N+Sg+Tra`
* *ameerikaniq:* `ameeriga+N+Sg+Ter`
* *ameerikaldaq:* `ameeriga+N+Sg+Abe`
* *ameerigagaq:* `ameeriga+N+Sg+Com`
* *ameerigaq:* `ameeriga+N+Pl+Nom`
* *ameerikidõ:* `ameeriga+N+Pl+Gen`
* *ameerikit:* `ameeriga+N+Pl+Par`
* *ameerikihe:* `ameeriga+N+Pl+Ill`
* *ameerikin:* `ameeriga+N+Pl+Ine`
* *ameerikist:* `ameeriga+N+Pl+Ela`
* *ameerikilõ:* `ameeriga+N+Pl+All`
* *ameerikil:* `ameeriga+N+Pl+Ade`
* *ameerikilt:* `ameeriga+N+Pl+Abl`
* *ameerikis:* `ameeriga+N+Pl+Tra`
* *ameerikiniq:* `ameeriga+N+Pl+Ter`
* *ameerikildaq:* `ameeriga+N+Pl+Abe`
* *ameerikidõgaq:* `ameeriga+N+Pl+Com`

* @OCDE@ haidak:haida%{kg%}
Noun (10) esäk
* *esäk:* `esäk+N+Sg+Nom`
* *esägu:* `esäk+N+Sg+Gen`
* *esäkut:* `esäk+N+Sg+Par`
* *esäkuhe:* `esäk+N+Sg+Ill`
* *esäkun:* `esäk+N+Sg+Ine`
* *esäkust:* `esäk+N+Sg+Ela`
* *esäkulõ:* `esäk+N+Sg+All`
* *esäkul:* `esäk+N+Sg+Ade`
* *esäkult:* `esäk+N+Sg+Abl`
* *esäkus:* `esäk+N+Sg+Tra`
* *esäkuniq:* `esäk+N+Sg+Ter`
* *esäkuldaq:* `esäk+N+Sg+Abe`
* *esäkugaq:* `esäk+N+Sg+Com`
* *esäguq:* `esäk+N+Pl+Nom`
* *esäkide:* `esäk+N+Pl+Gen`
* *esäkit:* `esäk+N+Pl+Par`
* *esäkihe:* `esäk+N+Pl+Ill`
* *esäkin:* `esäk+N+Pl+Ine`
* *esäkist:* `esäk+N+Pl+Ela`
* *esäkile:* `esäk+N+Pl+All`
* *esäkil:* `esäk+N+Pl+Ade`
* *esäkilt:* `esäk+N+Pl+Abl`
* *esäkis:* `esäk+N+Pl+Tra`
* *esäkiniq:* `esäk+N+Pl+Ter`
* *esäkildäq:* `esäk+N+Pl+Abe`
* *esäkidegaq:* `esäk+N+Pl+Com`
**N-hwrak10**

* esäk examples:*
* *esäk:* `esäk+N+Sg+Nom`
* *esägu:* `esäk+N+Sg+Gen`
* *esäkut:* `esäk+N+Sg+Par`
* *esäkuhe:* `esäk+N+Sg+Ill`
* *esäkun:* `esäk+N+Sg+Ine`
* *esäkust:* `esäk+N+Sg+Ela`
* *esäkulõ:* `esäk+N+Sg+All`
* *esäkul:* `esäk+N+Sg+Ade`
* *esäkult:* `esäk+N+Sg+Abl`
* *esäkus:* `esäk+N+Sg+Tra`
* *esäkuniq:* `esäk+N+Sg+Ter`
* *esäkuldaq:* `esäk+N+Sg+Abe`
* *esäkugaq:* `esäk+N+Sg+Com`
* *esäguq:* `esäk+N+Pl+Nom`
* *esäkide:* `esäk+N+Pl+Gen`
* *esäkit:* `esäk+N+Pl+Par`
* *esäkihe:* `esäk+N+Pl+Ill`
* *esäkin:* `esäk+N+Pl+Ine`
* *esäkist:* `esäk+N+Pl+Ela`
* *esäkile:* `esäk+N+Pl+All`
* *esäkil:* `esäk+N+Pl+Ade`
* *esäkilt:* `esäk+N+Pl+Abl`
* *esäkis:* `esäk+N+Pl+Tra`
* *esäkiniq:* `esäk+N+Pl+Ter`
* *esäkildäq:* `esäk+N+Pl+Abe`
* *esäkidegaq:* `esäk+N+Pl+Com`

Noun (10) perit
* *perit:* `perit+N+Sg+Nom`
* *peridü:* `perit+N+Sg+Gen`
* *peritüt:* `perit+N+Sg+Par`
* *peritühe:* `perit+N+Sg+Ill`
* *peritün:* `perit+N+Sg+Ine`
* *peritüst:* `perit+N+Sg+Ela`
* *peritüle:* `perit+N+Sg+All`
* *peritül:* `perit+N+Sg+Ade`
* *peritült:* `perit+N+Sg+Abl`
* *peritüs:* `perit+N+Sg+Tra`
* *peritüniq:* `perit+N+Sg+Ter`
* *peritüldäq:* `perit+N+Sg+Abe`
* *peritügäq:* `perit+N+Sg+Com`
* *peridüq:* `perit+N+Pl+Nom`
* *peritide:* `perit+N+Pl+Gen`
* *peritit:* `perit+N+Pl+Par`
* *peritihe:* `perit+N+Pl+Ill`
* *peritin:* `perit+N+Pl+Ine`
* *peritist:* `perit+N+Pl+Ela`
* *peritile:* `perit+N+Pl+All`
* *peritil:* `perit+N+Pl+Ade`
* *peritilt:* `perit+N+Pl+Abl`
* *peritis:* `perit+N+Pl+Tra`
* *peritiniq:* `perit+N+Pl+Ter`
* *peritildäq:* `perit+N+Pl+Abe`
* *peritidegaq:* `perit+N+Pl+Com`
**N-hwrak10**

* Noun 10 vidrik  examples:*
* *vidriku:* `vidrik+N+Sg+Nom`
* *hõraku:* `vidrik+N+Sg+Gen`
* *vidrikut:* `vidrik+N+Sg+Par`
* *vidrikuhe:* `vidrik+N+Sg+Ill`
* *vidrikun:* `vidrik+N+Sg+Ine`
* *vidrikust:* `vidrik+N+Sg+Ela`
* *vidrikulõ:* `vidrik+N+Sg+All`
* *vidrikul:* `vidrik+N+Sg+Ade`
* *vidrikult:* `vidrik+N+Sg+Abl`
* *vidrikus:* `vidrik+N+Sg+Tra`
* *vidrikuniq:* `vidrik+N+Sg+Ter`
* *vidrikuldaq:* `vidrik+N+Sg+Abe`
* *hõrakugaq:* `vidrik+N+Sg+Com`
* *vidrikuq:* `vidrik+N+Pl+Nom`
* *vidrikidõ:* `vidrik+N+Pl+Gen`
* *vidrikit:* `vidrik+N+Pl+Par`
* *vidrikihe:* `vidrik+N+Pl+Ill`
* *vidrikin:* `vidrik+N+Pl+Ine`
* *vidrikist:* `vidrik+N+Pl+Ela`
* *vidrikilõ:* `vidrik+N+Pl+All`
* *vidrikil:* `vidrik+N+Pl+Ade`
* *vidrikilt:* `vidrik+N+Pl+Abl`
* *vidrikis:* `vidrik+N+Pl+Tra`
* *vidrikiniq:* `vidrik+N+Pl+Ter`
* *vidrikildaq:* `vidrik+N+Pl+Abe`
* *vidrikidõgaq:* `vidrik+N+Pl+Com`
vowel_harmony: BACK and FRONT
gradation: no
**N-vidrik10**

* @OCDE@ aabits:aabi%{td%}s

* Noun 10 aabits  examples:*
* *aabits:* `aabits+N+Sg+Nom`
* *aabidsa:* `aabits+N+Sg+Gen`
* *aabitsat:* `aabits+N+Sg+Par`
* *aabitsahe:* `aabits+N+Sg+Ill`
* *aabitsan:* `aabits+N+Sg+Ine`
* *aabitsast:* `aabits+N+Sg+Ela`
* *aabitsalõ:* `aabits+N+Sg+All`
* *aabitsal:* `aabits+N+Sg+Ade`
* *aabitsalt:* `aabits+N+Sg+Abl`
* *aabitsas:* `aabits+N+Sg+Tra`
* *aabitsaniq:* `aabits+N+Sg+Ter`
* *aabitsaldaq:* `aabits+N+Sg+Abe`
* *aabidsagaq:* `aabits+N+Sg+Com`
* *aabidsaq:* `aabits+N+Pl+Nom`
* *aabitsidõ:* `aabits+N+Pl+Gen`
* *aabitsit:* `aabits+N+Pl+Par`
* *aabitsihe:* `aabits+N+Pl+Ill`
* *aabitsin:* `aabits+N+Pl+Ine`
* *aabitsist:* `aabits+N+Pl+Ela`
* *aabitsilõ:* `aabits+N+Pl+All`
* *aabitsil:* `aabits+N+Pl+Ade`
* *aabitsilt:* `aabits+N+Pl+Abl`
* *aabitsis:* `aabits+N+Pl+Tra`
* *aabitsiniq:* `aabits+N+Pl+Ter`
* *aabitsildaq:* `aabits+N+Pl+Abe`
* *aabitsidõgaq:* `aabits+N+Pl+Com`
**N-hwrak10**

vowel_harmony: ONLY FRONT
**N-lembit10**

**N-hwrak10**

* Noun 10 aadrõś  examples:*
* *aadrõś:* `aadrõś+N+Sg+Nom`
* *aadrõsi:* `aadrõś+N+Sg+Gen`
* *aadrõssit:* `aadrõś+N+Sg+Par`
* *aadrõssihe:* `aadrõś+N+Sg+Ill`
* *aadrõsin:* `aadrõś+N+Sg+Ine`
* *aadrõsist:* `aadrõś+N+Sg+Ela`
* *aadrõsilõ:* `aadrõś+N+Sg+All`
* *aadrõsil:* `aadrõś+N+Sg+Ade`
* *aadrõsilt:* `aadrõś+N+Sg+Abl`
* *aadrõsis:* `aadrõś+N+Sg+Tra`
* *aadrõsiniq:* `aadrõś+N+Sg+Ter`
* *aadrõsildaq:* `aadrõś+N+Sg+Abe`
* *aadrõsigaq:* `aadrõś+N+Sg+Com`
* *aadrõsiq:* `aadrõś+N+Pl+Nom`
* *aadrõssidõ:* `aadrõś+N+Pl+Gen`
* *aadrõssit:* `aadrõś+N+Pl+Par`
* *aadrõssihe:* `aadrõś+N+Pl+Ill`
* *aadrõssin:* `aadrõś+N+Pl+Ine`
* *aadrõssist:* `aadrõś+N+Pl+Ela`
* *aadrõssilõ:* `aadrõś+N+Pl+All`
* *aadrõssil:* `aadrõś+N+Pl+Ade`
* *aadrõssilt:* `aadrõś+N+Pl+Abl`
* *aadrõssis:* `aadrõś+N+Pl+Tra`
* *aadrõssiniq:* `aadrõś+N+Pl+Ter`
* *aadrõssildaq:* `aadrõś+N+Pl+Abe`
* *aadrõssidõgaq:* `aadrõś+N+Pl+Com`

* @OCDE@ ammat́:amma%{tt́d%}

* Noun 10 ammat́ examples:*
* *ammat́:* `ammat́+N+Sg+Nom`
* *ammadi:* `ammat́+N+Sg+Gen`
* *ammatit:* `ammat́+N+Sg+Par`
* *ammatihe:* `ammat́+N+Sg+Ill`
* *ammadin:* `ammat́+N+Sg+Ine`
* *ammadist:* `ammat́+N+Sg+Ela`
* *ammadilõ:* `ammat́+N+Sg+All`
* *ammadil:* `ammat́+N+Sg+Ade`
* *ammadilt:* `ammat́+N+Sg+Abl`
* *ammadis:* `ammat́+N+Sg+Tra`
* *ammadiniq:* `ammat́+N+Sg+Ter`
* *ammadildaq:* `ammat́+N+Sg+Abe`
* *ammadigaq:* `ammat́+N+Sg+Com`
* *ammadiq:* `ammat́+N+Pl+Nom`
* *ammatidõ:* `ammat́+N+Pl+Gen`
* *ammatit:* `ammat́+N+Pl+Par`
* *ammatihe:* `ammat́+N+Pl+Ill`
* *ammatin:* `ammat́+N+Pl+Ine`
* *ammatist:* `ammat́+N+Pl+Ela`
* *ammatilõ:* `ammat́+N+Pl+All`
* *ammatil:* `ammat́+N+Pl+Ade`
* *ammatilt:* `ammat́+N+Pl+Abl`
* *ammatis:* `ammat́+N+Pl+Tra`
* *ammatiniq:* `ammat́+N+Pl+Ter`
* *ammatildaq:* `ammat́+N+Pl+Abe`
* *ammatidõgaq:* `ammat́+N+Pl+Com`
**N-hwrak10**

* @OCDE@ hüpätś:hüpäts
vowel_harmony: ONLY FRONT
Gradation: YES
**N-lembit10**

LEXICON NMN_11AINWQ/KELMEQ  ainõq:ainõ

* Noun 11 ainõq examples:*
* *ainõq* `ainõq+N+Sg+Nom:`
* *ainõt* `ainõq+N+Sg+Par:`
* *ainõhe* `ainõq+N+Sg+Ill:`
* *ainõst* `ainõq+N+Sg+Ela:`
* *ainõlõ* `ainõq+N+Sg+All:`
* *ainõl* `ainõq+N+Sg+Ade:`
* *ainõlt* `ainõq+N+Sg+Abl:`
* *ainõs* `ainõq+N+Sg+Tra:`
* *ainõniq* `ainõq+N+Sg+Ter:`
* *ainõldaq* `ainõq+N+Sg+Abe:`
* *ainõgaq* `ainõq+N+Sg+Com:`
* *ainõq* `ainõq+N+Pl+Nom:`
* *ainit* `ainõq+N+Pl+Par:`
* *ainihe* `ainõq+N+Pl+Ill:`
* *ainist* `ainõq+N+Pl+Ela:`
* *ainilõ* `ainõq+N+Pl+All:`
* *ainil* `ainõq+N+Pl+Ade:`
* *ainilt* `ainõq+N+Pl+Abl:`
* *ainis* `ainõq+N+Pl+Tra:`
* *aininiq* `ainõq+N+Pl+Ter:`
* *ainildaq* `ainõq+N+Pl+Abe:`
* *ainidõgaq* `ainõq+N+Pl+Com:`
**A-ainwq11**

**A-vaih11**

LEXICON NMN_11ANNWQ/LAETEQ  läteq:lä%{tØ%}te

* Noun 11 läteq examples:*
* *läteq* `läteq+N+Sg+Nom:`
* *lätet* `läteq+N+Sg+Par:`
* *lättehe* `läteq+N+Sg+Ill:`
* *lättest* `läteq+N+Sg+Ela:`
* *lättele* `läteq+N+Sg+All:`
* *lättel* `läteq+N+Sg+Ade:`
* *lättelt* `läteq+N+Sg+Abl:`
* *lättes* `läteq+N+Sg+Tra:`
* *lätteniq* `läteq+N+Sg+Ter:`
* *lätteldäq* `läteq+N+Sg+Abe:`
* *lättegaq* `läteq+N+Sg+Com:`
* *lätteq* `läteq+N+Pl+Nom:`
* *lättit* `läteq+N+Pl+Par:`
* *lättihe* `läteq+N+Pl+Ill:`
* *lättist* `läteq+N+Pl+Ela:`
* *lättile* `läteq+N+Pl+All:`
* *lättil* `läteq+N+Pl+Ade:`
* *lättilt* `läteq+N+Pl+Abl:`
* *lättis* `läteq+N+Pl+Tra:`
* *lättiniq* `läteq+N+Pl+Ter:`
* *lättildäq* `läteq+N+Pl+Abe:`
* *lättidegaq* `läteq+N+Pl+Com:`

**A-ainwq11**

* Noun 12 repäń examples:*
* *repäń* `repäń+N+Sg+Nom:`
* *rebäst* `repäń+N+Sg+Par:`
* *rebäsehe* `repäń+N+Sg+Ill:`
* *rebäsest* `repäń+N+Sg+Ela:`
* *rebäsele* `repäń+N+Sg+All:`
* *rebäsel* `repäń+N+Sg+Ade:`
* *rebäselt* `repäń+N+Sg+Abl:`
* *rebäses* `repäń+N+Sg+Tra:`
* *rebäseniq* `repäń+N+Sg+Ter:`
* *rebäseldäq* `repäń+N+Sg+Abe:`
* *rebäsegaq* `repäń+N+Sg+Com:`
* *rebäseq* `repäń+N+Pl+Nom:`
* *rebäsit* `repäń+N+Pl+Par:`
* *rebäsihe* `repäń+N+Pl+Ill:`
* *rebäsist* `repäń+N+Pl+Ela:`
* *rebäsile* `repäń+N+Pl+All:`
* *rebäsil* `repäń+N+Pl+Ade:`
* *rebäsilt* `repäń+N+Pl+Abl:`
* *rebäsis* `repäń+N+Pl+Tra:`
* *rebäsiniq* `repäń+N+Pl+Ter:`
* *rebäsildäq* `repäń+N+Pl+Abe:`
* *rebäsidegaq* `repäń+N+Pl+Com:`

**N-repaenj12**

**N-suekues12**

**N-suekues12**

* :%^Pen%^WGStem%^NoPAL%>sõ       Harm_Neutr_SG_ALL_lE-STEM        ;  THIS NEEDS WORK

LEXICON NMN_13ALONW/TAEHINE  alonõ:alo

* Noun 13 alonõ examples:*
* *alonõ* `alonõ+N+Sg+Nom:`
* *alost* `alonõ+N+Sg+Par:`
* *alotsõhe* `alonõ+N+Sg+Ill:`
* *alotsõl* `alonõ+N+Sg+Ade:`
* *alotsõlt* `alonõ+N+Sg+Abl:`
* *alotsõs* `alonõ+N+Sg+Tra:`
* *alotsõniq* `alonõ+N+Sg+Ter:`
* *alotsõldaq* `alonõ+N+Sg+Abe:`
* *alotsõgaq* `alonõ+N+Sg+Com:`
* *alodsõq* `alonõ+N+Pl+Nom:`
* *alotsit* `alonõ+N+Pl+Par:`
* *alotsihe* `alonõ+N+Pl+Ill:`
* *alotsist* `alonõ+N+Pl+Ela:`
* *alotsilõ* `alonõ+N+Pl+All:`
* *alotsil* `alonõ+N+Pl+Ade:`
* *alotsilt* `alonõ+N+Pl+Abl:`
* *alotsis* `alonõ+N+Pl+Tra:`
* *alotsiniq* `alonõ+N+Pl+Ter:`
* *alotsildaq* `alonõ+N+Pl+Abe:`
* *alotsidõgaq* `alonõ+N+Pl+Com:`

**A-alonw**

LEXICON NMN_13VAHTSWNW  vahtsõnõ:vah

* Noun 13 alonõ examples:*
* *alonõ* `alonõ+N+Sg+Nom:`
* *alost* `alonõ+N+Sg+Par:`
* *alotsõhe* `alonõ+N+Sg+Ill:`
* *alotsõl* `alonõ+N+Sg+Ade:`
* *alotsõlt* `alonõ+N+Sg+Abl:`
* *alotsõs* `alonõ+N+Sg+Tra:`
* *alotsõniq* `alonõ+N+Sg+Ter:`
* *alotsõldaq* `alonõ+N+Sg+Abe:`
* *alotsõgaq* `alonõ+N+Sg+Com:`
* *alodsõq* `alonõ+N+Pl+Nom:`
* *alotsit* `alonõ+N+Pl+Par:`
* *alotsihe* `alonõ+N+Pl+Ill:`
* *alotsist* `alonõ+N+Pl+Ela:`
* *alotsilõ* `alonõ+N+Pl+All:`
* *alotsil* `alonõ+N+Pl+Ade:`
* *alotsilt* `alonõ+N+Pl+Abl:`
* *alotsis* `alonõ+N+Pl+Tra:`
* *alotsiniq* `alonõ+N+Pl+Ter:`
* *alotsildaq* `alonõ+N+Pl+Abe:`
* *alotsidõgaq* `alonõ+N+Pl+Com:`

**A-vahtswnw**

LEXICON NMN_13XX/SAEAENE  sääne:sää
**A-alonw**

* **LEXICON NMN_14RITS1KAS/HERNEH ** ritśkas:ritśka

* Noun 14 ritśkas examples:*
* *ritśkas* `ritśkas+N+Sg+Nom:`
* *ritśka* `ritśkas+N+Sg+Gen:`
* *ritśkast* `ritśkas+N+Sg+Par:`
* *ritśkahe* `ritśkas+N+Sg+Ill:`
* *ritśkast* `ritśkas+N+Sg+Ela:`
* *ritśkalõ* `ritśkas+N+Sg+All:`
* *ritśkal* `ritśkas+N+Sg+Ade:`
* *ritśkalt* `ritśkas+N+Sg+Abl:`
* *ritśkas* `ritśkas+N+Sg+Tra:`
* *ritśkaniq* `ritśkas+N+Sg+Ter:`
* *ritśkaldaq* `ritśkas+N+Sg+Abe:`
* *ritśkagaq* `ritśkas+N+Sg+Com:`
* *ritśkaq* `ritśkas+N+Pl+Nom:`
* *ritśkit* `ritśkas+N+Pl+Par:`
* *ritśkihe* `ritśkas+N+Pl+Ill:`
* *ritśkist* `ritśkas+N+Pl+Ela:`
* *ritśkilõ* `ritśkas+N+Pl+All:`
* *ritśkil* `ritśkas+N+Pl+Ade:`
* *ritśkilt* `ritśkas+N+Pl+Abl:`
* *ritśkis* `ritśkas+N+Pl+Tra:`
* *ritśkiniq* `ritśkas+N+Pl+Ter:`
* *ritśkildaq* `ritśkas+N+Pl+Abe:`
* *ritśkidõgaq* `ritśkas+N+Pl+Com:`

* **LEXICON NMN_14HAMMAS/IKAES ** hammas:ham%{bm%}a%{sØ%}

* Noun 14 hammas examples:*
* *hammas* `hammas+N+Sg+Nom:`
* *hammast* `hammas+N+Sg+Par:`
* *hambahe* `hammas+N+Sg+Ill:`
* *hambast* `hammas+N+Sg+Ela:`
* *hambalõ* `hammas+N+Sg+All:`
* *hambal* `hammas+N+Sg+Ade:`
* *hambalt* `hammas+N+Sg+Abl:`
* *hambas* `hammas+N+Sg+Tra:`
* *hambaniq* `hammas+N+Sg+Ter:`
* *hambaldaq* `hammas+N+Sg+Abe:`
* *hambagaq* `hammas+N+Sg+Com:`
* *hambaq* `hammas+N+Pl+Nom:`
* *hambit* `hammas+N+Pl+Par:`
* *hambihe* `hammas+N+Pl+Ill:`
* *hambist* `hammas+N+Pl+Ela:`
* *hambilõ* `hammas+N+Pl+All:`
* *hambil* `hammas+N+Pl+Ade:`
* *hambilt* `hammas+N+Pl+Abl:`
* *hambis* `hammas+N+Pl+Tra:`
* *hambiniq* `hammas+N+Pl+Ter:`
* *hambildaq* `hammas+N+Pl+Abe:`
* *hambidõgaq* `hammas+N+Pl+Com:`

Distinguished from 14RITS1KAS due to gradation
Yaml: __N-hammas_gt-norm.yaml__

* Noun 14 nummõŕ examples:*
* *nummõŕ* `nummõŕ+N+Sg+Nom:`
* *nummõrd* `nummõŕ+N+Sg+Par:`
* *numbrõhe* `nummõŕ+N+Sg+Ill:`
* *numbrõst* `nummõŕ+N+Sg+Ela:`
* *numbrõlõ* `nummõŕ+N+Sg+All:`
* *numbrõl* `nummõŕ+N+Sg+Ade:`
* *numbrõlt* `nummõŕ+N+Sg+Abl:`
* *numbrõs* `nummõŕ+N+Sg+Tra:`
* *numbrõniq* `nummõŕ+N+Sg+Ter:`
* *numbrõldaq* `nummõŕ+N+Sg+Abe:`
* *numbrõgaq* `nummõŕ+N+Sg+Com:`
* *numbrõq* `nummõŕ+N+Pl+Nom:`
* *numbrit* `nummõŕ+N+Pl+Par:`
* *numbrihe* `nummõŕ+N+Pl+Ill:`
* *numbrist* `nummõŕ+N+Pl+Ela:`
* *numbrilõ* `nummõŕ+N+Pl+All:`
* *numbril* `nummõŕ+N+Pl+Ade:`
* *numbrilt* `nummõŕ+N+Pl+Abl:`
* *numbris* `nummõŕ+N+Pl+Tra:`
* *numbriniq* `nummõŕ+N+Pl+Ter:`
* *numbrildaq* `nummõŕ+N+Pl+Abe:`
* *numbridõgaq* `nummõŕ+N+Pl+Com:`
Distinguished from 14RITS1KAS due to gradation
Yaml: __N-nummõŕ_gt-norm.yaml__

Distinguished from 14RITS1KAS due  to word final h
vowel_harmony_variant: hamõh
Yaml: __N-pereh_gt-norm.yaml__

* Noun 14 hamõh examples:*
* *hamõh* `hamõh+N+Sg+Nom:`
* *hamõht* `hamõh+N+Sg+Par:`
* *hammõhe* `hamõh+N+Sg+Ill:`
* *hammõst* `hamõh+N+Sg+Ela:`
* *hammõlõ* `hamõh+N+Sg+All:`
* *hammõl* `hamõh+N+Sg+Ade:`
* *hammõlt* `hamõh+N+Sg+Abl:`
* *hammõs* `hamõh+N+Sg+Tra:`
* *hammõniq* `hamõh+N+Sg+Ter:`
* *hammõldaq* `hamõh+N+Sg+Abe:`
* *hammõgaq* `hamõh+N+Sg+Com:`
* *hammõq* `hamõh+N+Pl+Nom:`
* *hammit* `hamõh+N+Pl+Par:`
* *hammihe* `hamõh+N+Pl+Ill:`
* *hammist* `hamõh+N+Pl+Ela:`
* *hammilõ* `hamõh+N+Pl+All:`
* *hammil* `hamõh+N+Pl+Ade:`
* *hammilt* `hamõh+N+Pl+Abl:`
* *hammis* `hamõh+N+Pl+Tra:`
* *hamminiq* `hamõh+N+Pl+Ter:`
* *hammildaq* `hamõh+N+Pl+Abe:`
* *hammidõgaq* `hamõh+N+Pl+Com:`
Distinguished from 14RITS1KAS due  to word final h
vowel_harmony_variant: pereh
Yaml: __N-hamwh_gt-norm.yaml__

* Noun 15 kotus examples:*
* *kotus* `kotus+Hom1+N+Sg+Nom:`
* *kotust* `kotus+Hom1+N+Sg+Par:`
* *kotussõhe* `kotus+Hom1+N+Sg+Ill:`
* *kotussõst* `kotus+Hom1+N+Sg+Ela:`
* *kotussõlõ* `kotus+Hom1+N+Sg+All:`
* *kotussõl* `kotus+Hom1+N+Sg+Ade:`
* *kotussõlt* `kotus+Hom1+N+Sg+Abl:`
* *kotussõs* `kotus+Hom1+N+Sg+Tra:`
* *kotussõniq* `kotus+Hom1+N+Sg+Ter:`
* *kotussõldaq* `kotus+Hom1+N+Sg+Abe:`
* *kotusõgaq* `kotus+Hom1+N+Sg+Com:`
* *kotusõq* `kotus+Hom1+N+Pl+Nom:`
* *kotussit* `kotus+Hom1+N+Pl+Par:`
* *kotussihe* `kotus+Hom1+N+Pl+Ill:`
* *kotussist* `kotus+Hom1+N+Pl+Ela:`
* *kotussilõ* `kotus+Hom1+N+Pl+All:`
* *kotussil* `kotus+Hom1+N+Pl+Ade:`
* *kotussilt* `kotus+Hom1+N+Pl+Abl:`
* *kotussis* `kotus+Hom1+N+Pl+Tra:`
* *kotussiniq* `kotus+Hom1+N+Pl+Ter:`
* *kotussildaq* `kotus+Hom1+N+Pl+Abe:`
* *kotussidõgaq* `kotus+Hom1+N+Pl+Com:`

* Noun 15 kotus examples:*
* *kotus* `kotus+Hom1+N+Sg+Nom:`
* *kotust* `kotus+Hom1+N+Sg+Par:`
* *kotussõhe* `kotus+Hom1+N+Sg+Ill:`
* *kotussõst* `kotus+Hom1+N+Sg+Ela:`
* *kotussõlõ* `kotus+Hom1+N+Sg+All:`
* *kotussõl* `kotus+Hom1+N+Sg+Ade:`
* *kotussõlt* `kotus+Hom1+N+Sg+Abl:`
* *kotussõs* `kotus+Hom1+N+Sg+Tra:`
* *kotussõniq* `kotus+Hom1+N+Sg+Ter:`
* *kotussõldaq* `kotus+Hom1+N+Sg+Abe:`
* *kotusõgaq* `kotus+Hom1+N+Sg+Com:`
* *kotusõq* `kotus+Hom1+N+Pl+Nom:`
* *kotussit* `kotus+Hom1+N+Pl+Par:`
* *kotussihe* `kotus+Hom1+N+Pl+Ill:`
* *kotussist* `kotus+Hom1+N+Pl+Ela:`
* *kotussilõ* `kotus+Hom1+N+Pl+All:`
* *kotussil* `kotus+Hom1+N+Pl+Ade:`
* *kotussilt* `kotus+Hom1+N+Pl+Abl:`
* *kotussis* `kotus+Hom1+N+Pl+Tra:`
* *kotussiniq* `kotus+Hom1+N+Pl+Ter:`
* *kotussildaq* `kotus+Hom1+N+Pl+Abe:`
* *kotussidõgaq* `kotus+Hom1+N+Pl+Com:`

LEXICON NMN_16ABILINW/INEMINE  inemine:inemi abilinõ:abili
* Yaml: **N-inemine16**

LEXICON NMN_16TSIRGUKWNW/TERAEKENE  inemine:inemi tsirgukõnõ:abili
* Yaml: **N-inemine16**

* LEXICON NMN_17ALGUS/UETSUES  aivastus:aivastus
* Yaml: **N-aivastus18**

LEXICON NMN_19ALOMANW/PEDAEJAENE   alomanõ:aloma
* Yaml: **A-alomanw19**

* Yaml: **N-latsj20**

* Yaml: **N-vaeitsj20**

* Yaml: **N-vaeitsj20**

* Yaml: **N-vaeitsj20**

* Yaml: **N-vaeitsj20**

LEXICON NMN_22NAANW  naanõ:naa
* Yaml: **N-vwrokwnw22**

LEXICON NMN_22VWROKWNW/VAEHAEKENE  vähäkene:vähäke
* Yaml: **N-vaehaekene22**

* **LEXICON NMN_23NUUL1/KIIL1 ** nuuĺ:nool
* Yaml: **N-nuulj**

* **LEXICON NMN_23SUUR1 ** suuŕ:suur
* Yaml: **N-suurj**

* Yaml: **N-kiilj23**

* Yaml: **N-hiirj23**

* Yaml: **N-susi24**

* Yaml: **N-susi24**

* Yaml: **N-sueaeq25**

* Yaml: **N-hepemj26**

* **LEXICON NMN_27HAPU ** hapu:hapu
Yaml: **N-hapu27**

* **LEXICON NMN_27XX/LAEMMI ** lämmi:lämmi
Yaml: **N-hapu27**

* **LEXICON NMN_27KUEMMEND ** kümmend:küm

* **LEXICON NMN_28TUETAER1 ** tütäŕ:tütär
* Yaml: **N-tuetaerj28, N-kannwl28**

* **LEXICON NMN_28AHER/XX ** aher:ah%{tØ%}er
* Yaml: **N-tuetaerj28**

* Yaml: **N-pindaer28**

* Yaml: **N-tuetaerj28, N-kannwl28**

* Yaml: **N-kannwl28**
gradation= yes

* Yaml: **N-kannwl28**
gradation= no

* Yaml: **N-pundar28**

* Yaml: **N-pää29**

* LEXICON NMN_30MAA/TUEUE  tüü:tüü
* Yaml: **N-tueue30**

* Noun 33 igä examples:*
* *igä:* `igä+N+Sg+Nom`
* *iä:* `igä+N+Sg+Gen`
* *ikä:* `igä+N+Sg+Par`
* *ikkä:* `igä+N+Sg+Ill`
* *iän:* `igä+N+Sg+Ine`
* *iäst:* `igä+N+Sg+Ela`
* *iäle:* `igä+N+Sg+All`
* *iäl:* `igä+N+Sg+Ade`
* *iält:* `igä+N+Sg+Abl`
* *iäs:* `igä+N+Sg+Tra`
* *iäniq:* `igä+N+Sg+Ter`
* *iäldäq:* `igä+N+Sg+Abe`
* *iägaq:* `igä+N+Sg+Com`
* *iäq:* `igä+N+Pl+Nom`
* *iki:* `igä+N+Pl+Gen`
* *iki:* `igä+N+Pl+Par`
* *ikkihe:* `igä+N+Pl+Ill`
* *ikin:* `igä+N+Pl+Ine`
* *ikist:* `igä+N+Pl+Ela`
* *ikile:* `igä+N+Pl+All`
* *ikil:* `igä+N+Pl+Ade`
* *ikilt:* `igä+N+Pl+Abl`
* *ikis:* `igä+N+Pl+Tra`
* *ikiniq:* `igä+N+Pl+Ter`
* *ikildäq:* `igä+N+Pl+Abe`
* *ikigaq:* `igä+N+Pl+Com`

* LEXICON NMN_35EGAE  egä:e%{kØ%}%{kg%}ä

* LEXICON NMN_35UMA/PESAE  pesä:pe%{sØ%}sä

nimi:nim
* Yaml: **N-nimi**

* nimi examples:*
* *nimi:* `nimi+N+Sg+Nom`
* *nime:* `nimi+N+Sg+Gen`
* *nimme:* `nimi+N+Sg+Par`
* *nimme:* `nimi+N+Sg+Ill`
* *nimen:* `nimi+N+Sg+Ine`
* *nimest:* `nimi+N+Sg+Ela`
* *nimele:* `nimi+N+Sg+All`
* *nimel:* `nimi+N+Sg+Ade`
* *nimelt:* `nimi+N+Sg+Abl`
* *nimes:* `nimi+N+Sg+Tra`
* *nimeniq:* `nimi+N+Sg+Ter`
* *nimeldäq:* `nimi+N+Sg+Abe`
* *nimegaq:* `nimi+N+Sg+Com`
* *nimeq:* `nimi+N+Pl+Nom`
* *nimmi:* `nimi+N+Pl+Gen`
* *nimmi:* `nimi+N+Pl+Par`
* *nimmihe:* `nimi+N+Pl+Ill`
* *nimin:* `nimi+N+Pl+Ine`
* *nimist:* `nimi+N+Pl+Ela`
* *nimile:* `nimi+N+Pl+All`
* *nimil:* `nimi+N+Pl+Ade`
* *nimilt:* `nimi+N+Pl+Abl`
* *nimis:* `nimi+N+Pl+Tra`
* *niminiq:* `nimi+N+Pl+Ter`
* *nimildäq:* `nimi+N+Pl+Abe`
* *nimmigaq:* `nimi+N+Pl+Com`

* +Err/Orth-no-pal:%^StrGStem%^NoPAL        Harm_Neutr_SG_NOM  ;  no palatal

* särǵ examples:*
* *särǵ:* `särǵ+N+Sg+Nom`
* *säre:* `särǵ+N+Sg+Gen`
* *särge:* `särǵ+N+Sg+Par`
* *särge:* `särǵ+N+Sg+Ill`
* *sären:* `särǵ+N+Sg+Ine`
* *särest:* `särǵ+N+Sg+Ela`
* *särele:* `särǵ+N+Sg+All`
* *särel:* `särǵ+N+Sg+Ade`
* *särelt:* `särǵ+N+Sg+Abl`
* *säres:* `särǵ+N+Sg+Tra`
* *säreniq:* `särǵ+N+Sg+Ter`
* *säreldäq:* `särǵ+N+Sg+Abe`
* *säregaq:* `särǵ+N+Sg+Com`
* *säreq:* `särǵ+N+Pl+Nom`
* *särgi:* `särǵ+N+Pl+Gen`
* *särgi:* `särǵ+N+Pl+Par`
* *särgihe:* `särǵ+N+Pl+Ill`
* *särin:* `särǵ+N+Pl+Ine`
* *särist:* `särǵ+N+Pl+Ela`
* *särile:* `särǵ+N+Pl+All`
* *säril:* `särǵ+N+Pl+Ade`
* *särilt:* `särǵ+N+Pl+Abl`
* *säris:* `särǵ+N+Pl+Tra`
* *säriniq:* `särǵ+N+Pl+Ter`
* *särildäq:* `särǵ+N+Pl+Abe`
* *särgigaq:* `särǵ+N+Pl+Com`

* LEXICON NMN_36KWIK1/XX1   kõiḱ:kõi%{kØ%}%{kḱg%}

**LEXICON NMN_46SWBWR **
sõbõr:sõbõr
Oblique plural in o
* Yaml: **N-swbwr36**
derived from 36SAERG1

kubõl:ku%{pb%}õl
Oblique plural in õ
* Yaml: **N-swbwr36**
derived from 36SAERG1

pini:pi%{nØ%}ni

* Noun 37 pini examples:*
* *pini* `pini+N+Sg+Nom:`
* *pini* `pini+N+Sg+Gen:`
* *pinni* `pini+N+Sg+Par:`
* *pinni* `pini+N+Sg+Ill:`
* *pinist* `pini+N+Sg+Ela:`
* *pinile* `pini+N+Sg+All:`
* *pinil* `pini+N+Sg+Ade:`
* *pinilt* `pini+N+Sg+Abl:`
* *pinis* `pini+N+Sg+Tra:`
* *pininiq* `pini+N+Sg+Ter:`
* *pinildäq* `pini+N+Sg+Abe:`
* *pinigaq* `pini+N+Sg+Com:`
* *piniq* `pini+N+Pl+Nom:`
* *pinne* `pini+N+Pl+Par:`
* *pinnehe* `pini+N+Pl+Ill:`
* *pinest* `pini+N+Pl+Ela:`
* *pinele* `pini+N+Pl+All:`
* *pinel* `pini+N+Pl+Ade:`
* *pinelt* `pini+N+Pl+Abl:`
* *pines* `pini+N+Pl+Tra:`
* *pineniq* `pini+N+Pl+Ter:`
* *pineldäq* `pini+N+Pl+Abe:`
* *pinnegaq* `pini+N+Pl+Com:`

pini:pi%{nØ%}ni

pung:pung

* Noun 38 pung examples:*

* LEXICON NMN_38PULL1/VIKS1  pulĺ:pull
* +Err/Orth-no-pal:%^StrGStem%^NoPAL%>        Harm_Neutr_SG_NOM  ;  no final palatal

* +Err/Orth-no-pal:%^StrGStem%^NoPAL%>        Harm_Neutr_SG_NOM  ;  no final palatal

* papṕ examples:*
* *papṕ:* `papṕ+N+Sg+Nom`
* *papi:* `papṕ+N+Sg+Gen`
* *pappi:* `papṕ+N+Sg+Par`
* *pappi:* `papṕ+N+Sg+Ill`
* *papin:* `papṕ+N+Sg+Ine`
* *papist:* `papṕ+N+Sg+Ela`
* *papilõ:* `papṕ+N+Sg+All`
* *papil:* `papṕ+N+Sg+Ade`
* *papilt:* `papṕ+N+Sg+Abl`
* *papis:* `papṕ+N+Sg+Tra`
* *papiniq:* `papṕ+N+Sg+Ter`
* *papildaq:* `papṕ+N+Sg+Abe`
* *papigaq:* `papṕ+N+Sg+Com`
* *papiq:* `papṕ+N+Pl+Nom`
* *pappõ:* `papṕ+N+Pl+Gen`
* *pappõ:* `papṕ+N+Pl+Par`
* *pappõhe:* `papṕ+N+Pl+Ill`
* *papõn:* `papṕ+N+Pl+Ine`
* *papõst:* `papṕ+N+Pl+Ela`
* *papõlõ:* `papṕ+N+Pl+All`
* *papõl:* `papṕ+N+Pl+Ade`
* *papõlt:* `papṕ+N+Pl+Abl`
* *papõs:* `papṕ+N+Pl+Tra`
* *papõniq:* `papṕ+N+Pl+Ter`
* *papõldaq:* `papṕ+N+Pl+Abe`
* *pappegaq:* `papṕ+N+Pl+Com`

   * :%^VOWRaise%^StrGStem%^PAL        Harm_Neutr_SG_NOM  ;  pu̬u̬ḿ
* +Err/Orth-no-pal:%^VOWRaise%^StrGStem%^NoPAL        Harm_Neutr_SG_NOM  ;  no final palatal
   * :%^VOWLower%^WGStem%^NoPAL%>i       SG_GEN_ZERO-STEM        ;  poomi

kuld:kul%{dl%}

* Noun 38 kuld examples:*
* *kuld* `kuld+N+Sg+Nom:`
* *kulla* `kuld+N+Sg+Gen:`
* *kulda* `kuld+N+Sg+Par:`
* *kulda* `kuld+N+Sg+Ill:`
* *kullast* `kuld+N+Sg+Ela:`
* *kullalõ* `kuld+N+Sg+All:`
* *kullal* `kuld+N+Sg+Ade:`
* *kullalt* `kuld+N+Sg+Abl:`
* *kullas* `kuld+N+Sg+Tra:`
* *kullaniq* `kuld+N+Sg+Ter:`
* *kullaldaq* `kuld+N+Sg+Abe:`
* *kullagaq* `kuld+N+Sg+Com:`
* *kullaq* `kuld+N+Pl+Nom:`
* *kuldõ* `kuld+N+Pl+Par:`
* *kuldõhe* `kuld+N+Pl+Ill:`
* *kullõst* `kuld+N+Pl+Ela:`
* *kullõlõ* `kuld+N+Pl+All:`
* *kullõl* `kuld+N+Pl+Ade:`
* *kullõlt* `kuld+N+Pl+Abl:`
* *kullõs* `kuld+N+Pl+Tra:`
* *kullõniq* `kuld+N+Pl+Ter:`
* *kullõldaq* `kuld+N+Pl+Abe:`
* *kuldõgaq* `kuld+N+Pl+Com:`

kuld:kul%{dl%}

* Noun 38 kuld examples:*
* *kuld* `kuld+N+Sg+Nom:`
* *kulla* `kuld+N+Sg+Gen:`
* *kulda* `kuld+N+Sg+Par:`
* *kulda* `kuld+N+Sg+Ill:`
* *kullast* `kuld+N+Sg+Ela:`
* *kullalõ* `kuld+N+Sg+All:`
* *kullal* `kuld+N+Sg+Ade:`
* *kullalt* `kuld+N+Sg+Abl:`
* *kullas* `kuld+N+Sg+Tra:`
* *kullaniq* `kuld+N+Sg+Ter:`
* *kullaldaq* `kuld+N+Sg+Abe:`
* *kullagaq* `kuld+N+Sg+Com:`
* *kullaq* `kuld+N+Pl+Nom:`
* *kuldõ* `kuld+N+Pl+Par:`
* *kuldõhe* `kuld+N+Pl+Ill:`
* *kullõst* `kuld+N+Pl+Ela:`
* *kullõlõ* `kuld+N+Pl+All:`
* *kullõl* `kuld+N+Pl+Ade:`
* *kullõlt* `kuld+N+Pl+Abl:`
* *kullõs* `kuld+N+Pl+Tra:`
* *kullõniq* `kuld+N+Pl+Ter:`
* *kullõldaq* `kuld+N+Pl+Abe:`
* *kuldõgaq* `kuld+N+Pl+Com:`

Derived from PUHM, Gradation="yes", stem="+Sg+Nom"
stem_vowel="o"

* +Err/Orth-no-pal:%^StrGStem%^NoPAL        Harm_Neutr_SG_NOM  ;  no final palatal

* juht́ examples:*
* *juht́:* `juht́+N+Sg+Nom`
* *juhi:* `juht́+N+Sg+Gen`
* *juhtõ:* `juht́+N+Sg+Par`
* *juhtõ:* `juht́+N+Sg+Ill`
* *juhin:* `juht́+N+Sg+Ine`
* *juhist:* `juht́+N+Sg+Ela`
* *juhilõ:* `juht́+N+Sg+All`
* *juhil:* `juht́+N+Sg+Ade`
* *juhilt:* `juht́+N+Sg+Abl`
* *juhis:* `juht́+N+Sg+Tra`
* *juhiniq:* `juht́+N+Sg+Ter`
* *juhildaq:* `juht́+N+Sg+Abe`
* *juhigaq:* `juht́+N+Sg+Com`
* *juhiq:* `juht́+N+Pl+Nom`
* *juhõ:* `juht́+N+Pl+Gen`
* *juhtõ:* `juht́+N+Pl+Par`
* *juhtõhõ:* `juht́+N+Pl+Ill`
* *juhõn:* `juht́+N+Pl+Ine`
* *juhõst:* `juht́+N+Pl+Ela`
* *juhõlõ:* `juht́+N+Pl+All`
* *juhõl:* `juht́+N+Pl+Ade`
* *juhõlt:* `juht́+N+Pl+Abl`
* *juhõs:* `juht́+N+Pl+Tra`
* *juhõniq:* `juht́+N+Pl+Ter`
* *juhõldaq:* `juht́+N+Pl+Abe`
* *juhõgaq:* `juht́+N+Pl+Com`

* :%^Pen%^PAL%^Pen%^JI20       SG_GEN_ZERO-STEM        ;  vaŕo
* +Err/Orth-no-pal:%^Pen%^NoPAL%^Pen%^JI20       SG_GEN_ZERO-STEM        ;  vaŕo

* :%^Pen%^NoPAL%^Pen%^JI2J%^VowRM%>õ    PL_GEN_ZERO ;  varjõ

* LEXICON NMN_42TUEHI  tühi:tüh

* :ä       SG_GEN_ZERO-STEM        ;  vaŕo

* :e    PL_GEN_ZERO ;  varjõ

* kanarik # examples:*
* *kanarik:* `kanarik+N+Sg+Nom`
* *kanarigu:* `kanarik+N+Sg+Gen`
* *kanarikku:* `kanarik+N+Sg+Par`
* *kanarikku:* `kanarik+N+Sg+Ill`
* *kanarigun:* `kanarik+N+Sg+Ine`
* *kanarigust:* `kanarik+N+Sg+Ela`
* *kanarigulõ:* `kanarik+N+Sg+All`
* *kanarigul:* `kanarik+N+Sg+Ade`
* *kanarigult:* `kanarik+N+Sg+Abl`
* *kanarigus:* `kanarik+N+Sg+Tra`
* *kanariguniq:* `kanarik+N+Sg+Ter`
* *kanariguldaq:* `kanarik+N+Sg+Abe`
* *kanarigugaq:* `kanarik+N+Sg+Com`
* *kanariguq:* `kanarik+N+Pl+Nom`
* *kanarikkõ:* `kanarik+N+Pl+Gen`
* *kanarikkõ:* `kanarik+N+Pl+Par`
* *kanarikkõhe:* `kanarik+N+Pl+Ill`
* *kanarigõn:* `kanarik+N+Pl+Ine`
* *kanarigõst:* `kanarik+N+Pl+Ela`
* *kanarigõlõ:* `kanarik+N+Pl+All`
* *kanarigõl:* `kanarik+N+Pl+Ade`
* *kanarigõlt:* `kanarik+N+Pl+Abl`
* *kanarigõs:* `kanarik+N+Pl+Tra`
* *kanarigõniq:* `kanarik+N+Pl+Ter`
* *kanarigõldaq:* `kanarik+N+Pl+Abe`
* *kanarigõgaq:* `kanarik+N+Pl+Com`

* saslõḱ # examples:*
* *saslõḱ:* `saslõḱ+N+Sg+Nom`
* *saslõgi:* `saslõḱ+N+Sg+Gen`
* *saslõkki:* `saslõḱ+N+Sg+Par`
* *saslõkki:* `saslõḱ+N+Sg+Ill`
* *saslõgin:* `saslõḱ+N+Sg+Ine`
* *saslõgist:* `saslõḱ+N+Sg+Ela`
* *saslõgilõ:* `saslõḱ+N+Sg+All`
* *saslõgil:* `saslõḱ+N+Sg+Ade`
* *saslõgilt:* `saslõḱ+N+Sg+Abl`
* *saslõgis:* `saslõḱ+N+Sg+Tra`
* *saslõginiq:* `saslõḱ+N+Sg+Ter`
* *saslõgildaq:* `saslõḱ+N+Sg+Abe`
* *saslõgigaq:* `saslõḱ+N+Sg+Com`
* *saslõgiq:* `saslõḱ+N+Pl+Nom`
* *saslõkke:* `saslõḱ+N+Pl+Gen`
* *saslõkke:* `saslõḱ+N+Pl+Par`
* *saslõkkehe:* `saslõḱ+N+Pl+Ill`
* *saslõgen:* `saslõḱ+N+Pl+Ine`
* *saslõgest:* `saslõḱ+N+Pl+Ela`
* *saslõgelõ:* `saslõḱ+N+Pl+All`
* *saslõgel:* `saslõḱ+N+Pl+Ade`
* *saslõgelt:* `saslõḱ+N+Pl+Abl`
* *saslõges:* `saslõḱ+N+Pl+Tra`
* *saslõgeniq:* `saslõḱ+N+Pl+Ter`
* *saslõgeldaq:* `saslõḱ+N+Pl+Abe`
* *saslõgegaq:* `saslõḱ+N+Pl+Com`

* apriĺ # examples:*
* *apriĺ:* `apriĺ+N+Sg+Nom`
* *aprili:* `apriĺ+N+Sg+Gen`
* *aprilli:* `apriĺ+N+Sg+Par`
* *aprilli:* `apriĺ+N+Sg+Ill`
* *aprilin:* `apriĺ+N+Sg+Ine`
* *aprilist:* `apriĺ+N+Sg+Ela`
* *aprililõ:* `apriĺ+N+Sg+All`
* *aprilil:* `apriĺ+N+Sg+Ade`
* *aprililt:* `apriĺ+N+Sg+Abl`
* *aprilis:* `apriĺ+N+Sg+Tra`
* *apriliniq:* `apriĺ+N+Sg+Ter`
* *aprilildaq:* `apriĺ+N+Sg+Abe`
* *apriligaq:* `apriĺ+N+Sg+Com`
* *apriliq:* `apriĺ+N+Pl+Nom`
* *aprille:* `apriĺ+N+Pl+Gen`
* *aprille:* `apriĺ+N+Pl+Par`
* *aprillehe:* `apriĺ+N+Pl+Ill`
* *aprilen:* `apriĺ+N+Pl+Ine`
* *aprilest:* `apriĺ+N+Pl+Ela`
* *aprilelõ:* `apriĺ+N+Pl+All`
* *aprilel:* `apriĺ+N+Pl+Ade`
* *aprilelt:* `apriĺ+N+Pl+Abl`
* *apriles:* `apriĺ+N+Pl+Tra`
* *aprileniq:* `apriĺ+N+Pl+Ter`
* *aprileldaq:* `apriĺ+N+Pl+Abe`
* *aprilegaq:* `apriĺ+N+Pl+Com`

* LEXICON NMN_44SWDA  sõda:sõ%{tØ%}%{tdØ%}a
gradation: yes

* sõda examples:*
* *sõda:* `sõda+N+Sg+Nom`
* *sõa:* `sõda+N+Sg+Gen`
* *sõta:* `sõda+N+Sg+Par`
* *sõtta:* `sõda+N+Sg+Ill`
* *sõan:* `sõda+N+Sg+Ine`
* *sõast:* `sõda+N+Sg+Ela`
* *sõalõ:* `sõda+N+Sg+All`
* *sõal:* `sõda+N+Sg+Ade`
* *sõalt:* `sõda+N+Sg+Abl`
* *sõas:* `sõda+N+Sg+Tra`
* *sõaniq:* `sõda+N+Sg+Ter`
* *sõaldaq:* `sõda+N+Sg+Abe`
* *sõagaq:* `sõda+N+Sg+Com`
* *sõaq:* `sõda+N+Pl+Nom`
* *sõto:* `sõda+N+Pl+Gen`
* *sõto:* `sõda+N+Pl+Par`
* *sõttohe:* `sõda+N+Pl+Ill`
* *sõton:* `sõda+N+Pl+Ine`
* *sõtost:* `sõda+N+Pl+Ela`
* *sõtolõ:* `sõda+N+Pl+All`
* *sõtol:* `sõda+N+Pl+Ade`
* *sõtolt:* `sõda+N+Pl+Abl`
* *sõtos:* `sõda+N+Pl+Tra`
* *sõtoniq:* `sõda+N+Pl+Ter`
* *sõtoldaq:* `sõda+N+Pl+Abe`
* *sõtogaq:* `sõda+N+Pl+Com`

* LEXICON NMN_45KANA/RIHAE  kana:ka%{nØ%}n%{ao%}
* Yaml: **N-kana45**

LEXICON NMN_46HAIN   jalg:jalg
gradation: no

LEXICON NMN_46TARK   jalg:jal%{gØ%}
gradation: yes

* LEXICON NMN_47ASI  asi:a%{sś%}%{jiØ%}

* :%^NoPAL%^VowRM%>ö       PL_ALL_lE-STEM ;  IS THIS A REAL FORM?

* LEXICON NMN_2KASUNUQ/ELAENUEQ  elänüq:elänü

### SINGULAR GENITIVE STEMS

### PLURAL ALLATIVE STEMS

### TAGS THAT CAN BE FOLLOWED BY CLITICS "K"
### PLURAL TAGS
* +Err/Orth-no-q+Pl+Abe:%>ld%{aä%} K ;  no q

### SINGULAR TAGS

* +Err/Orth-no-q+Sg+Com:%>ga K ;  no q
* +Err/Orth-no-q+Err/Orth-front+Sg+Com:%>gä K ;  no q, front
* +Err/Orth-no-q+Sg+Com:%>ga BACK_K ;  no q

LEXICON Harm_Neutr_SG_INE_hn  RARE

### TAGS THAT CANNOT BE FOLLOWED BY CLITICS

### CASES ONLY

### TAGS THAT CAN BE FOLLOWED BY CLITICS

### TAGS WITH NO ADDED MORPHOLOGY THAT CANNOT BE FOLLOWED BY CLITICS

digits

* **LEXICON SASCont ** FROM NUMERALS, gives -aastanõ etc.

* * *

<small>This (part of) documentation was generated from [src/fst/affixes/nouns.lexc](https://github.com/giellalt/lang-vro/blob/main/src/fst/affixes/nouns.lexc)</small>

---

Noun inflection for Võro

* Yaml: **suhvli**

* Yaml: **kerge**

* Yaml: **peraedue**

* Yaml: **peraedue**

* Yaml: **tervues**

* Yaml: **A-ainus**

* Yaml: **N-oppaja5**

* Yaml: **N-mängjä5**

* Yaml: **fueuesiga**

kipõnʼ:kipõn
* Yaml:**N-kipwnj9**

allaś:allas
* Yaml:**N-kipwnj9**

veteĺ:vetel
* Yaml:**N-kipwnj9**

tukõv:tukõv
* Yaml: **N-ellaei4, N-kipwnj9**

elläi:elläi
* Yaml: **N-ellaei4, N-kipwnj9**

verrev:verrev
* Yaml: **N-ellaei4, N-kipwnj9**

gradation: no

gradation: yes
distinguished from 14RITS1KAS due to gradation

distinguished from 14RITS1KAS due to word final h

distinguished from 14RITS1KAS due to word final h

kotus:kotus
* Yaml: **N-kotus15**

inemine:inemi
* Yaml: **N-inemine16**

abilinõ:abili
* Yaml: **N-abilinw16**

LEXICON NUM_22VWROKWNW  võrokõnõ:võrokõ

LEXICON NUM_22NAANW  naanõ:naa

Gradation: No

vowel_harmony: front

Gradation: No

tarõ:tar

pesä:tar

nimi:nim

* LEXICON NUM_36KATS1  katś:kat

* LEXICON NUM_36UETS1  ütś:üt

kokr:ko%{kg%}r
* Yaml: **N-kokr36**

sõbõr:sõbõr
* Yaml: **N-swbwr36**
derived from 36särǵ

* Yaml: **aig, kand**

* Yaml: **juht́**

* Yaml: **aig, aig**

LEXICON NUM_43KANARIK 

LEXICON NUM_44SWDA  sõda:sõda

* Yaml: **N-jalg, N-hain**

* Yaml: **N-jalg, N-tark**

vro-digits

* **LEXICON ARABICCASES**  adds +Arab

* **LEXICON ARABICCASE**  adds +Arab

* **LEXICON ARABICCASE0**  adds +Arab

* **LEXICON DIGITCASES**  to distinguish between 0 and oblique

* **LEXICON DIGITCASE0**

* **LEXICON DIGITCASE**

* **LEXICON ARABICCASEORD** ordinals

* **LEXICON ARABICCASEORD-ERR** ordinal inflection when preceded
by .:, and with reduced case forms. The Err/Orth tag is added in the calling lexicon.

* **LEXICON ARABICCASECOLL** collectives

* **LEXICON ROMNUMTAGOBL**

* **LEXICON ARABICCOMPOUNDS**  ! arabic as first part,

* * *

<small>This (part of) documentation was generated from [src/fst/affixes/numerals.lexc](https://github.com/giellalt/lang-vro/blob/main/src/fst/affixes/numerals.lexc)</small>

---

Postpositions 
The Võro language postpositions ...

### POSTPOSITIONS WITH READY CASE ENDINGS

* * *

<small>This (part of) documentation was generated from [src/fst/affixes/postpositions.lexc](https://github.com/giellalt/lang-vro/blob/main/src/fst/affixes/postpositions.lexc)</small>

---

Pronoun inflection
The Võro language pronouns inflect in the same cases as regular
nouns, but with a colon (':') as separator.

### PERSONAL PRONOUN

CHECKME vowel harmony

LEXICON PERS_PL1  maq:m

LEXICON PERS_PL2  saq:

LEXICON PERS_PL3  timä:

### DEMONSTRATIVE PRONOUNS

### INDEFINITE PRONOUNS

### INTERROGATIVE PRONOUNS

* LEXICON PRON_36UETS1  ütś:üt

* * *

<small>This (part of) documentation was generated from [src/fst/affixes/pronouns.lexc](https://github.com/giellalt/lang-vro/blob/main/src/fst/affixes/pronouns.lexc)</small>

---

Proper noun inflection
The Võro language proper nouns inflect in the same cases as regular
nouns, but with a colon (':') as separator.

LEXICON PROP_1HANS1A  1 hanśa:hanśa

LEXICON PROP_1VIU  1 viu:viu

LEXICON PROP_1HERRAE  1 herrä:herrä

* Yaml: **suhvli**

* Yaml: **kerge**

LEXICON PROP_3ALADU  aladu:aladu
* Yaml: **peraedue**

LEXICON PROP_VERE  Rakvere:Rakv
* Yaml: **Rakvere**

* Yaml: **tervues**

* Yaml: **A-ainus**

* Yaml: **N-oppaja5**

* Yaml: **N-oppaja5**

* Yaml: **fueuesiga**

harmony: front

kipõń:kipõń
* Yaml: **N-ellaei4, N-kipwnj9**

sallai:sallai
* Yaml: **N-ellaei4, N-kipwnj9**

elläi:elläi
* Yaml: **N-ellaei4, N-kipwnj9**

tukõv:tukõv
* Yaml: **N-ellaei4, N-kipwnj9**

LEXICON PROP_10AMEERIGA  Ameeriga:Ameerik
cf. _10HWRAK

LEXICON PROP_10ESAEK  esäk:esäk

LEXICON PROP_10LEMBIT  Lembit:Lembi%{td%}

LEXICON PROP_10VIDRIK  vidrik:vidrik
gradation: no

Gradation: No

Gradation: No

Gradation: No

LEXICON PROP_14HAMMAS  hammas:hamba, saabas:saapa
gradation: yes
distinguished from 14RITS1KAS due to gradation

distinguished from 14RITS1KAS due to word final h

distinguished from 14RITS1KAS due to word final h

kotus:kotus
* Yaml: **N-kotus15**

kotus:kotus
* Yaml: **N-kotus15**

kotus:kotus
* Yaml: **N-kotus15**

Gradation: No

LEXICON PROP_16ABILINW 
abilinõ:abili
* Yaml: **N-abilinw16**

Gradation: No

Gradation: No

Gradation: No

gradation: yes
vowel_harmony: front

gradation: yes
vowel_harmony: front

gradation: yes

* LEXICON PROP_29KUU  kuu:kuu
Gradation: No

* LEXICON PROP_29HAEAE  kuu:kuu
Gradation: No

Gradation: No

gradation: yes

gradation: yes

tarõ:tar

nimi:nim

pesä:pesä

pesä:pesä

LEXICON PROP_36TUUM1  tuuḿ:t%{ou%}%{ou%}m
:%{back%} NMN_36TUUM1/XX1-SG_OBL ;  This allows for place names, which, for the most part, have nominative singulars that are identical to their genitive singulars.

LEXICON PROP_36SAERG1  särǵ:särgʼ

LEXICON PROP_36PAEIV  päiv:päiv

kogõr:kogõr
* Yaml: **N-kogwr36**
derived from 36särǵ

LEXICON PROP_37PINI  pini:pini

LEXICON PROP_37WLI  pini:pini

* LEXICON PROP_38PULL1  pulĺ:pull

* LEXICON PROP_38VIKS1  pulĺ:pull

* LEXICON PROP_38PAPP1  papṕ:papp

LEXICON PROP_40TALO  talo:talo

LEXICON PROP_40UJA  uja:uja

LEXICON PROP_41ASK  ask:asko
* Yaml: __aig, aig__

LEXICON PROP_44SWDA  sõda:sõda

LEXICON PROP_46HAIN  hain:hain
* Yaml: **N-jalg, N-hain**

* * *

<small>This (part of) documentation was generated from [src/fst/affixes/propernouns.lexc](https://github.com/giellalt/lang-vro/blob/main/src/fst/affixes/propernouns.lexc)</small>

---

Quantifier inflection
The Võro language quantifiers inflect in cases.

* * *

<small>This (part of) documentation was generated from [src/fst/affixes/quantifiers.lexc](https://github.com/giellalt/lang-vro/blob/main/src/fst/affixes/quantifiers.lexc)</small>

---


# Symbol affixes

* * *

<small>This (part of) documentation was generated from [src/fst/affixes/symbols.lexc](https://github.com/giellalt/lang-vro/blob/main/src/fst/affixes/symbols.lexc)</small>

---

Verb inflection
Võro language verbs inflect for person and number.

There are other verbs here, cf. V_ELAEMAE
* Yaml: **V-kasuma48**

There are other verbs here, cf. V_ELAEMAE
* Yaml: **V-kuioma48**

There are other verbs here, cf. V_ELAEMAE
* Yaml: **V-palama48**

There are other verbs here, cf. V_ELAEMAE
* Yaml: ____

There are other verbs here, cf. V_ELAEMAE
* Yaml: __V-sadama48__

Pss_PrfPrc: sadat

* **LEXICON V_49LWPMA** lõpma:lõpp
* **LEXICON V_49LWPMA/XX** lõpma:lõ%{pØ%}p

* **LEXICON V_50TONISWMA** tonisõma:tonis
* Yaml: **toniswma50**
* **LEXICON V_50TONISWMA/HELISEMAE** tonisõma:tonis

* **LEXICON V_50HELISEMAE** helisemä:helis
* Yaml: **helisemae50**

* **LEXICON V_51NWSWMA** nõsõma:nõs
* Yaml: **nwswma51**
cf. tulõma
* **LEXICON V_51PAESEMAE** päsemä:päs
* Yaml: **paesemae51**
cf. tulõma

* **LEXICON V_51NWSWMA/PAESEMAE** nõsõma:nõs

* **LEXICON V_52ALOSTWLWMA** alostõlõma:alostõll
* Yaml: **alostwllwma52**
* **LEXICON V_52EHITELEMAE** ehitelemä:ehitell
ehitelemä:ehitell
* Yaml: **ehitellemae52**

* **LEXICON V_52ALOSTWLWMA/EHITELEMAE** alostõllõma:alostõ%{lØ%}l

* **LEXICON V_53KAEMA** kaema:ka
* **LEXICON V_53JAEAEMAE** 
* **LEXICON V_53XX/JAEAEMAE** 

* :%^VOWRaise Harm_Neutr_77JUUMA/SUEUEMAE-PSS_IND_PRT_di ;  only 3rd person

*  ACT-PRFPRC_nUq-SG_NOM ;  jäänüq keenüq

* :%^VOWRaise%^VowRM%>i V_77JUUMA/SUEUEMAE_RAISED-VOWEL-TENSE ;  jäi kii
* :%^VowRM%>i V_77JUUMA/SUEUEMAE_NON-RAISED-VOWEL-TENSE ;  jäi kei
* :%^VOWRaise ACT_IND_PRS_3_s/sEq ;  (5) RAISED jääs jääseq 

* +Err/Dial: ACT_IND_PRS_PL3_vAq ;  (6) joovaq sööväq

* **LEXICON V_53KAEMA/XX** kaema:ka

* :%>e Harm_Neutr_77JUUMA/SUEUEMAE-PSS_IND_PRT_di ;  only 3rd person

* :%>e ACT-PRFPRC_nUq-SG_NOM ;  jäänüq keenüq

* :%>i V_77JUUMA/SUEUEMAE_RAISED-VOWEL-TENSE ;  jäi kii
* :%>e V_77JUUMA/SUEUEMAE_NON-RAISED-VOWEL-TENSE ;  jäi kei
* :%>e ACT_IND_PRS_3_s/sEq ;  (5) RAISED jääs jääseq 

* :%>e ACT_IND_PRS_PL3_vAq ;  (6) joovaq sööväq

* __LEXICON V_54PUTMA__ 
* __LEXICON V_54LEPMAE__ 

* __LEXICON V_54PUTMA/LEPMAE__

* __LEXICON V_54ISTMA__ 
* __LEXICON V_54KAEAETSMAE__ 
* __LEXICON V_54ISTMA/KAEAETSMAE__ 

* **LEXICON V_55KWNWLWMA** kõnõlõma:kõ̭nõl
* Yaml: **kwnwlwma55**
* **LEXICON V_55HAERELEMAE** härelemä:härel
* Yaml: **haerelemae55**

* **LEXICON V_56HIIBWLWMA** hiibõlõma:hiibõl
* Yaml: **hiibwlwma56**
* **LEXICON V_56HEIKELEMAE** heikelemä:heikel
* Yaml: **heikelemae56**

* **LEXICON V_56HIIBWLWMA/HEIKELEMAE** hiibõlõma:hiibõl

* **LEXICON V_56KAIBLWMA** kaiblõma+V:kai%{bv%}%{õØ%}l
* Yaml: **hiibwlwma56**

* **LEXICON V_56KAIBLWMA/XX** kaiblõma+V:kai%{bv%}%{õØ%}l

taplõma:tapõl
* Yaml: **taplwma57**
ütlemä:ütel
* Yaml: **kiirdlemae57**

* *taplõma:* `taplõma+V+Inf/mA` (Eng. # (1))
* *tapõldaq:* `taplõma+V+Inf` (Eng. # (2))
* *tapõlnuq:* `taplõma+V+Act+PrfPrc` (Eng. # (3))
* *tapõld:* `taplõma+V+Pss+PrfPrc` (Eng. # (4))
* *taplõ:* `taplõma+V+Act+Ind+Prs+Sg1` (Eng. # (5))
* *taplõt:* `taplõma+V+Act+Ind+Prs+Sg2` (Eng. # (5))
* *taplõs:* `taplõma+V+Act+Ind+Prs+Sg3` (Eng. # (6))
* *taplõmiq:* `taplõma+V+Act+Ind+Prs+Pl1` (Eng. # (5))
* *taplõtiq:* `taplõma+V+Act+Ind+Prs+Pl2` (Eng. # (5))
* *taplõsõq:* `taplõma+V+Act+Ind+Prs+Pl3` (Eng. # (5))
* *taplõ:* `taplõma+V+Act+Ind+ConNegII` (Eng. # (1))
* *tapli:* `taplõma+V+Act+Ind+Prt+Sg1` (Eng. # (7))
* *taplit:* `taplõma+V+Act+Ind+Prt+Sg2` (Eng. # (7))
* *tapõĺ:* `taplõma+V+Act+Ind+Prt+Sg3` (Eng. # (8))
* *taplimiq:* `taplõma+V+Act+Ind+Prt+Pl1` (Eng. # (7))
* *taplitiq:* `taplõma+V+Act+Ind+Prt+Pl2` (Eng. # (7))
* *tapliq:* `taplõma+V+Act+Ind+Prt+Pl3` (Eng. # (7))
* *tapõlda:* `taplõma+V+Pss+Ind+Prs+Sg1` (Eng. # (4))
* *tapõldas:* `taplõma+V+Pss+Ind+Prs+Sg3` (Eng. # (4))
* *taplõv:* `taplõma+V+Act+PrsPrc+Sg+Nom` (Eng. # (1))
* *tapõlguq:* `taplõma+V+Jus` (Eng. # (2,3,4, ?9))

võitlõma:võitõl
* Yaml: **taplwma57**
kiirdlemä:keerdel
* Yaml: **kiirdlemae57**

* *väär{dØ}{eØ}{lĺ}{front}^Pen^VOWRaise^Pen^StrGStem^Pen^VowRM^NoPAL>{eõ}>m{aä}*
* *väärd0l00000000>e>mä*

kullõma+V:ku%{lØ%}l%{õØ%}%{lĺ%}
* Yaml: **kiirdlemae57**

* *ku%{lØ%}l%{õØ%}%{lĺ%}{back}^Pen^VOWRaise^Pen^CC2C^Pen^VowRM^NoPAL>{eõ}>m{aä}*
* *ku0l0l00000000>õ>ma*

* **LEXICON V_58HIRNAHTAMA** hirnahtama:hirnahta
* Yaml: **V-hirnahtama58**

* **LEXICON V_58TAEHENDAEMAE** tähendämä:tähendä
* Yaml: **V-hirnahtama58, V-taehendaemae**
front

* **LEXICON V_58HIRNAHTAMA/TAEHENDAEMAE** hirnahtama:hirnahta, tähendämä:tähend

* **LEXICON V_59KAOTAMA** kaotama:kaota
Based on 59KAOTAMA
* Yaml: **kerguetaemae**

* **LEXICON V_59KAOTAMA/KERGUETAEMAE** kaotama:kao%{tt́d%}, kergütämä:kergü%{tt́d%}

+Pss+Ind+Prs+Sg1, +Pss+Ind+Prt+Sg1
+Pss+PrsPrc, +Pss+PrfPrc

+Act+Ind+Prs+Sg1, +Act+Ind+ConNegII, +Act+Imprt+Sg2
+Act+Ind+Prs+Neg, +Act+Ind+Prt+Neg, +Act+Ind+ConNegI

+Act+Ind+Prs+Sg3, +Act+Ind+Prs+Pl3

* :%^VOWRaise%^WGStem%^NoPAL%>i   ACT_IND_PRT_SG1_ZERO/SG2_q/PL3_q ;  kaodi
+Act+Ind+Prt+Sg1, +Err/Dial+Act+Ind+Prt+Sg2, +Act+Ind+Prt+Pl3

+Act+Ind+Prs+Sg2, +Err/Dial+Act+Ind+Prs+Sg2, 
+Act+Ind+Prs+Pl1, +Act+Ind+Prs+Pl2

* :%^VOWRaise%^StrGStem%^NoPAL%>i Harm_Neutr_ACT_IND_PRT_SG2_USUALLY-STRONG ;  kaoti
+Act+Ind+Prt+Sg2, +Err/Dial+Act+Ind+Prt+Sg2, +Act+Ind+Prt+Pl1,
+Act+Ind+Prt+Pl2, +Err/Dial+Act+Ind+Prt+Pl3

+Act+Ind+Prt+Sg3

* kaotama examples:*
* *kaoda-aiq:* `kaotama+V+Act+Ind+Prs+Neg`
* *kaoda-as:* `kaotama+V+Act+Ind+Prt+Neg`
* *kaoda:* `kaotama+V+Act+Ind+ConNegII`
* *kaoda:* `kaotama+V+Act+Ind+Prs+Sg1`
* *kaodaq:* `kaotama+V+Act+Ind+ConNegI`
* *kaodi:* `kaotama+V+Act+Ind+Prt+Sg1`
* *kaodiq:* `kaotama+V+Act+Ind+Prt+Pl3`
* *kaotaguq:* `kaotama+V+Jus`
* *kaotama:* `kaotama+V+Inf/mA`
* *kaotamiq:* `kaotama+V+Act+Ind+Prs+Pl1`
* *kaotanu:* `kaotama+V+Act+PrfPrc+Sg+Gen`
* *kaotanuhe:* `kaotama+V+Act+PrfPrc+Sg+Ill`
* *kaotanuid:* `kaotama+V+Act+PrfPrc+Pl+Par`
* *kaotanuidõ:* `kaotama+V+Act+PrfPrc+Pl+Gen`
* *kaotanuihe:* `kaotama+V+Act+PrfPrc+Pl+Ill`
* *kaotanuq:* `kaotama+V+Act+PrfPrc`

* **LEXICON V_60MANITSWMA** manitsõma:mani
* Yaml: **manitswma60,manitswma61>manitswma**
* **LEXICON V_60EHITSEMAE** ehitsemä:ehii
* Yaml: **manitswma60,manitswma61>manitswma**

* **LEXICON V_60MANITSWMA/EHITSEMAE** manitsõma:mani

argnõma:arg
* Yaml: **argnwma62**
tärknemä:tärk
* Yaml: **taerknemae62**

* **LEXICON V_63SWIMAMA** sõimama:sõima
* Yaml: **V-swimama63**
* **LEXICON V_63SWIMAMA/XX** sõimama:sõima

* **LEXICON V_63VISKAMA** viskama:vis%{kØ%}a
gradation: yes
* Yaml: **V-viskama63**
* **LEXICON V_63HINGAEMAE** hingämä:hingä
gradation: no
* Yaml: **V-hingaemae63**

* **LEXICON V_63VISKAMA/HINGAEMAE** viskama:viska

* +Err/Dial+Pss+Ind+Prt+Sg2:%^Pen%^VOWLower%^Pen%^WGStem%>di K ;  no    q
* +Err/Dial+Pss+Ind+Prt+Pl3:%^Pen%^VOWLower%^Pen%^WGStem%>di K ;  no    q
* +Err/Dial+Pss+Ind+Prt+Sg2:%^Pen%^VOWLower%^Pen%^WGStem%>tid%{eõ%} K ;  no    q
* +Err/Dial+Pss+Ind+Prt+Pl1:%^Pen%^VOWLower%^Pen%^WGStem%>timi K ;  no    q
* +Err/Dial+Pss+Ind+Prt+Pl2:%^Pen%^VOWLower%^Pen%^WGStem%>titi K ;  no    q
* +Err/Dial+Pss+Ind+Prt+Pl3:%^Pen%^VOWLower%^Pen%^WGStem%>tiv%{aä%} K ;  no    q

+Pss+Ind+Prt +Sg1-+Pl3, ConNeg

THIS FAR 2016-08-27
* Yaml: **V-puhksama64**
* Yaml: **V-rehksaemae64**

* **LEXICON V_67HARINWMA** harinõma:hari
* Yaml: **harinwma66,harinwma67 =>harinwma**
* **LEXICON V_67NAEGUENEMAE** nägünemä:nägü
* Yaml: **harinwma66,harinwma67 =>harinwma**

* **LEXICON V_67HARINWMA/NAEGUENEMAE** harinõma:hari

* Yaml: **V-harkuma68**
* Yaml: **V-naelguemae68**

* **LEXICON V_69HAARDUMA** haarduma:haar%{dØ%}u
* **LEXICON V_69SUENDUEMAE** sündümä:sün%{dn%}ü
* **LEXICON V_69HAARDUMA/SUENDUEMAE** sündümä:sündü

Act_Ind_Prs_Pl3: essüseq

* **LEXICON V_69SUURDUMA** suurduma:suurdu
* **LEXICON V_69HUEUERDUEMAE** hüürdümä:h%{öü%}%{öü%}r%{dØ%}ü
* **LEXICON V_69SUURDUMA/HUEUERDUEMAE** hüürdümä:h%{öü%}%{öü%}r%{dØ%}ü vowel raising Required 2016-09-15

V_Inf/mA: miildümä 

* **LEXICON V_70UNWHTUMA** unõhuma:unõhtu
* Yaml: **V-unwhuma**
* **LEXICON V_70ÄNGÄHTÜMÄ** ängähümä:ängähtü
* Yaml: **V-eraelduemae**

* **LEXICON V_70UNWHTUMA/ÄNGÄHTÜMÄ** unõhuma:unõhtu

* **LEXICON V_70VIPWRDUMA** unõhtuma:unõhtu
* Yaml: **V-unwhtuma**
* **LEXICON V_70ERAELDUEMAE** eräldümä:eräldü
* Yaml: **V-eraelduemae**

* **LEXICON V_70VIPWRDUMA/ERAELDUEMAE** unõhtuma:unõhtu

* **LEXICON V_71HALLWTUMA** hallõtuma:hallõtu
* Yaml: **V-hallwtuma**
* **LEXICON V_71ERAETUEMAE** erätümä:erä%{td%}ü
* Yaml: **V-eraetuemae**

* **LEXICON V_71HALLWTUMA/ERAETUEMAE** hallõtuma:hallõtu

* **LEXICON V_72VAOMA** vaoma:%{ˋØ%}va%^I7o
* Yaml: **vaoma**
* **LEXICON V_72TAEUEMAE** täümä:täü
* Yaml: **haeoemae**

* **LEXICON V_72VAOMA/TAEUEMAE** vaoma:vao

* **LEXICON V_74KULUMA** kuluma:kullu
* Yaml: **V-kuluma**
* **LEXICON V_74VAESUEMAE** väsümä:vässü
* Yaml: **V-vaesuemae**

* **LEXICON V_74KULUMA/VAESUEMAE** kuluma:kullu

* **LEXICON V_75VALAMA** valama:vala
* Yaml: **V-valama75**
vala, valla, vali, valõ
* **LEXICON V_75JAERAEMAE** järämä:järä
* Yaml: **V-jaeraemae75**

* **LEXICON V_75VALAMA/JAERAEMAE** valama:vala

* **LEXICON V_76HIGOMA** higoma:hi%{kg0%}o
* Yaml: **V-higoma76**
* **LEXICON V_76PUEGAEMAE** pügämä:pü%{kg0%}ä
* Yaml: **V-puegaemae76**

* **LEXICON V_76HIGOMA/PUEGAEMAE** higoma:hi%{kg0%}o
+Act+PrsPrc+Sg OBL, Inf/mA, 

* :%^Pen%^G3 Harm_Neutr_INF_ZEROq ;  (2) lukõq
* :%^Pen%^G3 Harm_Neutr_ACT_PRSPRC_SG_NOM_v ;  (2b) lukõv
Inf, Act+PrsPrc+Sg+Nom

Pss+PrfPrc, Pss+PrsPrc

* :%^Pen%^G2 ACT_IND_PRS_SG3_ZERO/PL3_vAq ;  (6) lugõma
Ind+Prs+ 3

Retain consonant and stem vowel

Weaken consonant and semi-retension of stem vowel

Act+Ind+Prs+Sg1/Sg2/Pl1/Pl2, Ind+ConNegII, Ind+Prs+ConNeg
Pss+Ind

Retain consonant and stem vowel

Weaken consonant and replace stem vowel with i
* :%^Pen%^VOWLower%^Pen%^WGStem%^VowRM%>i Harm_Neutr_LOGÕMA_ACT_IND_PRT-SG1 ;  (7) loi
Act+Ind+PrtSg1/Sg2/Pl1-3

Retain consonant remove stem vowel and add i
* :%^VowRM ACT_IND_PRT_SG3_i ;  (8) lugi
Act+Ind+Prt+Sg3

+Jus

* **LEXICON V_76JAGAMA** jagama:ja%{kg0%}a
* Yaml: **V-higoma76**

* **LEXICON V_76JAGAMA/XX** jagama:ja%{kg0%}a
+Act+PrsPrc+Sg OBL, Inf/mA, 

* :%^Pen%^G3 Harm_Neutr_INF_ZEROq ;  (2) lukõq
* :%^Pen%^G3 Harm_Neutr_ACT_PRSPRC_SG_NOM_v ;  (2b) lukõv
Inf, Act+PrsPrc+Sg+Nom

Pss+PrfPrc, Pss+PrsPrc

* :%^Pen%^VOWLower%^Pen%^WGStem%^VowRM%>e Harm_Neutr_LUGWMA_PSS-PRC ;  (4) loet

*  ACT_IND_PRS_SG3_ZERO/PL3_vAq ;  (6) lugõma
Ind+Prs+ 3

Retain consonant and stem vowel

Weaken consonant and semi-retension of stem vowel

Act+Ind+Prs+Sg1/Sg2/Pl1/Pl2, Ind+ConNegII, Ind+Prs+ConNeg
Pss+Ind

Retain consonant and stem vowel

Weaken consonant and replace stem vowel with i
* :%^Pen%^VOWLower%^Pen%^WGStem%^VowRM%>i Harm_Neutr_LOGÕMA_ACT_IND_PRT-SG1 ;  (7) loi
Act+Ind+PrtSg1/Sg2/Pl1-3

Retain consonant remove stem vowel and add i
* :%^VowRM ACT_IND_PRT_SG3_i ;  (8) lugi
Act+Ind+Prt+Sg3

+Jus

* **LEXICON V_76LUGWMA** lugõma:lu%{kg0%}õ
* Yaml: **V-higoma76**

* **LEXICON V_76LUGWMA/XX** lugõma:lu%{kg0%}õ

Retain consonant and stem vowel
* :%^Pen%^G2 Harm_Neutr_INF_mA ;  (1) lugõma:lu%{kgØ%}õ

Pss+PrfPrc, Pss+PrsPrc

Weaken consonant and semi-retension of stem vowel

Weaken consonant and semi-retension of stem vowel

Act+Ind+Prs+Sg1/Sg2/Pl1/Pl2, Ind+ConNegII, Ind+Prs+ConNeg
Pss+Ind

Retain consonant and stem vowel
*  ACT_IND_PRS_SG3_ZERO/PL3_vAq ;  (6) lugõma
Ind+Prs+ 3

Weaken consonant and replace stem vowel with i
* :%^Pen%^VOWLower%^Pen%^WGStem%^VowRM%>i Harm_Neutr_LOGÕMA_ACT_IND_PRT-SG1 ;  (7) loi
Act+Ind+PrtSg1/Sg2/Pl1-3

Retain consonant remove stem vowel and add i
* :%^VowRM ACT_IND_PRT_SG3_i ;  (8) lugi
Act+Ind+Prt+Sg3

* **LEXICON V_77JUUMA** juuma:joo
* Yaml: **juuma**
* **LEXICON V_77SUEUEMAE** süümä:süü
* Yaml: **sueuemae**

* **LEXICON V_77JUUMA/SUEUEMAE** juuma:joo

* :%^OO2Õ%>i V_77JUUMA/SUEUEMAE_NON-RAISED-VOWEL-TENSE ;  (4) jõi- poi- sei- möi-

* :%^VOWRaise V_77JUUMA/SUEUEMAE_RAISED-VOWEL ;  (1) juu, süü

* :%^VOWLower V_77JUUMA/SUEUEMAE_NOT-RAISED-VOWEL ;  (2) joo- söö-

* :%^VOWRaise%^VowRM%>vv V_77JUUMA/SUEUEMAE_RAISED-VOWEL-TENSE ;  (3) juvv

* :%^VOWRaise ACT_IND_PRS_SG3_ZERO ;  (5) RAISED juu süü
* +Err/Orth:%^VOWRaise%>s ACT-COND ;  juussiq
*  ACT_IND_PRS_PL3_vAq ;  (6) joovaq sööväq

*  PSS_PRFPRC_d ; 

*  Harm_Neutr_77JUUMA/SUEUEMAE-PSS_IND_PRT_di ;  only 3rd person

* LEXICON V_77JUUMA/SUEUEMAE_NOT-RAISED-VOWEL  joo- söö-
*  ACT-PRFPRC_nUq-SG_NOM ;  joonuq

* LEXICON V_77JUUMA/SUEUEMAE_RAISED-VOWEL-TENSE  juvv
*  Harm_Neutr_INF_Aq ;  juvvaq süvväq
* :%>%{aä%} Harm_Neutr_JUVVA_PSS_IND_PRS ;  juvva süvvä
* :%>i Harm_Neutr_JUVVA_PSS_IND_PRT_1/2 ;  juvvi süvvi

* LEXICON V_77JUUMA/SUEUEMAE_NON-RAISED-VOWEL-TENSE  jõi-

* **LEXICON V_77KAEUEMAE** käümä:käü
* Yaml: **sueuemae**

* **LEXICON V_77XX/KAEUEMAE** käümä:käü

* :%^VOWRaise V_77JUUMA/SUEUEMAE_RAISED-VOWEL ;  (1) käü

*  V_77JUUMA/SUEUEMAE_NOT-RAISED-VOWEL ;  (2) käü-

* :%^VowRM%>vv V_77JUUMA/SUEUEMAE_RAISED-VOWEL-TENSE ;  (3) kävv

* :%^VowRM%>ve V_77JUUMA/SUEUEMAE_NON-RAISED-VOWEL-TENSE ;  (4) käve

*  ACT_IND_PRS_SG3_ZERO ;  (5) RAISED käü

*  ACT_IND_PRS_PL3_vAq ;  (6) käüväq

* **LEXICON V_78VWIMA** võima:või
* Yaml: **V-vwima**
* **LEXICON V_VWIMA/XX** võima:või

* Yaml: **saama**

* Yaml: __V-viimae__

* **LEXICON V_78MINEMAE** minemä:min
* Yaml: **V-minemae**
* **LEXICON V_XX/MINEMAE** minemä:min

Remainder is in exceptions.lexc
minemä **to go/ mennä**

* **LEXICON V_79TULWMA** tulõma:tul
* Yaml: **tulwma**
* **LEXICON V_79TULWMA/XX** tulõma:tul

Retain consonant and stem vowel

* :l Harm_Neutr_INF_Aq ;  (2) tullaq
* :l%>%{eõ%} Harm_Neutr_ACT_PRSPRC_SG_NOM_v ;  (2b) tullõv
Act+PrsPrc+Sg+Nom

* **LEXICON V_79PURWMA** purõma:pur
* Yaml: **purwma**
* **LEXICON V_79PURWMA/XX** purõma:pur
Retain consonant 
*  Harm_Neutr_LUGWMA_PSS-PRC ;  (4) pur
Pss+PrfPrc, Pss+PrsPrc, 

Retain consonant and stem vowel
* :%{eõ%} Harm_Neutr_ACT_PRSPRC_v_LUGWMA ;  (1) purõma
+Act+PrsPrc+Sg OBL, Inf/mA, 
+Jus, 

Strengthen consonant
* :%^StrGStem Harm_Neutr_INF_Aq ;  (2) purraq
Inf 
Strengthen consonant 
* :%^StrGStem%>%{eõ%} Harm_Neutr_ACT_PRSPRC_SG_NOM_v ;  (2b) purrõv
Act+PrsPrc+Sg+Nom

Retain consonant and stem vowel
*  Harm_Neutr_ACT-PRFPRC_v_LUGWMA ;  (3) purnuq
+Act+PrfPrc

Retain consonant and add õ
* :%{eõ%} Harm_Neutr_LUGWMA_IND-CONNEGII ;  (5) purõ
Act+Ind+Prs+Sg1/Sg2/Pl1/Pl2, Ind+ConNegII, Ind+Prs+ConNeg
Pss+Ind

Retain consonant and stem vowel
* :%{eõ%} ACT_IND_PRS_SG3_ZERO/PL3_vAq ;  (6) purõma
Ind+Prs+ 3

Strengthen consonant and replace stem vowel with i
* :%>i TULWMA_ACT_IND_PRT_ZERO_and_X ;  (7) puri
Act+Ind+PrtSg1/Sg2/Pl1-3

consonant and add i
* ACT_IND_PRT_SG3_i ;  (8)1 puri
Act+Ind+Prt+Sg3

* **LEXICON V_79OLWMA** olõma:o

* **LEXICON V_79OLWMA/XX** olõma:o

* **LEXICON V_80RAPAHUTMA** rapahutma:rapahuta
* **LEXICON V_80HAEMMAEHUETMAE** hämmähütmä:hämmähütä

* LEXICON V_80RAPAHUTMA/HAEMMAEHUETMAE  rapahutma:rapahuta

Retain consonant and stem vowel
* :t Harm_Neutr_ACT_PRSPRC_v_LUGWMA ;  (1) rapahutma
+Act+PrsPrc+Sg OBL, Inf/mA, 
+Jus, 

Strengthen consonant
* :t%>%{aä%} Harm_Neutr_INF_ZEROq ;  (2) rapahutaq
Inf 
Strengthen consonant 
* :t Harm_Neutr_ACT_PRSPRC_SG_NOM_vA ;  (2b) rapahutva
Act+PrsPrc+Sg+Nom

Retain consonant and stem vowel
* :t Harm_Neutr_ACT-PRFPRC_v_LUGWMA ;  (3) rapahutnuq
+Act+PrfPrc

Retain consonant 
* :d%>%{eõ%} Harm_Neutr_LUGWMA_PSS-PRC ;  (4) rapahudõ
Pss+PrfPrc, Pss+PrsPrc, 

Retain consonant and add õ
* :d%>%{aä%} Harm_Neutr_LUGWMA_IND-CONNEGII ;  (5) rapahuda

Act+Ind+Prs+Sg1/Sg2/Pl1/Pl2, Ind+ConNegII, Ind+Prs+ConNeg
Pss+Ind

Retain consonant and stem vowel
* :t ACT_IND_PRS_SG3_ZERO/PL3_vAq ;  (6) rapahut
Ind+Prs+ 3

Strengthen consonant and replace stem vowel with i
* :d%^VowRM%>i TULWMA_ACT_IND_PRT_ZERO_and_X ;  (7) rapahudi
Act+Ind+PrtSg1/Sg2/Pl1-3

Strengthen consonant and add ʼ
* : ACT_IND_PRT_SG3_t-PAL ;  (8) rapahut́ and error rapahut
Act+Ind+Prt+Sg3

* **LEXICON V_81TEGEMAE** tegemä:t
* Yaml: **tegemä**
Work
* **LEXICON V_81XX/TEGEMAE** tegemä:t

* tegemä examples:*
* *tegemä:* `tegemä+V+Inf/mA` (Eng. # (1))
* *tetäq:* `tegemä+V+Inf` (Eng. # (2))
* *tennüq:* `tegemä+V+Act+PrfPrc` (Eng. # (3))
* *tett:* `tegemä+V+Pss+PrfPrc` (Eng. # (4))
* *tii:* `tegemä+V+Act+Ind+Prs+Sg1` (Eng. # (5))
* *tiit:* `tegemä+V+Act+Ind+Prs+Sg2` (Eng. # (5))
* *tege:* `tegemä+V+Act+Ind+Prs+Sg3` (Eng. # (6))
* *teemiq:* `tegemä+V+Act+Ind+Prs+Pl1` (Eng. # (?5)!!)
* *tiitiq:* `tegemä+V+Act+Ind+Prs+Pl2` (Eng. # (5))
* *tegeväq:* `tegemä+V+Act+Ind+Prs+Pl3` (Eng. # (?6)!!)
* *tiiq:* `tegemä+V+Act+Ind+ConNegI` (Eng. # ()!!)
* *tii:* `tegemä+V+Act+Ind+ConNegII` (Eng. # ()!!)
* *tei:* `tegemä+V+Act+Ind+Prt+Sg1` (Eng. # (7))
* *teit:* `tegemä+V+Act+Ind+Prt+Sg2` (Eng. # (7))
* *tekḱ:* `tegemä+V+Act+Ind+Prt+Sg3` (Eng. # (8))
* *teimiq:* `tegemä+V+Act+Ind+Prt+Pl1` (Eng. # (7))
* *teitiq:* `tegemä+V+Act+Ind+Prt+Pl2` (Eng. # (7))
* *teiq:* `tegemä+V+Act+Ind+Prt+Pl3` (Eng. # (7))
* *tetä:* `tegemä+V+Pss+Ind+Prs+Sg1` (Eng. # (?4)!!)
* *tetäs:* `tegemä+V+Pss+Ind+Prs+Sg3` (Eng. # (?4)!!)
* *tettäv:* `tegemä+V+Pss+PrsPrc+Sg+Nom` (Eng. # (4))
* *tekuq:* `tegemä+V+Jus` (Eng. # (9))

tegemä **to do/ tehdä**

* **LEXICON V_81NAEGEMAE** nägemä:täg
* Yaml: **nägemä**
Work
* **LEXICON V_81XX/NAEGEMAE** nägemä:te%{kØ%}%{ḱgØ%}

* nägemä examples:*
* *nägemä:* `nägemä+V+Inf/mA` (Eng. # (1))
* *nätäq:* `nägemä+V+Inf` (Eng. # (2))
* *nännüq:* `nägemä+V+Act+PrfPrc` (Eng. # (3))
* *nätt:* `nägemä+V+Pss+PrfPrc` (Eng. # (4))
* *näi:* `nägemä+V+Act+Ind+Prs+Sg1` (Eng. # (5))
* *näit:* `nägemä+V+Act+Ind+Prs+Sg2` (Eng. # (5))
* *näge:* `nägemä+V+Act+Ind+Prs+Sg3` (Eng. # (6))
* *näemiq:* `nägemä+V+Act+Ind+Prs+Pl1` (Eng. # (?5)!!)
* *näitiq:* `nägemä+V+Act+Ind+Prs+Pl2` (Eng. # (5))
* *nägeväq:* `nägemä+V+Act+Ind+Prs+Pl3` (Eng. # (?6)!!)
* *näiq:* `nägemä+V+Act+Ind+ConNegI` (Eng. # ()!!)
* *näi:* `nägemä+V+Act+Ind+ConNegII` (Eng. # ()!!)
* *näi:* `nägemä+V+Act+Ind+Prt+Sg1` (Eng. # (7))
* *näit:* `nägemä+V+Act+Ind+Prt+Sg2` (Eng. # (7))
* *näkḱ:* `nägemä+V+Act+Ind+Prt+Sg3` (Eng. # (8))
* *näimiq:* `nägemä+V+Act+Ind+Prt+Pl1` (Eng. # (7))
* *näitiq:* `nägemä+V+Act+Ind+Prt+Pl2` (Eng. # (7))
* *näiq:* `nägemä+V+Act+Ind+Prt+Pl3` (Eng. # (7))
* *nätä:* `nägemä+V+Pss+Ind+Prs+Sg1` (Eng. # (?4)!!)
* *nätäs:* `nägemä+V+Pss+Ind+Prs+Sg3` (Eng. # (?4)!!)
* *nättäv:* `nägemä+V+Pss+PrsPrc+Sg+Nom` (Eng. # (4))
* *näkuq:* `nägemä+V+Jus` (Eng. # (9))

nägemä **to see/nähdä**

* **LEXICON V_82ANDMA** andma:and
* Yaml: **andma**
* **LEXICON V_82PUEUEDMAE** püüdmä:püüd
* Yaml: **pueuedmae**

* **LEXICON V_82ANDMA/PUEUEDMAE** andma:%{ˋØ%}an%{dd́n%}

* LEXICON V_83NÕSTMA   nõstma:nõst
gradation: no
* Yaml: **nwstma**
* LEXICON V_83PÄSTMÄ   nõstma:nõst
gradation: no
* Yaml: **nwstma**

* LEXICON V_83NÕSTMA/PÄSTMÄ   nõstma:nõst

* LEXICON V_83SÕITMA   sõitma:sõit
gradation: yes
* Yaml: **switma**
* LEXICON V_83HEITMAE   heitmä:heit
gradation: yes
* Yaml: **heitmae**

* LEXICON V_83SÕITMA/HEITMAE   sõitma:sõi%{tt́d%}a

IS THIS RIGHT? 2015-09-02

sõida

* LEXICON V_83TAHTMA   sõitma:sõit
gradation: yes
* Yaml: **switma**

* LEXICON V_83TAHTMA/XX   sõitma:sõi%{tt́d%}a tahtma+V:tah%{tt́Ø%}a

IS THIS RIGHT? 2015-09-02

sõida

* LEXICON V_83LAULMA   laulma:laul
gradation: yes
* Yaml: **switma**

* LEXICON V_83LAULMA/XX   laulma:lau%{lĺ%}

HERE is the distinction 2016-10-04

IS THIS RIGHT? 2015-09-02

* LEXICON V_83ATMA   atma:atta
gradation: yes
* Yaml: **switma**

* LEXICON V_83ATMA/XX   atma:a%{tØ%}%{tt́%}

IS THIS RIGHT? 2015-09-02

* LEXICON V_83SUTMA   atma:a%{tØ%}%{tt́%}a
gradation: yes
* Yaml: **switma**
* LEXICON V_83PETMÄ   petmä:pe%{tØ%}%{tt́%}ä
gradation: G3, G4
* Yaml: **heitmae**

* LEXICON V_83SUTMA/PETMÄ   sutma:su%{tØ%}%{tt́%}a

IS THIS RIGHT? 2015-09-02

sõida

* LEXICON V_83VWTMA   võtma:võ%{tØ%}%{tt́Ø%}a
gradation: G3, G4, G1
* Yaml: **vwtma**

* LEXICON V_83VWTMA/XX   võtma:võ%{tØ%}%{tt́Ø%}a

sõida

* LEXICON V_84LASKMA  laskma:lask
* Yaml: **nwstma**
* LEXICON V_84KAESKMAE  käskmä:käsk
* Yaml: **nwstma**
* LEXICON V_84LASKMA/KAESKMAE  laskma:las%{kḱØ%}
* Yaml: **nwstma**

* **LEXICON V_85HIRNMA** kakma:kaku hirnma:hirnu
* Yaml: **kakma**
* **LEXICON V_85TUEMPSMAE** kakma:kaku hirnma:hirnu
* Yaml: **kakma**
* **LEXICON V_85HIRNMA/TUEMPSMAE** kakma:kaku hirnma:hirnu

* **LEXICON V_85HAUDMA**  kakma:%{ˋØ%}ka%{kØ%}%{kḱ%}u 
* Yaml: **haudma**
* **LEXICON V_85VAELKMAE**  haudma:haud
* Yaml: **vaelkmae**
* **LEXICON V_85HAUDMA/VAELKMAE** kakma:kakk haudma:haud

* **LEXICON V_85KAKMA**  kakma:%{ˋØ%}ka%{kØ%}%{kḱ%}u 
* Yaml: **haudma**
* **LEXICON V_85TRUEKMAE**  trükmä:trü%{kØ%}%{kḱ%}ü
* Yaml: **vaelkmae**
* **LEXICON V_85KAKMA/TRUEKMAE** kakma:ka%{kØ%}%{kḱ%}u

* **LEXICON V_86ISTMA** istma:istu
* Yaml: **istma**
* **LEXICON V_86ISTMA/XX** istma:istu

* **LEXICON V_86PUTMA** istma:istu
* Yaml: **istma**
* **LEXICON V_86PUTMA/XX** istma:istu

* **LEXICON V_86JAHTJMA** jaht́ma:ˋjah%{tØ%}i
* Yaml: **jahtjma**
* **LEXICON V_86EHTJMÄ** eht́mä:ehti
* Yaml: **V-ehtjmae**

* **LEXICON V_86JAHTJMA/EHTJMÄ** eht́mä:eh%{tt́%}

* **LEXICON V_86TOL1MA** jaht́ma:ˋjah%{tØ%}i
* Yaml: **jahtjma**
* **LEXICON V_86TIK1MÄ** eht́mä:ehti
* Yaml: **V-ehtjmae**

* **LEXICON V_86TOL1MA/TIK1MÄ** eht́mä:eh%{tt́%}

* **LEXICON V_87KOSIMA** kosima:ko%{sØ%}si
* Yaml: **V-kosima**
* **LEXICON V_87KERIMAE** kerimä:keri
* Yaml: **V-kerimae**

* **LEXICON V_87KOSIMA/KERIMAE** kosima:kosi

* LEXICON V_88SIBAHAMA  sibama:siba
* Yaml: **V-sibama88,sibahama**
* Yaml: **V-juevaemae88**
* LEXICON V_88SIBAHAMA/JUEVAEHAEMAE  sibama:siba

### SETS BY CONSONANT QUALITY

* : Harm_Neutr_ACT_IND_PRS_SG2_USUALLY-STRONG ;  kaota
+Act+Ind+Prs+Sg2, +Err/Dial+Act+Ind+Prs+Sg2, 
+Act+Ind+Prs+Pl1, +Act+Ind+Prs+Pl2

* : ACT_IND_PRS_3_s/sEq ;  
+Act+Ind+Prs+Sg3, +Act+Ind+Prs+Pl3

### INDICATIVE PRESENT ACTIVE CONJUGATION

* +Ind+Prs+Neg:%-%{XV%}iq K ;  This gives stress
* +Err/Orth-no-q+Ind+Prs+Neg:%-iq K ;  This gives stress
* +Err/Orth-no-q+Ind+Prs+Neg:%-%{XV%}i K ;  more neutral without q
* +Err/Orth-no-q+Ind+Prs+Neg:%-i K ;  more neutral without q

### JUS
* LEXICON ACT_JUS_guq  regardless of harmony this is back 

CHECK THIS

### PASSIVE INDICATIVE PRESENT CONJUGATION

* LEXICON Harm_Neutr_JUVVA_PSS_IND_PRS  juvva süvvä

* LEXICON Harm_Neutr_JUVVA_PSS_IND_PRT_1/2  juvvi süvvi

### INDICATIVE PRETERIT SUBJECT CONJUGATION

### PASSIVE INDICATIVE PRETERIT CONJUGATION

* +Err/Orth-no-q+Pss+PrfPrc+Pl+Nom:%>tt%{uü%} K ;  no q
* +Err/Orth-no-q+Pss+PrfPrc+Pl+Nom:%>t%{uü%} K ;  no q
* +Err/Orth-no-q+Pss+PrfPrc+Pl+Nom:%>d%{uü%} K ;  no q

### NON-FINITES

* +Err/Orth-no-q+Inf:%>d%{aä%} K ;  no q

* +Err/Orth-no-q+Inf:%>i%{aä%} K ;  no q

* +Err/Orth-no-q+Inf:%>%{aä%} K ;  no q

* +Err/Orth-no-q+Inf:%>t%{aä%} K ;  no q

* +Err/Orth-no-q+Inf: K ;  no q

* **+Der/JA+N:%>j NMN_9KIPWN1/ELLAEI ;** This should have a +Der/JA tag

* +Err/Dial+Act+PrsPrc+Pl+Nom:%>v%{aä%} K ;  no q

* LEXICON ACT-PRFPRC-OBL_nU  only oblique cases and Pl+Nom

PASSIVE DISTRIBUTION
* Harm_Neutr_NÕSTMA-PSS_IND_PRS_dA ;  +Pss+Ind+Prs+Sg1: sõidõda
* Harm_Neutr_KAOTAMA-PSS_PRFPRC_t ;  +Pss+PrfPrc+Sg+Nom: kaotõt

* PSS_PRSPRC_dAv ;  +Pss+PrsPrc+Sg+Nom: kaotõdav
* Harm_Neutr_KAOTAMA-PSS_PRFPRC_t ;  +Pss+PrfPrc+Sg+Nom: kaotõt

* +Err/Dial+Pss+Ind+Prs+Sg2:%>t%{aä%}d%{eõ%} K ;  no q
* +Err/Dial+Pss+Ind+Prs+Pl1:%>t%{aä%}mi K ;  no q
* +Err/Dial+Pss+Ind+Prs+Pl2:%>t%{aä%}ti K ;  no q
* +Err/Dial+Pss+Ind+Prs+Pl3:%>t%{aä%}s%{eõ%} K ;  no q

* +Err/Orth-no-q+Pss+PrsPrc+Pl+Nom:%>t%{aä%}%>v%{aä%} K ;  no q

* +Err/Orth-no-q+Pss+PrsPrc+Pl+Nom:%>d%{aä%}%>v%{aä%} K ;  no q

* +Err/Orth-no-q+Pss+PrsPrc+Pl+Nom:%>tt%{aä%}%>v%{aä%} K ;  no q

* +Err/Dial+Pss+PrfPrc+Sg+Nom:%>d%{uü%} K ; 

* +Err/Orth-no-q+Pl+Nom:%>d%{uü%} K ;  no q

* +Err/Orth-no-q+Pl+Nom:%>t%{uü%} K ;  no q

* LEXICON Harm_Neutr_ACT_PRSPRC_v_LUGWMA  lugõma:lugõ
Retain consonant and stem vowel

* +Err/Orth-no-q+Act+PrsPrc+Pl+Nom:%>v%{aä%} K ;  no q

* +Err/Orth-no-q+Act+PrfPrc:%>n%{uü%} K ;  no q

* +Err/Orth-no-q+Pss+PrsPrc+Pl+Nom:%>t%{aä%}%>v%{aä%} K ;  no q

* +Err/Orth-no-q+Pss+PrsPrc+Pl+Nom:%>t%{aä%}%>v%{aä%} K ;  no q

* * *

<small>This (part of) documentation was generated from [src/fst/affixes/verbs.lexc](https://github.com/giellalt/lang-vro/blob/main/src/fst/affixes/verbs.lexc)</small>

---

Clitics in Võro

* * *

<small>This (part of) documentation was generated from [src/fst/clitics.lexc](https://github.com/giellalt/lang-vro/blob/main/src/fst/clitics.lexc)</small>

---

# The Võro morphophonological/twolc rules file 

This file documents the [phonology.twolc file](http://github.com/giellalt/lang-vro/blob/main/src/fst/phonology.twolc) 

## Special letters
* **u̬** u plus U+032C COMBINING CARON BELOW
* **U̬** u plus U+032C COMBINING CARON BELOW
* **ü̬** ü plus U+032C COMBINING CARON BELOW
* **Ü̬** ü plus U+032C COMBINING CARON BELOW
* **i̬** i plus U+032C COMBINING CARON BELOW
* **I̬** i plus U+032C COMBINING CARON BELOW
* **õ̭** õ plus U+032D COMBINING CIRCUMFLEX ACCENT BELOW
* **Õ̭** õ plus U+032D COMBINING CIRCUMFLEX ACCENT BELOW
* **ˋ** U+02CB MODIFIER LETTER GRAVE ACCENT other parts of stem
```%{ˋØ%}:0 — U+02CB MODIFIER LETTER GRAVE ACCENT used in rules```
**ˋ:0** — U+02CB MODIFIER LETTER GRAVE ACCENT used outside of rules, this is temporary removal 2017-04-20

## Vowel harmony with "(t)a/ä"
```
 %{aä%}:0    — Vowel harmony with "(t)a/ä" AÄ1:a AÄ1:ä AÄ1:0
 %{ae%}:a   — Vowel harmony with "a/e/õ" passive tahetu
 %{aõ%}:a   — Vowel harmony with "a/e/õ" passive sõidõtu
 %{äe%}:ä    — Vowel harmony with "ä/e/õ" passive
 %{eõ%}:0    — Vowel harmony with "e/õ"
 %{uü%}:0    — Vowel harmony with "u/ü"
 %{öü%}:ö    — Vowel raising
 %{ou%}:o    — Vowel raising
 %{ei%}:e    — Vowel raising
 %{õy%}:õ    — Vowel raising
 %{ao%}:a    — Vowel raising

 %{eØ%}:e    — ütlemä:üt%{eØ%}l  
 %{õØ%}:õ    — ütlemä:üt%{eØ%}l  
 %{Øõ%}:0    — juurdlõma:juur%{dØ%}%{0õ%}l

 %{dØ%}:d    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{dv%}:d    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{dn%}:d    — HJK and KimmoK ideas lammas:lam%{bm%}a%{sØ%}
 %{dl%}:d    — HJK and KimmoK ideas lammas:lam%{bm%}a%{sØ%}

 %{ij%}:i    ellä%{ij%}
 %{gv%}:g    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{gl%}:g    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{gØ%}:g    — HJK and KimmoK ideas argnõma:ar%{gØ%}
 %{uv%}:u    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{üv%}:ü    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{hØ%}:h    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{jØ%}:j    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{kØ%}:k    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{lØ%}:l    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{mØ%}:m    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{nØ%}:n    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{pØ%}:p    — HJK and KimmoK ideas oppama:o%{pØ%}pama
 %{rØ%}:r    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{sØ%}:s    — HJK and KimmoK ideas närväs:när%{bv%}ä%{sØ%}
 %{vØ%}:v    — HJK and KimmoK ideas kana:ka%{nØ%}na

 %{pØ%}:0    — häbü:häbü+N:hä%{pØ%}%{pbØ%}ü
 %{tØ%}:0    — koda:ko%{tØ%}%{tdØ%}a
 %{kØ%}:0    — nägo:nä%{kØ%}%{kgØ%}o

 %{bv%}:b    — HJK and KimmoK ideas närväs:när%{bv%}ä%{sØ%}
 %{dr%}:d    — HJK and KimmoK ideas parras:par%{dr%}a%{sØ%}
 %{bm%}:b    — HJK and KimmoK ideas lammas:lam%{bm%}a%{sØ%}
 %{pb%}:p    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{pb%}:b    — HJK and KimmoK ideas kana:ka%{nØ%}na

 %{tØ%}:t    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{t́Ø%}:t    — HJK and KimmoK ideas jaht́lõma:jah%{t́Ø%}%{eØ%}%{lĺ%}
 %{td%}:t    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{t́d́%}:t́    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{kg%}:k    — HJK and KimmoK ideas kaigas:kai%{kg%}as

 %{pbØ%}:p   — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{pbØ%}:b   — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{pbØ%}:0   — HJK and KimmoK ideas kana:ka%{nØ%}na

 %{pbv%}:p   %{pbv%}:b   %{pbv%}:v   — tõbi: tõvõ tõpõ tõppõ

 %{tdØ%}:d   — HJK and KimmoK ideas kana:ka%{nØ%}na

 %{kgØ%}:k   — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{kgØ%}:g   — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{kgØ%}:0   — HJK and KimmoK ideas kana:ka%{nØ%}na

 %{jiØ%}:i   — HJK and KimmoK ideas vari:var%{jiØ%}o
 %{qmn%}:q   — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{qn%}:q    — HJK and KimmoK ideas kana:ka%{nØ%}na

 %{dd́Ø%}:d   
 %{dd́n%}:d   
 %{dd́r%}:d   
 %{dd́v%}:d   
 %{dd́Ø%}:d   
 %{gǵv%}:g   
 %{gǵØ%}:g   
 %{kḱg%}:k    %{kḱg%}:ḱ    %{kḱg%}:g   
 %{kḱØ%}:k   
 %{pṕb%}:p   %{pṕb%}:ṕ    %{pṕb%}:b   
 %{tt́d%}:t    %{tt́d%}:t́    %{tt́d%}:d   
 %{tt́Ø%}:t    täh%{tt́Ø%}
 %{pṕØ%}:p   

```

## Palatalization of consonants
```
 %{bb́%}:b    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{cć%}:c    — HJK and KimmoK ideas Isaać:Isaa%{cć%}:ci
 %{dd́%}:d    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{ff́%}:f    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{gǵ%}:g    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{hh́%}:h    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{kḱ%}:k    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{lĺ%}:l     — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{lĺ%}:ĺ     — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{mḿ%}:m    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{nń%}:n    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{pṕ%}:p    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{rŕ%}:r    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{sś%}:s    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{sś%}:ś    — HJK and KimmoK ideas vaśma:va%{sØ%}%{sś%}
 %{tt́%}:t    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{vv́%}:v    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{ḱǵj%}:ḱ   — HJK and KimmoK ideas laǵa:la%{ḱǵj%}a
 %{zź%}:z    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{dd́n%}:d 
```

## Miscellaneous other symbols
```
 %{XV%}:0    — This is used for echoing the previous vowel
 %{XC%}:0    — This is used for lengthening a consonant
 %^I7:0      — This appears in stem vaoma:va%^I7o for vaio
 %^K7:0      — This appears in stem väemä:vä%^K7e for väkeq
 %^V7:0      — This appears in stem häömä:hä%^V7ö for hävvü
 %^T7:0      — This appears in stem kaoma:ka%^T7o for katoq
 %^Y7:õ      — This appears for syna = s%^Y7na and is rendered as õ in the norm
```

## Triggers
```
   %^OO2Õ:0    — joo%^OO2Õ%>i:j0õ0%>i
   %^CC2C:0    — att%^CC2C%>m%{aä%} atma
 %^PSS:0       vowel in passive tahetu, sõidõtu, eletü
 %^ÄI2ÄÄ:0    — päiv%^ÄI2ÄÄ%>ä: päävä
 %{front%}:0    — front harmony
 %{back%}:0    — back harmony
%^ErrorBack:0  — +Err/Orth+Clt:%>kinaq in front harmony context BHARM disallowance
 %{PrsSg1%}:0  — this helps with %{eõ%}:i̬
```

```

 %{td%}:t 	 HJK and KimmoK ideas kana:ka%{nØ%}na
 %{kg%}:k 	 HJK and KimmoK ideas kaigas:kai%{kg%}as

 %{qmn%}:q 	 HJK and KimmoK ideas kana:ka%{nØ%}na
 %{qn%}:q 	 HJK and KimmoK ideas kana:ka%{nØ%}na
 %{XV%}:0		 This is used for echoing the previous vowel
 %{XC%}:0	 This is used for lengthening a consonant
 %^I7:0          This appears in stem vaoma:va%^I7o for vaio
 %^K7:0           This appears in stem väemä:vä%^K7e for väkeq
 %^V7:0          This appears in stem häömä:hä%^V7ö for hävvü
 %^T7:0          This appears in stem kaoma:ka%^T7o for katoq

**%^Y7:õ  **  This appears for syna = s%^Y7na and is rendered as õ in the norm
```

```
%^NoGrad:0     — This will be placed after a stem to break Gradation
%^APOCH:0      — This causes apochope: puhksama vs puhastaq
%^StrD2T:0     — This changes g,d,b => k,t,p

%^G1:0	       — This is used with %{pØ%} %{pbØ%} for 0 0, also t, k
%^G2:0	       — This is used with %{pØ%} %{pbØ%} for 0 b, also t, k
%^G3:0	       — This is used with %{pØ%} %{pbØ%} for 0 p, also t, k
%^G4:0	       — This is used with %{pØ%} %{pbØ%} for p p, also t, k

%^WGStem:0     — This weakens "kipõń" to "kibõna", "ompel" to "ommel"
%^StrGStem:0   — This strengthens "perädü" to "perätüt"
%^ShortGStem:0   — This shortens "pu%{tØ%}tu" to "putma", an orthographic convension
%^LongGStem:0     — This lengthens "pu%{tØ%}tu" to "puttuq"

%^Pen:0        — This moves us to penultimate coda
%^PAL:0	       — Palatalization
%^NoPAL:0	       — NoPalatalization

%^JI20:0	       — in vari: vaŕo
%^JI2I:0	       — in vari vari
%^JI2J:0	       — in vari: varjo

%^PenWGStem:0  — This weakens "kipõń" to "kibõna"
%^PenVowRM:0   — syncope tapõld : taplõma 
%^D2S:0        — The ti => si
%^TS2S:0       — The -ts- => -s-
%^I2J:0        — The i => j change
%^PLPRT:0      — The a:o attested in Plural kana:kanno and prt
%^VOWRaise:0   — Raises vowel
%^VOWLower:0   — Lowers vowel
%^XLowerVow:0  — Lowers vowel two levels
%^VOWLowerDelab:0   — Lowers vowel and delabializes it
%^XLowerVowDelab:0  — Lowers vowel two levels and delabializes it
%^U2E:0        — lowers u:õ and ü:e delabializes and lowers
%^U2A:0        — lowers u:a and ü:ä delabializes and lowers
%^VowRM:0      — this will remove stem final vowel
%^CnsRM:0      — this will remove stem final consonant tervüs:tervü
```

Onset consonant or word boundary

* *füüsi{kg}a{back}^Pen^StrGStem^VowRM>i>dõ*
* *füüsik00000>i>dõ*

Right context for gradation

# Rules

## VOWEL HARMONY 
### Vowel harmony suffixes Front
**%{aä%}:a**

**%{aä%}:ä**

**%{uü%}:u**

**%{uü%}:ü**

**%{eõ%}:õ**

**%{eõ%}:e**

**%{ae%}:e**
tahtma+V+Pss+PrfPrc+Sg+Nom: **want/haluta**
* *tah{tt́Ø}{ae}{back}^Pen^VOWLower^Pen^WGStem>{eõ}>t{uü}*
* *tah0e00000>0>tu*

**%{aõ%}:õ**

**%{äe%}:e**

### VOWEL LOWERING

**u:o**
* *lugõ%{back%}%^Pen%^VOWLower%^Pen%^WGStem%^VowRM%>i*
* *lo00000000%>i*

**ü:ö**
* *pü{kgØ}ä{front}^Pen^VOWLower^Pen^WGStem^VowRM>e>t*
* *pö00000000>e>t*
* *süü%{front%}%^VOWLower%^WGStem%>nüq*
* *söö000%>nüq*

**o2õ**
* *joo%{back%}%^OO2Õ%>i*
* *jõ000%>i*
* *aigo%{back%}%^OO2Õ*
* *aigõ00*

**u2õ**
* *laulu%{back%}%^OO2Õ*
* *laulõ00*

**ö2e**
* *söö%{front%}%^OO2Õ%>i*
* *se000%>i*

**Delabializing o and ö**

### VOWEL RAISING
**Delabializing o and ö**

### PALATALIZATION
**n2ń palatalization all**
kestmä+V+Act+Ind+Prt+Sg3:
* *kes{tt́}{äe}{front}^Pen^PAL^VowRM*
* *kest́00000*

akaŕ+A+Sg+Nom
* *a%{kg%}a%{rŕ%}%{back%}%^Pen%^G2%^PAL*
* *akaŕ0000*

asi+N+Sg+Gen:
* *a%{sś%}%{jiØ%}%{back%}%^PAL%^VowRM%>%{aä%}*
* *aś0000%>a*

alostama+V+Act+Ind+Prt+Sg3:
* *alos{tt́}a^Pen^VOWRaise^Pen^PAL^VowRM*
* *alost́000000*

**%{kḱ%}:ḱ**
kakma
* *ka%{kØ%}%{kḱ%}u%{back%}^Pen^VOWRaise^Pen^G4^Pen^PAL%^VowRM*
* *kakḱ000000000*
* *ka{kØ}{kḱ}u{back}^Pen^VOWRaise^Pen^G3^Pen^NoPAL^VowRM>n{uü}q*
* *ka0k000000000>nuq*

**n2n no palatalization all**

rehksämä+V+Inf/mA:
* *reh{kØ}ä{sś}{front}^Pen^StrGStem^Pen^VowRM^NoPAL>{aä}>m{aä}*
* *rehk0s000000>ä>mä*
hanǵ+N+Sg+Gen: **snow pack/hanki**
* *han{gǵ}{back}^NoPAL>%{eõ%}*
* *hang000>e*

**{dd́n}:d́ palatalization for 3-way**

särǵ+N+Sg+Nom: **roach/särki**
* *sär{gǵØ}{front}^StrGStem^PAL*
* *särǵ000*
andma+V+Act+Ind+Prs+Sg3
* *an%{dd́n%}%{back%}%^PAL*
* *and́00*

**{dd́n}:n weaken 3-way**

andma+V+Act+Ind+Prs+Sg1
* *an%{dd́n%}%{back%}%^WGStem%>m%{aä%}*
* *ann00%>ma*

püüdmä+V+Act+Ind+Prs+Sg1
* *pü%{üv%}%{dd́v%}%{front%}%^WGStem%>%{aä%}*
* *püvv00%>ä*

**%{dd́v%}:v**

**%{pṕb%}:p**
loroṕ+N+Sg+Par:
* *loro{pṕb}{back}^StrGStem^NoPAL>i*
* *lorop000>i*

**%{tt́d%}:t**

hainatama+V+Inf/mA
* *haina{tt́d}a{back}^Pen^VOWRaise^Pen^StrGStem>m{aä}*
* *hainata00000>ma*

**%{kḱg%}:k**
* *pisla%{kḱg%}%{back%}%^G2%>*
* *pislaḱ00%>*

**%{pṕb%}:ṕ**
loroṕ
* *loro{pṕb}{back}^StrGStem^PAL*
* *loroṕ000*

**%{tt́d%}:t́**

**%{kḱg%}:ḱ**
* *pisla%{kḱg%}%{back%}%^StrGStem%^PAL*
* *pislaḱ000*

kõiḱ+Pron+Sg+Nom
* *kõ̭i%{kØ%}%{kḱg%}%{back%}%^CC2C%^PAL*
* *kõ̭i0ḱ000*

### VOWEL CHANGE WITH PLURAL

tegemä+V+Act+Ind+Prs+Sg1: **do**
* *teg%{front%}%^WGStem%>%{eõ%}*
* *ti̬000%>i̬*

* *k%{ei%}%{ei%}%{lĺ%}%{front%}%^VOWRaise%^PAL*
* *ki̬i̬ĺ000*

**õ2õ̭**
* *sõda%{back%}%^WGStem*
* *sõ̭0a00*

**o2u̬**

**Vx%{ou%}:Vyo**

hoolas+A+Sg+Nom:
* *h%{ou%}%{ou%}la%{sØ%}%{back%}%^Pen%^VOWLower%^Pen%^G1*
* *hoolas00000*
Toomas+N+Prop+Sg+Nom
* *T{ou}{ou}ma{sØ}{back}^Pen^VOWLower^Pen^WGStem^StrGStem*
* *Toomas000000*

**Vx%{ou%}2Vyu̬**
nuuĺ+N+Sg+Nom: **arrow**
* *n%{ou%}%{ou%}%{lĺ%}%{back%}%^VOWRaise%^PAL*
* *nu̬u̬ĺ000*
juuma+V+Pss+Cond+ConNegI: **drink/juoda**
* *j{ou}{ou}{back}^VOWRaise^VowRM>vv{aä}>siq*
* *ju̬0000>vva>siq*

kiiĺ+N+Sg+Gen: **tongue/kieli**
* *k%{ei%}%{ei%}{lĺ}%{front%}%^VOWRaise%^PAL*
* *ki̬i̬ĺ000*
* *k%{ei%}%{ei%}r%{dØ%}%{eØ%}%{lĺ%}%{front%}%^Pen%^VOWRaise%^Pen%^VowRM%>%{eõ%}%>m%{aä%}*
* *ki̬i̬rd0l00000%>e%>mä*

**i2e**
pini+N+Pl+Par: **dog/koira**
* *pi%{nØ%}ni%{front%}%^Pen%^StrGStem%^VowRM%>%{eõ%}*
* *pinn00000%>e*
kiiĺ+N+Sg+Gen: **tongue/kieli**
* *k%{ei%}%{ei%}{lĺ}%{front%}%^VOWLower%^NoPAL%>%{eõ%}*
* *keel000%>e*
leib+N+Sg+Gen: **bread/leipä**
* *lei{bv}{front}^ÄI2ÄÄ^WGStem>{aä}*
* *leev000>ä*
* *pi%{tdØ%}ä%{front%}%^Pen%^VOWLower%^Pen%^WGStem%^VowRM%{eõ%}%>t%{aä%}s*
* *pe00000000e%>täs*

**i:ä**
päiv+N+Sg+Gen: **day/päivä**
* *päiv%{front%}%^ÄI2ÄÄ%>ä*
* *pääv00%>ä*

**a2o**
```
* *ka%{nØ%}na%{back%}%^Pen%^StrGStem%^PLPRT*
* *kanno0000*
```

**{ao}o**
```
* *ka%{nØ%}n%{ao%}%{back%}%^G3%^PLPRT*
* *kanno000*
```

### VOWEL LOSS
**a:0**
      a _ (HarmDummiesVar) %>  i  ;  
* *saa%{back%}%>i*
* *sa00%>i*
sõimama+V+Act+Ind+Prt+Sg1
* *sõima%{back%}%^Pen%^VOWLower%^Pen%^WGStem%^VowRM%>ssi*
* *sõim0000000%>ssi*
* *puhkas%{back%}%^Pen%^VowRM%>a%>ma*
* *puhk0s000%>a%>ma*
võtma+V+Inf/mA: **to take/ottaa**
* *võ{tØ}{tt́}a{back}^Pen^WGStem^Pen^NoPAL^VowRM>m{aä}*
* *võ0t0000000>ma*
võtma+V+Ind+Prt+Sg3: **to take/ottaa**
* *võ{tØ}{tt́}a{back}^Pen^StrGStem^Pen^PAL^VowRM*
* *võtt́0000000*

sõda+N+Pl+Par:
* *sõ%{tØ%}%{tdØ%}a%{back%}%^Pen%^G3%^VowRM%>o*
* *sõ0t00000%>o*

**ä:0**
pügämä+V+Pss+PrfPrc:
* *pü%{kgØ%}ä%{front%}%^Pen%^VOWLower%^Pen%^WGStem%^VowRM%{eõ%}%>t*
* *pö00000000e%>t*
rehksämä+V+Inf/mA:
* *reh{kØ}ä{sś}{front}^Pen^StrGStem^Pen^VowRM^NoPAL>{aä}>m{aä}*
* *rehkäs000000>ä>mä*

* *jää%{front%}%^VOWRaise%^VowRM%>i*
* *jä0000%>i*
* *elä%{front%}%>et*
* *el00%>et*
tütär+N+Sg+Gen
* *tütä%{rŕ%}%{front%}%^VowRM%>e*
* *tüt0r000%>e*

**U:0 Vx**
```
* *hirnu{back}^Pen^CC2C^VowRM>m{aä}*
* *hirn00000>ma*
* *kut{sś}u{back}^Pen^VOWRaise^Pen^PAL^VowRM*
* *kutś0000000*
* *tervüs{front}^VowRM^CnsRM>i>t*
* *terv00000>i>t*
juusk+N+Sg+Nom: ____
* *j{ou}{ou}s{kØ}u{back}^VOWRaise^VowRM*
* *ju̬u̬sk0000*

* *kuu{back}^VOWLower^VowRM>i>d*
* *ku0000>i>d*
```

[ Cns: |ArchCns:| Vow: ] _ (s:) (HarmDummiesVar) [(%^Pen: %^CC2C:|%^Pen: %^G3:|%^Pen: %^G4:|PenVOWHite %^Pen: %^G1:) %^VowRM: ]( CnsInZero: (%^Pen: %^CC2C:) %^VowRM: %^CnsRM: )  ; 
* *tüü%{front%}%^VowRM%>hüq*
* *tü000%>hüq*
* *tervüs%{front%}%^VowRM%^WGStem%>i%>t*
* *terv00000%>i%>t*

**e:0**
* *herne%{hØ%}%{front%}%^VowRM%^WGStem%>id%{eõ%}*
* *hern00000%>ide*
läteq+N+Pl?Gen: **spring/lähde**
* *lä{tØ}te{front}^Pen^VOWRaise^Pen^StrGStem^VowRM>id{eõ}*
* *lätt0000000>ide*

**o:0**
juuma+V+Inf
* *j{ou}{ou}{back}^VOWRaise^VowRM>vv>{aä}q*
* *ju̬0000>vv>aq*

**Vx%{ou%}:0**
juuma+V+Inf
* *j{ou}{ou}{back}^VOWRaise^VowRM>vv>{aä}q*
* *ju̬0000>vv>aq*

**Vx%{äe%}:0 Passive stem vowel**
nõstma+V+Inf/mA
* *nõs{tt́}{aõ}{back}^Pen^NoPAL^VowRM>m{aä}*
* *nõst00000>ma*
kestmä+V+Act+Ind+Prt+Sg3:
* *kes{tt́}{äe}{front}^Pen^PAL^VowRM*
* *kest́00000*

**ö:0**

**i:0**
hüdsi+N+Sg+Par:
* *hüdsi%{front%}%^TS2S%^VowRM%>t*
* *hü0s0000%>t*
* *aigo%{back%}%^Pen%^WGStem*
* *a00o000*

**õ:0**
* *tapõl{back}^Pen^VowRMõ>m{aä}*
* *tap0l000õ>ma*
* *kan%{dn%}õ%{lĺ%}{back}^StrGStem^Pen^VowRM>õ*
* *kand0l0000>õ*
kogõr+N
* *ko%{kg%}õr{back}^StrGStem^Pen^VowRM>õ*
* *kok0r0000>õ*
hamõq+N+Pl+Ill
* *ha%{mØ%}mõ%{back%}%^Pen%^VOWRaise%^Pen%^StrGStem%^VowRM%>ihe*
* *ha0m0000000%>ihe*

**%{eØ%}: 0**

**%{õØ%}: 0**

VOWEL LENGTHENING

**%{XV%}:u**

**%{XV%}:ü**

**%{XV%}:o**
* *taso%{back%}%-%{XV%}iq*
* *taso0%-oiq*

**%{XV%}:a**

**%{XV%}:ä**

**%{XV%}:õ**
kannõĺ+N+Sg+Gen: **kantele**
* *kan%{dn%}õ%{lĺ%}%{back%}%^Pen%^StrGStem%^Pen%^VowRM%^NoPAL%>%{XV%}*
* *kand0l0000%>õ*
**%{XV%}:e**
käskmä+V+Act+Ind+Prs+Neg **command/käskeä**
* *käs%{kØ%}%{front%}%^WGStem%>%{eõ%}%-%{XV%}iq*
* *käs000%>e%-eiq*

**%{XV%}:i**

**i2j**
* *asi%{back%}%^I2J%>a*
* *asj00%>a*
elläi+N+Sg+Gen
* *e{lØ}lä{ij}{front}^Pen^WGStem^I2J>{aä}*
* *e0läj0000>ä*

**%{ij%}:j**

**%{jiØ%}:j**

**%{jiØ%}:i**
* *ki{rŕ}{jiØ}{front}^NoPAL^JI2I*
* *kiri000*

**%{jiØ%}:0**
vari+N+Sg+Gen: **shadow/varjo**
* *va%{rŕ%}%{jiØ%}o%{back%}%^Pen%^PAL%^Pen%^WGStem*
* *vaŕ0o00000*

**%{jØ%}:0**
vari+N+Sg+Gen: **shadow/varjo**
* *va%{rŕ%}%{jiØ%}o%{back%}%^Pen%^PAL%^Pen%^WGStem*
* *vaŕ0o00000*

**u2v** depricate to "%{uv%}:v"

**%{uv%}:v**
* *lu{uv}{dv}{back}^WGStem>{aä}*
* *luvv00>a*
joudma+V+Act+Ind+Prt+Sg1
* *jõ%{uv%}%{dd́v%}%{back%}%^WGStem%>i*
* *jõvv00%>i*
* *la{uv}{dv}{back}^WGStem>{aä}*
* *lavv00>a*

**{üv}:v**
* *pü{üv}{dd́v}{front}^WGStem>et*
* *püvv00>et*
* *sü{üv}{dv}{front}^WGStem>ä*
* *süvv00>ä*

*  examples:*

*  examples:*

**%^I7:i**
* *va%^I7o%^StrGStem%>i*
* *vaio0%>0*

**%^I7:i**

CONSONANT
**%{pṕØ%}:ṕ**
* *pap%{pṕØ%}%{back%}%^G2%^PAL*
* *papṕ000*

**%{tt́Ø%}:t́ **
* *täh%{tt́Ø%}%{front%}%^StrGStem%^PAL*
* *täht́000*
* *võ{tØ}{tt́Ø}a{back}^Pen^StrGStem^Pen^PAL^VowRM*
* *võtt́0000000*

**%{tt́Ø%}:t **

täht́+N+Err/Orth-no-pal+Sg+Nom: __star/tähti__
* *täh{tt́Ø}{front}^StrGStem^NoPAL*
* *täht000*
võtma+V+Act+Ind+Prt+Pl3
* *võ{tØ}{tt́Ø}a{back}^Pen^G3^Pen^NoPAL^VowRM>iq*
* *võ0t0000000>iq*
* *hoi{tt́Ø}{back}^VOWRaise^StrGStem^NoPAL>aq*
* *hoit00000>aq*

**%{kḱØ%}:ḱ**

SECONDARY CONSONANT LENGTHENING

**%{pØ%}:p**
```
* *hä%{pØ%}%{pbØ%}ü%{front%}%^Pen%^G4*
* *häppü000*
* *tõ%{pØ%}%{pbv%}%{back%}%^G4%>%{eõ%}*
* *tõpp00%>õ*
* *se%{pØ%}p%{front%}%^StrGStem*
* *sepp00*
* *nu%{pØ%}pu%{back%}%^Pen%^VOWRaise%^Pen%^StrGStem%^VowRM*
* *nupp0000000*
```

**{tØ}:t**
* *sõ%{tØ%}da%{back%}%^G4%^PLPRT*
* *sõtto000*
* *si%{tØ%}t%{front%}%^StrGStem*
* *sitt00*
* *ü%{tØ%}te%{front%}%^Pen%^StrGStem*
* *ütte000*
* *mü%{tØ%}tü%{front%}%^Pen%^VOWRaise%^Pen%^StrGStem%^VowRM*
* *mütt0000000*
sõda+N+Sg+Ill:
* *sõ%{tØ%}%{tdØ%}a%{back%}%^Pen%^G3*
* *sõtta000*
* *uh{tØ}a{sś}{back}^Pen^StrGStem^Pen^VowRM^NoPAL>{aä}>m{aä}*
* *uht0s000000>a>ma*
* *unõh{tØ}u{back}^Pen^StrGStem*
* *unõhtu000*

**%{t́Ø%}:t́**

**%{Øk%}:k**
igä+N+Sg+Ill
* *i{kØ}{kgØ}ä{front}^Pen^G4*
* *ikkä00*
* *mä%{Øk%}%{kgØ%}%{front%}%^G4%>%{eõ%}*
* *mäkk00%>e*

**%{XC%}:s**

**%{XC%}:l**

**%{XC%}:ĺ**

**%{XC%}:k**

**%{cć%}:ć**

**%{cć%}:c**

### Consonant weakening 

**kToZero**  
* *puhkas%{back%}%^WGStem%>taq*
* *puh0as00%>taq*

* *ikkõ%{back%}%^Pen%^CC2C%^VowRM%>m%{aä%}*
* *ik000000%>ma*

**%{pṕØ%}:0**  

**%{tt́Ø%}:0**  
* *võ{tØ}{tt́Ø}a^Pen^G1^Pen^NoPAL^VowRM>eti*
* *võ00000000>eti*

**%{kḱØ%}:0**  

* *j{ou}{ou}s{kḱØ}{back}^VOWLower^WGStem>{eõ}*
* *joos0000>õ*
* ★*j{ou}{ou}s{kḱØ}{back}^VOWLower^WGStem>{eõ}* (is not standard language)
* ★*joosk000>õ* (is not standard language)

**%{sØ%}:0**  

* *su%{sØ%}śo%{back%}%^Pen%^WGStem*
* *su0śo000*
vaśma+V+Inf/mA: **answer/vastata**
* *va{sØ}{sś}{back}^VOWRaise^WGStem^PAL>m{aä}*
* *va0ś0000>ma*
* *ham%{bm%}a%{sØ%}%{back%}%^Pen%^VOWRaise%^Pen%^StrGStem%^WGStem*
* *hamba0000000*

* *rahva{sØ}{back}^VowRM^WGStem>id{eõ}*
* *rahv00000>idõ*

**%{vØ%}:0**  
kruv́ma+V+Inf/mA
* *kru{vØ}{vv́}{back}^VOWRaise^WGStem^PAL>m{aä}*
* *kru0v́0000>ma*

**%{rØ%}:0**  
* *a%{rØ%}ro%{back%}%^Pen%^G2*
* *a0ro000*

**%{nØ%}:0**  
* *su%{nØ%}ńo%{back%}%^Pen%^WGStem*
* *su0ńo000*
* *va{nØ}{nń}u{back}^Pen^VOWRaise^Pen^CC2C^Pen^NoPAL^VowRM>m{aä}*
* *va0n000000000>m{aä}*

**%{lØ%}:0**  
* *ta%{lØ%}lo%{back%}%^Pen%^WGStem*
* *ta0lo000*

**%{mØ%}:0**  
* *su%{sØ%}śo%{back%}%^Pen%^WGStem*
* *su0śo000*

**%{kØ%}:0**  
* *puh%{kØ%}as%{back%}%^WGStem%>taq*
* *puh0as00%>taq*
* *vis%{kØ%}a%{back%}%^WGStem%>aq*
* *vis0a00%>aq*

nätsk+A+Sg+Gen
* *nä%{td%}s%{kØ%}%{front%}%^G1%>%{aä%}*
* *näds000%>ä*

* *eläni{kØ}{kg}{front}^G3*
* *eläni0k00*
* *i%{kØ%}kõ%{back%}%^Pen%^CC2C%^VowRM%>m%{aä%}*
* *i0k00000%>ma*

kakma:
* *ka%{kØ%}%{kḱ%}u%{back%}%^Pen%^CC2C%^VowRM%>m%{aä%}*
* *ka0k00000%>ma*

kõiḱ+Pron+Sg+Nom
* *kõi%{kØ%}%{kḱg%}%{back%}%^CC2C%^PAL*
* *kõi0ḱ000*
* *ri%{kØ%}ka%{sØ%}%{back%}%^Pen%^VOWLower%^Pen%^WGStem*
* *ri0kas00000*
jõgi+N+Sg+Gen: **river/joki**
* *jõ%{kØ%}%{kgØ%}%{back%}%^G1%>%{eõ%}*
* *jõ0000%>õ*

**pToZero**
* *tapp%{back%}%^CC2C%>m%{aä%}*
* *tap000%>ma*

**%{pØ%}:0**
* *se%{pØ%}p%{front%}%^WGStem*
* *se0p00*

* *tap%{pØ%}%{back%}%^CC2C%>m%{aä%}*
* *tap000%>ma*

**XØToZero**
agras+A+Sg+Gen
* *a%{kg%}ra%{sØ%}%{back%}%^Pen%^VOWRaise%^Pen%^G2%^WGStem*
* *akra0000000*
* *ve%{rØ%}rev%{front%}%^Pen%^WGStem%>%{aä%}*
* *ve0rev000%>ä*
elläi+N+Sg+Gen
* *e{lØ}lä{ij}{front}^Pen^WGStem^I2J>{aä}*
* *e0läj0000>ä*
pereh+N+Sg+Gen: **family/perhe**
* *pe{rØ}re{hØ}{front}^Pen^StrGStem^WGStem*
* *perre00000*
hamõh+N+Sg+Nom
* *ha%{mØ%}mõ%{hØ%}%{back%}%^Pen%^VOWLower%^Pen%^WGStem%^StrGStem*
* *ha0mõh000000*

**XØToSelf**
villui+A+Sg+Nom
* *vi{lØ}lui{back}^Pen^G3*
* *villui000*

kevväi+N+Sg+Gen: **spring**
* *ke%{vØ%}vä%{ij%}%{front%}%^Pen%^WGStem%>ä*
* *ke0väj000%>ä*

**%{sØ%}:s**
ratas+N+Sg+Nom
* *ra%{tØ%}ta%{sØ%}%{back%}%^Pen%^VOWLower%^Pen%^WGStem%^StrGStem*
* *ra0tas000000*
kaardas+N+Sg+Nom
* *kaar%{dØ%}a%{sØ%}%{back%}%^Pen%^VOWLower%^Pen%^WGStem%^StrGStem*
* *kaardas000000*
agras+A+Sg+Nom
* *a%{kg%}ra%{sØ%}%{back%}%^Pen%^VOWLower%^Pen%^WGStem%^StrGStem*
* *agras000000*

**%{hØ%}:h**
hamõh+N+Sg+Nom
* *ha%{mØ%}mõ%{hØ%}%{back%}%^Pen%^VOWLower%^Pen%^WGStem%^StrGStem*
* *ha0mõh000000*

**%{kØ%}:k**
rehksämä+V+Inf/mA:
* *reh{kØ}ä{sś}{front}^Pen^StrGStem^Pen^VowRM^NoPAL>{aä}>m{aä}*
* *rehk0s000000>ä>mä*
* *as%{kØ%}o%{back%}%^Pen%^G2*
* *asko000*
* *eläni{kØ}{kg}{back}^G4>{eõ}*
* *elänikk00>e*
makḱ+N+Pl+All
* *ma{kØ}{kḱ}{back}^StrGStem^NoPAL>{eõ}>l{eõ}*
* *makk000>õ>lõ*
egä+Det+Sg+Ill:
* *e{kØ}{kg}ä{front}^Pen^G4*
* *ekkä000*
igä+N+Sg+Ill: **age/ikä**
* *i{kØ}{kgØ}ä{front}^Pen^G4*
* *ikkä000*

**%{pb%}:p**
* *kau%{pb%}%{õØ%}%{lĺ%}%{back%}%^Pen%^VOWRaise%^Pen%^StrGStem%^Pen%^VowRM%>%{eõ%}%>m%{aä%}*
* *kaup0l0000000%>õ%>ma*

* *li%{pb%}õ%{back%}%^Pen%^G2*
* *lipõ000*

**%{t́d́%}:d́**

**%{t́d́%}:t́**

**%{td%}:t**
* *lu̬u̬dusõkai{td}sõ^Pen^VOWLower^Pen^WGStem>q*
* *lu̬u̬dusõkaitsõ0000>q*
võitlõma+V+Inf/mA
* *või{td}{õØ}{lĺ}{back}^Pen^VOWRaise^Pen^StrGStem^Pen^VowRM^NoPAL>{eõ}>m{aä}*
* *võit0l00000000>õ>ma*
nätsk+A+Sg+Nom
* *nä%{td%}s%{kØ%}%{front%}%^G2*
* *nätsk00*
hõrts+N+Sg+Nom
* *hõr%{td%}so%{back%}%^Pen%^VOWRaise%^Pen%^StrGStem%^VowRM*
* *hõrts0000000*

**%{kg%}:k**
akaŕ+A+Sg+Nom
* *a%{kg%}a%{rŕ%}%{back%}%^Pen%^G2%^PAL*
* *akaŕ0000*
* *rän%{kg%}%{front%}%^G3*
* *ränk00*

* *avali{kØ}{kg}{back}^G3*
* *avali0k00*
egä+Det+Sg+Nom:
* *e{kØ}{kg}ä{front}^Pen^G2*
* *e0gä000*

**%{kg%}:g**
apteḱ+N+Sg+Gen:
* *apte{kØ}{kḱg}{back}^VOWLower^G2>i*
* *apte0g000%>i*
agras+A+Sg+Nom:
* *a%{kg%}ra%{sØ%}%{back%}%^Pen%^VOWLower%^Pen%^WGStem*
* *agras00000*
egä+Det+Sg+Nom:
* *e{kØ}{kg}ä{front}^Pen^G2*
* *e0gä000*

* *hõl%{kg%}a%{sØ%}%{back%}%^Pen%^G2*
* *hõlgas000*
* *rän%{kg%}%{front%}%^G2%{aä%}*
* *räng00ä*

nõkõś+N+Sg+Ill
* *nõ%{kg%}õ%{sś%}%{back%}%^Pen%^WGStem%{XC%}%>õ%>he*
* *nõgõs000s%>õ%>he*

* *a%{kg%}ra%{sØ%}%{back%}%^Pen%^WGStem*
* *agras000*

**%{td%}:d**

kaotama+V+Act+Ind+Prs+Sg1:
* *kao%{td%}a%{back%}%^Pen%^G2*
* *kaoda000*

**%{tt́d%}:d**
kergütämä+V+Act+Ind+Prs+Sg1:
* *kergü{tt́d}{front}^VOWRaise^WGStem^NoPAL>{aä}*
* *kergüd0000>ä*

**tToZero**
hüdsi+N+Sg+Par:
* *hüdsi%{front%}%^TS2S%^VowRM%>t*
* *hü0s0000%>t*

* *att%{back%}%^CC2C%>m%{aä%}*
* *at000%>ma*

**%{tØ%}:0**
* *puh%{tØ%}a%{sØ%}%{back%}%^Pen%^WGStem*
* *puh0as000*
ratas+N+Sg+Nom
* *ra%{tØ%}ta%{sØ%}%{back%}%^Pen%^VOWLower%^Pen%^WGStem%^StrGStem*
* *ra0tas00000*

sõda+N+Sg+Gen:
* *sõ%{tØ%}%{tdØ%}a%{back%}%^Pen%^G1*
* *sõ00a000*

**%{t́Ø%}:0**

### CONSONANT QUALITY CHANGE

**%{pṕb%}:b**
* *loro%{pṕb%}%{back%}%^G2%>i*
* *lorob00%>i*

**%{pb%}:b**
habras+A+Sg+Nom
* *ha%{pb%}ra%{sØ%}%{back%}%^Pen%^WGStem%^StrGStem*
* *habras0000*

* *ki%{pb%}õ%{nń%}%{back%}%^Pen%^WGStem%>%{aä%}*
* *kibõn000%>a*

**p2b**

**b20**

**%{pbØ%}:b**

**%{dr%}:r**
murrõq+N+Sg+Nom
* *mur%{dr%}õ%{back%}%^Pen%^VOWLower%^Pen%^WGStem%>q*
* *murrõ00000%>q*

**%{dr%}:d**
murrõq+N+Sg+Gen
* *mur%{dr%}õ%{back%}%^Pen%^VOWRaise%^Pen%^StrGStem*
* *murdõ00000*

**%{ḱǵj%}:ǵ**

**%{ḱǵj%}:ḱ**

**%{ḱǵj%}:0**

**%{tdØ%}:d**

**%{dØ%}:d**
väärdlemä+V+Inf/mA
* *väär{dØ}{eØ}{lĺ}{front}^Pen^VOWRaise^Pen^StrGStem^Pen^VowRM^NoPAL>{eõ}>m{aä}*
* *väärd0l00000000>e>mä*

kaardas+N+Sg+Nom
* *kaar%{dØ%}a%{sØ%}%{back%}%^Pen%^VOWLower%^Pen%^StrGStem%^StrGStem*
* *kaardas000000*

**%{kgØ%}:g**
jõgi+N+Sg+Nom: **river / joki**
* *jõ{kØ}{kgØ}{back}^G2>i*
* *jõ0g00>i*
lugõma+V+Act+Ind+Prs+Sg3
* *lu{kgØ}õ{back}^Pen^G2*
* *lugõ000*

**%{pbv%}:b**
* *tõ%{pØ%}%{pbv%}%{back%}%^G2i*
* *tõ0b00i*

hammas
* *ham%{bm%}a%{sØ%}%{back%}%^Pen%^WGStem*
* *hammas000*

**%{bm%}:m**
* *ham%{bm%}a%{sØ%}%{back%}%^Pen%^VOWLower%^Pen%^WGStem*
* *hammas00000*

**%{bm%}:b**
* *ham%{bm%}a%{sØ%}%^Pen%^VOWRaise%^Pen%^G2%^WGStem*
* *hamba000000*

**%{bv%}:v**
* *när%{bv%}ä%{sØ%}%{back%}%^Pen%^VOWLower%^Pen%^WGStem*
* *närväs00000*
leib+N+Sg+Gen: **bread/leipä**
* *lei{bv}{front}^ÄI2ÄÄ^WGStem>{aä}*
* *leev000>ä*

**%{dn%}:n**
kannõĺ+N+Sg+Nom: **kantele**
* *kan%{dn%}õ%{lĺ%}%{back%}%^Pen%^WGStem%^PAL*
* *kannõĺ0000*

**%{dl%}:l**
* *tul%{back%}%>%{dl%}aq%^Pen%^WGStem*
* *tul0%>laq00*
* *kõnõl%{back%}%>%{dl%}aq%^Pen%^WGStem*
* *kõnõl0%>laq00*
* *val%{dl%}%{back%}%^G1%>n*
* *vall00%>n*

**%{dv%}:v**
* *pü%{üv%}%{dv%}%{front%}%^G1%>et*
* *püvv00%>et*
* *lu{uv}{dv}{back}^WGStem>{aä}*
* *luvv00>a*
* *sü%{üv%}%{dv%}%{front%}%^G1%>ä*
* *süvv00%>ä*

__VdVToVtV__

**dTos**

**tTos**

**tTod**
kaotama+V+Act+Ind+Prs+Sg1: 
* *kaota%{back%}%^Pen%^WGStem*
* *kaoda000*

There should always be a trigger

** %{dn%}:d**

* *kan%{dn%}õl%{back%}%^Pen%^G2%^Pen%^VowRM%>õ*
* *kand0l00000%>õ*

**j2i**

**{kḱg}:g **

kõiḱ+Pron+Sg+Gen
* *kõi%{kØ%}%{kḱg%}%{back%}%^G2%^NoPAL%>%{eõ%}*
* *kõi0g00%>õ*

**k2g**
* *hõrak%{back%}%^G1%>a*
* *hõrag00%>a*
* ★*hõrak%{back%}%^G1%>a* (is not standard language)
* ★*hõrak00%>a* (is not standard language)
* *kisk%{back%}%^G1%>%{uü%}%>t%{aä%}v*
* *kis000%>u%>tav*

* *süküs%{front%}%^Pen%^WGStem%>e*
* *sügüs000%>e*

igä+N+Sg+Ill
* *i{kØ}{kgØ}ä{front}^Pen^G4*
* *ikkä00*
* *ko%{kg%}õr%{back%}%^StrGStem%^Pen%^VowRM%>õ*
* *kok0r0000%>õ*

**bTop**

**%{pbv%}:p**
* *tõ%{pØ%}%{pbv%}%{back%}%^G4%>%{eõ%}*
* *tõpp00%>e*

**%{pbØ%}:p**

**%{tdØ%}:t**

**%{kgØ%}:k**
* *mä%{kØ%}%{kgØ%}%{front%}%^G4%>%{eõ%}*
* *mäkk00%>e*

### STEM-FINAL CONSONANT LOSS
**s20**
kirotus+N+Pl+Gen:
* *kirotus%{back%}%^CnsRM%>isi*
* *kirotu000%>isi*

usś+N+Sg+Par **door**
* *uss%{back%}%^TS2S%>t*
* *us000%>t*

vaśma+V+Inf/mA
* *va{sØ}{sś}{back}^VOWRaise^WGStem^PAL>m{aä}*
* *va0ś0000>ma*

**%{bv%}:b**
närväs+A+Sg+Gen:
* *när%{bv%}ä%{sØ%}%{front%}%^Pen%^VOWLower%^Pen%^StrGStem%^WGStem*
* *närbä0000000*

**%{gØ%}:g**
liig+A+Sg+Nom:
* *lii%{gØ%}%{back%}%^StrGStem*
* *liig00*
huug

**d20**
* *hüdsi%{front%}%^TS2S%^VowRM%>te*
* *hü0s0000%>te*

**%{dØ%}:0**

**g20** deprication to {gǵØ}:0
* *aig%{back%}%^WGStem%>o*
* *a0000%>o*
argnõma+V+Inf
* *ar%{gØ%}{back}{eõ}^Pen^WGStem>d{aä}q*
* *ar00õ00>daq*

**%{gØ%}:0**
* *aig{back}^WGStem>o*
* *a0000>o*
igä+N+Sg+Gen
* *i{kØ}{kgØ}ä{front}^Pen^G1*
* *i00ä000*
lugõma+V+Pss+PrfPrc **read/lukea**
* *lu{kgØ}õ{back}^Pen^VOWLower^Pen^WGStem^VowRM>e>t*
* *lo00000000>e>t*
argnõma+V+Inf
* *ar{gØ}{back}{eõ}^Pen^WGStem>d{aä}q*
* *ar00õ00>daq*

* *palgõ%{back%}%^WGStem%>h*
* *pal0õ00%>h*

**{gǵØ}:0**
särǵ+N+Sg+Gen: **roach/särki**
* *sär{gǵØ}{front}^WGStem^NoPAL>%{eõ%}*
* *sär0000>e*

**{gǵØ}:g**
särǵ+N+Sg+Ill: **roach/särki**
* *sär{gǵØ}{front}^StrGStem^NoPAL>%{eõ%}*
* *särg000>e*

**%{pbv%}:v**
* *tõ%{pØ%}%{pbv%}%{back%}%^G1%>%{eõ%}*
* *tõ0v00%>õ*

**%{pbØ%}:0**

**%{tdØ%}:0**
* *hüdsi%{front%}%^TS2S%^VowRM%>te*
* *hü0s0000%>te*

**%{kgØ%}:0**
* *mä%{kØ%}%{kgØ%}%{front%}%^G1%>%{eõ%}*
* *mä0000%>e*

* *u%{jØ%}jo%{back%}%^Pen%^WGStem%>m%{aä%}*
* *u0jo000%>ma*

püüdmä+V+Act+Ind+Prs+Sg3
* *pü%{üv%}%{dd́v%}%{front%}%^PAL*
* *püüd́00*

pereq
* *pe%{rØ%}re%{front%}%^WGStem%>h*
* *pe0re00%>h*

naŕma
* *na%{rØ%}%{rŕ%}%{back%}%^CC2C%^PAL%>m%{aä%}*
* *na0r000%>ma*

### Other marks
* *ki%{pb%}õ%{nń%}%{back%}%>a*
* *kipõn0%>a*

**Disallow %^ErrorBack:0 in BHARM**

**Disallow %^ErrorBack:0 in BHARM**

* * *

<small>This (part of) documentation was generated from [src/fst/phonology.twolc](https://github.com/giellalt/lang-vro/blob/main/src/fst/phonology.twolc)</small>

---


# Võru tags and basic lexica

# Definitions for Multichar_Symbols

## Analysis symbols
The morphological analyses of wordforms for the Võro
language are presented in this system in terms of the following symbols.
(It is highly suggested to follow existing standards when adding new tags).

* **+WORK** (eng) work needed 
* __b́__ b plus U+0301 COMBINING ACUTE
* __d́__ d plus U+0301 COMBINING ACUTE
* __f́__ f plus U+0301 COMBINING ACUTE
* __h́__ h plus U+0301 COMBINING ACUTE
* __t́__ t plus U+0301 COMBINING ACUTE
* __v́__ v plus U+0301 COMBINING ACUTE
* __B́__ B plus U+0301 COMBINING ACUTE
* __D́__ D plus U+0301 COMBINING ACUTE
* __F́__ F plus U+0301 COMBINING ACUTE
* __H́__ H plus U+0301 COMBINING ACUTE
* __T́__ T plus U+0301 COMBINING ACUTE
* __V́__ V plus U+0301 COMBINING ACUTE

* **u̬** u plus U+032C COMBINING CARON BELOW
* **U̬** u plus U+032C COMBINING CARON BELOW
* **ü̬** ü plus U+032C COMBINING CARON BELOW
* **Ü̬** ü plus U+032C COMBINING CARON BELOW
* **i̬** i plus U+032C COMBINING CARON BELOW
* **I̬** i plus U+032C COMBINING CARON BELOW
* **õ̭** õ plus U+032D COMBINING CIRCUMFLEX ACCENT BELOW
* **Õ̭** õ plus U+032D COMBINING CIRCUMFLEX ACCENT BELOW
```%{ˋØ%} - U+02CB MODIFIER LETTER GRAVE ACCENT used in rules```

The parts-of-speech are:
* **+N** Noun
* **+A** Adjective
* **+Adv** Adverb
* **+V** Verb

* **+Pron** Pronoun
* **+CS** subjunction
* **+CC** Correlating conjunction
* **+Det** Determiners
* **+Adp** Adpositions
* **+Po** Postposition
* **+Pr** Preposition
* **+Interj** Interjections
* **+Pcle**
* **+Num** Numerals
* **+Qnt**

The parts of speech are further split up into:

* **+Prop**
* **+Pers**
* **+Dem**
* **+Interr**
* **+Refl**
* **+Recipr**
* **+Rel**
* **+Indef**
* **+Deg** adjective or adverb modifier. This is degree, depricate + AdA

The Usage extents are marked using following tags:
* **+Err/Orth**
* **+Err/Orth-dAq-should-be-q-inf** hirnahtadaq should be hirnahtaq
* **+Err/Orth-no-pal** palatalization is missing
* **+Err/Orth-no-q** Q is missing
* **+Err/Orth-raised-vow** 
* **+Err/Orth-lowered-vow** 
* **+Err/Orth-e-stem** should be i stem, but is e stem
* **+Err/Orth-o-stem** should be u stem, but is o stem
* **+Err/Orth-u-stem** should be o stem, but is u stem
* **+Err/Orth-est** 
* **+Err/Orth-weak-grade**
* **+Err/Orth-back** erroneous back harmony, see flags
* **+Err/Orth-front** erroneous front harmony, see flags
* **+Err/Dial** This is the initial Dialect distinction
it will require further work from a professional, i.e., Sullõv or like for
distinguishing dialects.
* **+Dial/-u-not-o** dialect u stem where o expected
* **+Use/-Spell**
* **+Use/SpellNoSugg** not suggested in speller
* **+Use/NG** No generation
* **+Cmp/Hyph** 
* **+Use/PMatch**
* **+Use/TTS** – **only** retained in the HFST Text-To-Speech disambiguation tokeniser
* **+Use/-TTS** – **never** retained in the HFST Text-To-Speech disambiguation tokeniser

The nominals are inflected in the following Case and Number
* **+Sg** Singular
* **+Pl** Plural
* **+SP** Singular and Plural, used for CG and Apertium

* **+Abe** abessive
* **+Abl** ablative
* **+Acc** accusative
* **+Ade** adessive
* **+All** allative
* **+Com** comitative
* **+Com/Sh**
* **+Ela** elative
* **+Ess** essive
* **+Ill** illative
* **+Ine** inessive
* **+Gen** genitive
* **+Loc** locative
* **+Nom** nominative
* **+Par** partitive
* **+Ter** terminative
* **+Tra** translative

The possession is marked as such:
There are no possessive markers

The comparative forms are:
* **+Comp**
* **+Superl**
Numerals are classified under:
* **+Attr**
* **+Card**
* **+Ord**
Verb moods are:
* **+Cond**
* **+Imprt**
* **+Ind**
* **+Jus**
* **+Prs**
* **+Prt**
* **+Pot**
* **+Quo** = quotative, quoted speech

Verb personal forms are:

Subject conjugation

* **+Sg1**
* **+Sg2**
* **+Sg3**
* **+Pl1**
* **+Pl2**
* **+Pl3**

* **+ScSg1**
* **+ScSg2**
* **+ScSg3**
* **+ScPl1**
* **+ScPl2**
* **+ScPl3**
* **+Sc**

Passive conjugation

* **+PcSg1**
* **+PcSg2**
* **+PcSg3**
* **+PcPl1**
* **+PcPl2**
* **+PcPl3**
* **+Pc**
Other verb forms are
* **+Inf** sõimadaq, elädäq
* **+Inf/mA** sõimama, elämä
* **+Ger** ollõn
* **+ConNeg** saa eiq 3 elements in 2 orthographic units
* **+ConNegII** ei saaq 3 elements in 2 orthographic units
* **+Neg** saa-aiq 3 elements in 1 orthographic unit
* **+ImprtII**
* **+PrsPrc**
* **+PrfPrc**
* **+Sup** olõman, olõmaldaq; oldama
* **+VGen**
* **+VAbess**
* **+Act** active
* **+Pss** passive
* **+PrsPrc**
* **+PrfPrc** elet

* **+ABBR**
* +Symbol = independent symbols in the text stream, like £, €, ©
* **+ACR**
* **+Acro**

Special symbols are classified with:
* **+CLB**
* **+PUNCT**
* **+LEFT**
* **+RIGHT**
The verbs are syntactically split according to transitivity:
* **+TV**
* **+IV**
Special multiword units are analysed with:
* **+Multi**
Non-dictionary words can be recognised with:
* **+Guess**

Question and Focus particles:

* **+Qst**
* **+Foc**
* **+Clt**

* **+Hom1**
* **+Hom2**
* **+Hom3**
* **+Hom4**

### Tags distinguishing different versions of the same lemma (before POS)
* +v1
* +v2
* +v3
* +v4
* +v5
* +v6
* +v7
* +v8
* +v9
* +v10
* +v11
* +v12
* +v13
* +v14
* +v15
* +v16
* +v17
* +v18
* +v19
* +v20
* +v21
* +v22
* +v23
* +v24

* **+Sem/ID** used with numerals 2023_04_04

* **+Sem/Act** Activity
* **+Sem/Amount** Amount
* **+Sem/Ani** Animate
* **+Sem/Aniprod** Animal Product
* **+Sem/Body** Bodypart
* **+Sem/Body-abstr** siellu, vuoig?a, jierbmi
* **+Sem/Build** Building
* **+Sem/Build-part** Part of Bulding, like the closet
* **+Sem/Cat** Category
* **+Sem/Clth** Clothes
* **+Sem/Clth-jewl** Jewelery
* **+Sem/Clth-part** part of clothes, boallu, sávdnji...
* **+Sem/Ctain** Container
* **+Sem/Ctain-abstr** Abstract container like bank account
* **+Sem/Ctain-clth**
* **+Sem/Curr** Currency like dollár, Not Money
* **+Sem/Dance** Dance
* **+Sem/Dir** Direction like GPS-kursa
* **+Sem/Domain** Domain like politics, reindeerherding (a system of actions)
* **+Sem/Drink** Drink
* **+Sem/Dummytag** Dummytag
* **+Sem/Edu** Educational event
* **+Sem/Event** Event
* **+Sem/Feat** Feature, like Árvu
* **+Sem/Feat-phys** Physiological feature, ivdni, fárda
* **+Sem/Feat-psych** Psychological feauture
* **+Sem/Feat-measr** Psychological feauture
* **+Sem/Fem** Female name
* **+Sem/Food** Food
* **+Sem/Food-med** Medicine
* **+Sem/Furn** Furniture
* **+Sem/Game** Game
* **+Sem/Geom** Geometrical object
* **+Sem/Group** Animal or Human Group
* **+Sem/Hum** Human
* **+Sem/Hum-abstr** Human abstract
* **+Sem/Ideol** Ideology
* **+Sem/Lang** Language
* **+Sem/Mal** Male name
* **+Sem/Mat** Material for producing things
* **+Sem/Measr** Measure
* **+Sem/Money** Has to do with money, like wages, not Curr(ency)
* **+Sem/Obj** Object
* **+Sem/Obj-clo** Cloth
* **+Sem/Obj-cogn** Cloth
* **+Sem/Obj-el** (Electrical) machine or apparatus
* **+Sem/Obj-ling** Object with something written on it
* **+Sem/Obj-rope** flexible ropelike object
* **+Sem/Obj-surfc** Surface object
* **+Sem/Org** Organisation
* **+Sem/Part** Feature, oassi, bealli
* **+Sem/Perc-cogn** Cognative perception
* **+Sem/Perc-emo** Emotional perception
* **+Sem/Perc-phys** Physical perception
* **+Sem/Perc-psych** Physical perception
* **+Sem/Plant** Plant
* **+Sem/Plant-part** Plant part
* **+Sem/Plc** Place
* **+Sem/Plc-abstr** Abstract place
* **+Sem/Plc-elevate** Place
* **+Sem/Plc-line** Place
* **+Sem/Plc-water** Place
* **+Sem/Pos** Position (as in social position job)
* **+Sem/Process** Process
* **+Sem/Prod** Product
* **+Sem/Prod-audio** Audio product
* **+Sem/Prod-cogn** Cognition product
* **+Sem/Prod-ling** Linguistic product
* **+Sem/Prod-vis** Visual product
* **+Sem/Rel** Relation
* **+Sem/Route** Name of a Route
* **+Sem/Rule** Rule or convention
* **+Sem/Semcon** Semantic concept
* **+Sem/Sign** Sign (e.g. numbers, punctuation) 
* **+Sem/Sport** Sport
* **+Sem/State** 
* **+Sem/State-sick** Illness
* **+Sem/Substnc** Substance, like Air and Water
* **+Sem/Sur** Surname
* **+Sem/Symbol** Symbol
* **+Sem/Time** Time
* **+Sem/Tool** Prototypical tool for repairing things
* **+Sem/Tool-catch** Tool used for catching (e.g. fish)
* **+Sem/Tool-clean** Tool used for cleaning
* **+Sem/Tool-it** Tool used in IT
* **+Sem/Tool-measr** Tool used for measuring
* **+Sem/Tool-music** Music instrument
* **+Sem/Tool-write** Writing tool
* **+Sem/Txt** Text (girji, lávlla...)
* **+Sem/Veh** Vehicle
* **+Sem/Wpn** Weapon
* **+Sem/Wthr** The Weather or the state of ground

* **+Sem/Ant_Fem**
* **+Sem/Ant_Mal**
* **+Temp**

Derivations are classified under the morphophonetic form of the suffix, the
source and target part-of-speech.
* **+V→N**
* **+V→V**
* **+V→A**
* **+Prop→A**
* **+Der**
* **+Der/xxx**
** +Der/JA **	NomAg
** +Der/minE ** NomAct
** +Der/Us   ** A→N
**+Der/lt	   ** A→Adv

# Morphophonology
To represent phonologic variations in word forms we use the following
symbols in the lexicon files:
```
 %{aä%}    — Vowel harmony with "(t)a/ä" AÄ1:a AÄ1:ä AÄ1:0
 %{ae%}   — Vowel harmony with "a/e/õ" passive tahetu
 %{aõ%}   — Vowel harmony with "a/e/õ" passive sõidõtu
 %{äe%}    — Vowel harmony with "ä/e/õ" passive
 %{eõ%}    — Vowel harmony with "e/õ"
 %{uü%}    — Vowel harmony with "u/ü"
 %{öü%}    — Vowel raising
 %{ou%}    — Vowel raising
 %{ei%}    — Vowel raising
 %{õy%}    — Vowel raising
 %{ao%}    — Vowel raising
 %{eØ%}    — ütlemä:üt%{eØ%}l  
 %{õØ%}    — ütlemä:üt%{eØ%}l  
 %{Øõ%}    — juurdlõma:juur%{dØ%}%{0õ%}l
 %{XV%}    — This is used for echoing the previous vowel
 %{XC%}    — This is used for lengthening a consonant
 %{dØ%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{tØ%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{t́Ø%}    — HJK and KimmoK ideas jaht́lõma:jah%{t́Ø%}%{eØ%}%{lĺ%}
 %{dv%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{ij%}    ellä%{ij%}
 %{gv%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{gl%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{gØ%}    — HJK and KimmoK ideas argnõma:ar%{gØ%}
 %{uv%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{üv%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
```

## Gemination
```
 %{hØ%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{jØ%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{kØ%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{lØ%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{mØ%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{nØ%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{pØ%}    — HJK and KimmoK ideas oppama:o%{pØ%}pama
 %{rØ%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{sØ%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{vØ%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{Øp%}    — häbü:hä%{Øp%}%{pbØ%}ü
 %{Øt%}    — koda:ko%{Øt%}%{tdØ%}a
 %{Øk%}    — nägo:nä%{Øk%}%{kgØ%}o

```

## Strong and weak
```
 %{pb%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{td%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{t́d́%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{kg%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{bv%}    — HJK and KimmoK ideas närväs:när%{bv%}ä%{sØ%}
 %{dr%}    — HJK and KimmoK ideas parras:par%{dr%}a%{sØ%}
 %{bm%}    — HJK and KimmoK ideas lammas:lam%{bm%}a%{sØ%}
 %{dn%}    — HJK and KimmoK ideas lammas:lam%{bm%}a%{sØ%}
 %{dl%}    — HJK and KimmoK ideas lammas:lam%{bm%}a%{sØ%}
 %{pbØ%}   — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{pbv%}   — tõbi: tõvõ tõpõ tõppõ
 %{tdØ%}   — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{kgØ%}   — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{jiØ%}   — HJK and KimmoK ideas vari:var%{jiØ%}o
 %{qmn%}   — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{qn%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{dd́Ø%}   
 %{dd́n%}   
 %{dd́r%}   
 %{dd́v%}   
 %{dd́Ø%}   
 %{gǵv%}   
 %{gǵØ%}   
 %{tt́d%}   
 %{tt́Ø%}    täh%{tt́Ø%}
 %{kḱg%}   
 %{kḱØ%}   
 %{pṕb%}   
 %{pṕØ%}   

 %{dśtv%}    tä%{üv%}%{śtv%}
 %{djśt%}    vii%{jśt%}
 %{drśt%}    var%{rśt%}

```

## Palatalization
```
 %{bb́%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{dd́%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{ff́%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{gǵ%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{hh́%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{kḱ%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{lĺ%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{mḿ%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{nń%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{pṕ%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{rŕ%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{sś%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{tt́%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{vv́%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{ḱǵj%}   — HJK and KimmoK ideas laǵa:la%{ḱǵj%}a
 %{zź%}    — HJK and KimmoK ideas kana:ka%{nØ%}na
 %{dd́n%}  
```

** %^I7         **  This appears in stem vaoma:va%^I7o for vaio
** %^K7         **  This appears in stem väemä:vä%^K7e for väkeq
** %^V7         **  This appears in stem häömä:hä%^V7ö for hävvü
** %^T7         **  This appears in stem kaoma:ka%^T7o for katoq
** %^Y7         **  This appears for syna = s%^Y7na and is rendered as õ in the norm

And following triggers to control variation
%^ErrorBack	 +Err/Orth+Clt:%>kinaq in front harmony context BHARM disallowance

 %^CC2C 	 att%^CC2C%>m%{aä%} atma
 %^OO2Õ		  joo%^OO2Õ%>i:j0õ0%>i
 %^PSS		 vowel in passive tahetu, sõidõtu, eletü

 %^ÄI2ÄÄ  päiv%^ÄI2ÄÄ%>ä: päävä
 %{PrsSg1%}  — this helps with %{eõ%}:i̬

%^StrD2T  This changes g,d,b, => k,t,p

** %^VowRM  ** this will remove stem final vowel
** %^CnsRM  ** this will remove stem final consonant tervüs:tervü
** %^StrGStem ** This strengthens "perädü" to "perätüt"
 **%^NoGrad**
** %^WGStem ** This weakens
 %^G1	       — This is used with %{pØ%} %{pbØ%} for 0 0, also t, k
 %^G2	       — This is used with %{pØ%} %{pbØ%} for 0 b, also t, k
 %^G3	       — This is used with %{pØ%} %{pbØ%} for 0 p, also t, k
 %^G4	       — This is used with %{pØ%} %{pbØ%} for p p, also t, k "sõda" to "sõtta"
%^ShortGStem   — This shortens "pu%{tØ%}tu" to "putma", an orthographic convension
%^LongGStem     — This lengthens "pu%{tØ%}tu" to "puttuq"
 %^Pen	       This moves us to penultimate coda
 %^PAL	       — Palatalization
 %^NoPAL       — NoPalatalization
%^JI20	       — in vari: vaŕo
%^JI2I	       — in vari vari
%^JI2J	       — in vari: varjo

%^PenWGStem  This weakens "kipõń" to "kibõna"

** %^PenVowRM ** syncope tapõld : taplõma

**%^D2S	  ** käsi, susi
%^TS2S  The -ts- => -s-
%^I2J  The i => j change

** %^PLPRT ** The a:o attested in Plural kana:kanno and prt
**%^VOWRaise      ** Raises vowel
**%^VOWLower  ** Lowers vowel
**%^XLowerVow ** Lowers vowel two levels
**%^VOWLowerDelab ** Lowers vowel and delabializes it
**%^XLowerVowDelab ** Lowers vowel two levels and delabializes it
%^U2E  lowers u:õ and ü:e delabializes and lowers
%^U2A  lowers u:a and ü:ä delabializes and lowers

**∑** = a symbol used in front of `#` to block backtracking and
mwe reanalysis in hfst-tokenise (e.g. in dynanic compounds).
Makes it possible to distinguish lexical and dynamic compounds
in rules. It is converted to zero together with `#`.

| Flag | Explanation
| ---- | ----------- 
|  @D.ErrOrth.ON@ 
|  @C.ErrOrth@ 
|  @P.ErrOrth.ON@ 
|  @R.ErrOrth.ON@ 

* **@P.Pmatch.Backtrack@**:

* **+Gram/TAbbr**:  Transitive abbreviation (it needs an argument)
* **+Gram/NoAbbr**:  Intransitive abbreviations that are homonymous
with more frequent words. They should only be considered
abbreviations in the middle of a sentence.
* **+Gram/TNumAbbr**:  Transitive abbreviation if the following
constituent is numeric
* **+Gram/NumNoAbbr**:  Transitive abbreviations for which numerals
are complements and normal words. The abbreviation usage
is less common and thus only the occurences in the middle of
the sentence can be considered as true cases.
* **+Gram/TIAbbr**:  Both transitive and intransitive abbreviation
* **+Gram/IAbbr**:  Intransitive abbreviation (it takes no argument)
* **+Gram/3syll**: trisyllabic verbs
; +Gram/Superl 
; +Gram/Comp 

# Oahpa Place names and case used 
* **+%<plc_ine%>  **:  Ine, Ill, Ela
* **+%<plc_ade%>  **:  Ade, All, Abl
* **+%<pcl_pääl%> **:  pääl, pääle, päält

The tagged part of the compound should make a compound using:

* **+CmpN/SgN** Singular Nominative
* **+CmpN/SgG** Singular Genitive

# Flag diacritics
We have manually optimised the structure of our lexicon using the following
flag diacritics to restrict morhpological combinatorics - only allow
compounds with verbs if the verb is further derived into a noun again:
|  **@P.NeedNoun.ON@** | (Dis)allow compounds with verbs unless nominalised
|  **@D.NeedNoun.ON@** | (Dis)allow compounds with verbs unless nominalised
|  **@C.NeedNoun@** | (Dis)allow compounds with verbs unless nominalised

For languages that allow compounding, the following flag diacritics are needed
to control position-based compounding restrictions for nominals. Their use is
handled automatically if combined with +CmpN/xxx tags. If not used, they will
do no harm.
|  **@P.CmpFrst.FALSE@** | Require that words tagged as such only appear first
|  **@D.CmpPref.TRUE@** | Block such words from entering ENDLEX
|  **@P.CmpPref.FALSE@** | Block these words from making further compounds
|  **@D.CmpLast.TRUE@** | Block such words from entering R
|  **@D.CmpNone.TRUE@** | Combines with the next tag to prohibit compounding
|  **@U.CmpNone.FALSE@** | Combines with the prev tag to prohibit compounding
|  **@P.CmpOnly.TRUE@** | Sets a flag to indicate that the word has passed R
|  **@D.CmpOnly.FALSE@** | Disallow words coming directly from root.

Use the following flag diacritics to control downcasing of derived proper
nouns (e.g. Finnish Pariisi -> pariisilainen). See e.g. North Sámi for how to use
these flags. There exists a ready-made regex that will do the actual down-casing
given the proper use of these flags.

|  **@U.Cap.Obl@** | Allowing downcasing of derived names: deatnulasj.
|  **@U.Cap.Opt@** | Allowing downcasing of derived names: deatnulasj.

|  **@U.Case.Abe@** | Abessive
|  **@U.Case.Abl@** | Ablative
|  **@U.Case.Ade@** | Adessive
|  **@U.Case.All@** | Allative
|  **@U.Case.Com@** | Comitative
|  **@U.Case.Ela@** | Elative
|  **@U.Case.Gen@** | Genitive
|  **@U.Case.Ill@** | Illative
|  **@U.Case.Ine@** | Inessive
|  **@U.Case.Nom@** | Nominative
|  **@U.Case.Par@** | Partitive
|  **@U.Case.Ter@** | Terminative
|  **@U.Case.Tra@** | Translative

|  **@U.Number.Pl@** | Plural
|  **@U.Number.Sg@** | Singular

The following flag diacritics are being applied for vowel harmony variation
|  **@U.VowHarm.B@** | Back harmony, used with subsequent Err/Orth-front
|  **@U.VowHarm.F@** | Front harmony, used with subsequent Err/Orth-back

# The Root lexicon

The word forms in the Võro language start from the lexeme roots of basic
word classes, or optionally from prefixes:
* **adpositions ;**
* **adverbs ;**
* **conjunctors ;**
* **interjections ;**
* **pronouns ;**
* **PronounTypes ;**
* **Punctuation ;**
* **Symbols ;**
* **numerals ;**
look at verb_newwords.lexc

* **Exceptions ;**
* **Abbreviation ;**
* **Acronym ;**

Incoming
* **A_NEWWORDS ;**
* **ADP_NEWWORDS ;**
* **ADV_NEWWORDS ;** 
* **DET_NEWWORDS ;**
* **INTERJ_NEWWORDS ;**
* **N_NEWWORDS ;**
* **@U.Cap.Obl@ PROP_NEWWORDS ;**
* **@U.Cap.Opt@ PROP_NEWWORDS ;**
* **V_NEWWORDS ;**
* **GenitiveAttributes ;** Borrowed from experimental_languages est
* **NUM-PREFIXES ;** copied from giella-shared/smi

less complex word classes

* * *

<small>This (part of) documentation was generated from [src/fst/root.lexc](https://github.com/giellalt/lang-vro/blob/main/src/fst/root.lexc)</small>

---

Acronyms
Veps acronyms ...

* * *

<small>This (part of) documentation was generated from [src/fst/stems/acronyms.lexc](https://github.com/giellalt/lang-vro/blob/main/src/fst/stems/acronyms.lexc)</small>

---

This is where new words are added as lexc entries before they are 
added to the xml source files.
kõhna+A:kõhna A_1HANS1A "" ;

ADD NOUNS BELOW

| --- 

* * *

<small>This (part of) documentation was generated from [src/fst/stems/adjectives_newwords.lexc](https://github.com/giellalt/lang-vro/blob/main/src/fst/stems/adjectives_newwords.lexc)</small>

---

This is where new words are added as lexc entries before they are
added to the xml source files.
perrä:perrä PO_ "(eng) /(est) /(fin) " ;

ADD NOUNS BELOW

* * *

<small>This (part of) documentation was generated from [src/fst/stems/adpositions_newwords.lexc](https://github.com/giellalt/lang-vro/blob/main/src/fst/stems/adpositions_newwords.lexc)</small>

---



CHECKME

* * *

<small>This (part of) documentation was generated from [src/fst/stems/adverbs_newwords.lexc](https://github.com/giellalt/lang-vro/blob/main/src/fst/stems/adverbs_newwords.lexc)</small>

---

This is where new words are added as lexc entries before they are
added to the xml source files.
perrä:perrä PO_ "(eng) /(est) /(fin) " ;

ADD DETERMINERS BELOW

* * *

<small>This (part of) documentation was generated from [src/fst/stems/determiners_newwords.lexc](https://github.com/giellalt/lang-vro/blob/main/src/fst/stems/determiners_newwords.lexc)</small>

---


### ADVERBS

### ADJECTIVES

### CONJUNTIONS

### GENITIVE ATTRIBUTES

### NOUNS

### PROPER NOUNS

### PLURAL NOUNS

### NUMERALS

### POSTPOSITIONA

### PRONOUNS

### VERBS

andma **to give/antaa**

### VERBS WITH FORMS TO STUDY

kündma **to plow/kyntää**

nakkama **to begin/ alkaa**

olõma **to be/ olla**

nakkama **to start/ alkaa**

pandma **to put/panna**

pidämä **to keep/ pitää**

tundma **to feel/tuntea**

* * *

<small>This (part of) documentation was generated from [src/fst/stems/exceptions.lexc](https://github.com/giellalt/lang-vro/blob/main/src/fst/stems/exceptions.lexc)</small>

---

This is where new words are added as lexc entries before they are 
added to the xml source files.

ADD INTERJECTIONS BELOW

* * *

<small>This (part of) documentation was generated from [src/fst/stems/interjections_newwords.lexc](https://github.com/giellalt/lang-vro/blob/main/src/fst/stems/interjections_newwords.lexc)</small>

---


hanśa+N:hanśa N_1HANS1A "" ;

* * *

<small>This (part of) documentation was generated from [src/fst/stems/nouns.lexc](https://github.com/giellalt/lang-vro/blob/main/src/fst/stems/nouns.lexc)</small>

---

This is where new words are added as lexc entries before they are 
added to the xml source files.
hanśa+N:hanśa N_1HANS1A "" ;

ADD NOUNS BELOW

N_HAIDAK, N_10ESAEK in -gu
N_10AABITS in -dsa, -ga
N_10HWRAK in -ga ~ -gu
N_10HEERITS in -dsä
N_10RAAMAT, N_LEMBIT in -du/dü

two-syllable

Three-syllable words

* * *

<small>This (part of) documentation was generated from [src/fst/stems/nouns_newwords.lexc](https://github.com/giellalt/lang-vro/blob/main/src/fst/stems/nouns_newwords.lexc)</small>

---


atma+V:atta, ikma+V:ikkõ
petmä+V:pettä

* * *

<small>This (part of) documentation was generated from [src/fst/stems/verbs.lexc](https://github.com/giellalt/lang-vro/blob/main/src/fst/stems/verbs.lexc)</small>

---

This is where new words are added as lexc entries before they are
added to the xml source files.

ADD VERBS BELOW

verb type split

atma+V:atta, ikma+V:ikkõ
petmä+V:pettä

* * *

<small>This (part of) documentation was generated from [src/fst/stems/verbs_newwords.lexc](https://github.com/giellalt/lang-vro/blob/main/src/fst/stems/verbs_newwords.lexc)</small>

---



retroflex plosive, voiceless			t`  ʈ	    0288, 648 (` = ASCII 096)
retroflex plosive, voiced			d`	ɖ		0256, 598
labiodental nasal					F 	ɱ		0271, 625
retroflex nasal						n` 	ɳ		0273, 627
palatal nasal						J 	ɲ		0272, 626
velar nasal							N 	ŋ		014B, 331
uvular nasal							N\	ɴ		0274, 628
	
bilabial trill						B\ 	ʙ		0299, 665
uvular trill							R\ 	ʀ		0280, 640
alveolar tap							4	ɾ		027E, 638
retroflex flap						r` 	ɽ		027D, 637
bilabial fricative, voiceless		p\ 	ɸ		0278, 632
bilabial fricative, voiced			B 	β		03B2, 946
dental fricative, voiceless			T 	θ		03B8, 952
dental fricative, voiced				D 	ð		00F0, 240
postalveolar fricative, voiceless	S	ʃ		0283, 643
postalveolar fricative, voiced		Z 	ʒ		0292, 658
retroflex fricative, voiceless		s` 	ʂ		0282, 642
retroflex fricative, voiced			z` 	ʐ		0290, 656
palatal fricative, voiceless			C 	ç		00E7, 231
palatal fricative, voiced			j\ 	ʝ		029D, 669
velar fricative, voiced	        	G 	ɣ		0263, 611
uvular fricative, voiceless			X	χ		03C7, 967
uvular fricative, voiced				R 	ʁ		0281, 641
pharyngeal fricative, voiceless		X\ 	ħ		0127, 295
pharyngeal fricative, voiced			?\ 	ʕ		0295, 661
glottal fricative, voiced			h\	ɦ		0266, 614

alveolar lateral fricative, vl.		K 
alveolar lateral fricative, vd.		K\

labiodental approximant				P (or v\) 
alveolar approximant					r\ 
retroflex approximant				r\` 
velar approximant					M\

retroflex lateral approximant		l` 
palatal lateral approximant			L 
velar lateral approximant			L\
Clicks

bilabial								O\	(O = capital letter) 
dental								|\
(post)alveolar						!\ 
palatoalveolar						=\ 
alveolar lateral						|\|\
Ejectives, implosives

ejective								_>	e.g. ejective p		p_>
implosive							_<	e.g. implosive b	b_<
Vowels

close back unrounded					M
close central unrounded 				1 
close central rounded				} 
lax i								I 
lax y								Y 
lax u								U

close-mid front rounded				2 
close-mid central unrounded			@\ 
close-mid central rounded			8 
close-mid back unrounded				7

schwa	ə							@

open-mid front unrounded				E 
open-mid front rounded				9
open-mid central unrounded			3 
open-mid central rounded				3\ 
open-mid back unrounded				V 
open-mid back rounded				O

ash (ae digraph)						{ 
open schwa (turned a)				6

open front rounded					& 
open back unrounded	        		A 
open back rounded					Q
Other symbols

voiceless labial-velar fricative		W 
voiced labial-palatal approx.		H 
voiceless epiglottal fricative		H\ 
voiced epiglottal fricative			<\ 
epiglottal plosive					>\

alveolo-palatal fricative, vl. 		s\ 
alveolo-palatal fricative, voiced	z\ 
alveolar lateral flap				l\ 
simultaneous S and x					x\ 
tie bar								_
Suprasegmentals

primary stress						" 
secondary stress						% 
long									: 
half-long							:\ 
extra-short							_X 
linking mark							-\
Tones and word accents

level extra high						_T 
level high							_H
level mid							_M 
level low							_L 
level extra low						_B
downstep								! 
upstep								^	(caret, circumflex)

contour, rising						 
contour, falling						_F 
contour, high rising					_H_T 
contour, low rising					_B_L 

contour, rising-falling				_R_F 
(NB Instead of being written as diacritics with _, all prosodic 
marks can alternatively be placed in a separate tier, set off 
by < >, as recommended for the next two symbols.)
global rise						<R> 
global fall						<F>
Diacritics						
									
voiceless						_0	(0 = figure), e.g. n_0
voiced							_v 
aspirated						_h 
more rounded						_O	(O = letter) 
less rounded						_c 
advanced							_+
retracted						_-
centralized						_" 
syllabic							=	(or _=) e.g. n= (or n_=) 
non-syllabic						_^ 
rhoticity						`
									
breathy voiced					_t 
creaky voiced					_k
linguolabial						_N 
labialized						_w 
palatalized						'	(or _j) e.g. t' (or t_j) 
velarized						_G 
pharyngealized					_?\
									
dental							_d 
apical							_a 
laminal							_m
nasalized						~	(or _~) e.g. A~ (or A_~) 
nasal release					_n
lateral release					_l 
no audible release				_}

velarized or pharyngealized		_e 
velarized l, alternatively		5 
raised							_r 
lowered							_o 
advanced tongue root				_A 
retracted tongue root			_q

* * *

<small>This (part of) documentation was generated from [src/phonetics/txt2ipa.xfscript](https://github.com/giellalt/lang-vro/blob/main/src/phonetics/txt2ipa.xfscript)</small>

---



We describe here how abbreviations are in Võro are read out, e.g.
for text-to-speech systems.

For example:

* s.:syntynyt # ;  
* os.:omaa% sukua # ;  
* v.:vuosi # ;  
* v.:vuonna # ;  
* esim.:esimerkki # ; 
* esim.:esimerkiksi # ; 

* * *

<small>This (part of) documentation was generated from [src/transcriptions/transcriptor-abbrevs2text.lexc](https://github.com/giellalt/lang-vro/blob/main/src/transcriptions/transcriptor-abbrevs2text.lexc)</small>

---



Ordinal numerals begin

* * *

<small>This (part of) documentation was generated from [src/transcriptions/transcriptor-numbers-digit2text.lexc](https://github.com/giellalt/lang-vro/blob/main/src/transcriptions/transcriptor-numbers-digit2text.lexc)</small>

---


[ L A N G U A G E ]  G R A M M A R   C H E C K E R

# DELIMITERS

# TAGS AND SETS

## Tags

This section lists all the tags inherited from the fst, and used as tags
in the syntactic analysis. The next section, **Sets**, contains sets defined
on the basis of the tags listed here, those set names are not visible in the output.

### Beginning and end of sentence
BOS
EOS

### Parts of speech tags

N
A
Adv
V
Pron
CS
CC
CC-CS
Po
Pr
Pcle
Num
Interj
ABBR
ACR
CLB
LEFT
RIGHT
WEB
PPUNCT
PUNCT

COMMA
¶

### Tags for POS sub-categories

Pers
Dem
Interr
Indef
Recipr
Refl
Rel
Coll
NomAg
Prop
Allegro
Arab
Romertall

### Tags for morphosyntactic properties

Nom
Acc
Gen
Ill
Loc
Com
Ess
Ess
Sg
Du
Pl
Cmp/SplitR
Cmp/SgNom Cmp/SgGen
Cmp/SgGen
PxSg1
PxSg2
PxSg3
PxDu1
PxDu2
PxDu3
PxPl1
PxPl2
PxPl3
Px

Comp
Superl
Attr
Ord
Qst
IV
TV
Prt
Prs
Ind
Pot
Cond
Imprt
ImprtII
Sg1
Sg2
Sg3
Du1
Du2
Du3
Pl1
Pl2
Pl3
Inf
ConNeg
Neg
PrfPrc
VGen
PrsPrc
Ger
Sup
Actio
VAbess

Err/Orth

### Semantic tags

Sem/Act
Sem/Ani
Sem/Atr
Sem/Body
Sem/Clth
Sem/Domain
Sem/Feat-phys
Sem/Fem
Sem/Group
Sem/Lang
Sem/Mal
Sem/Measr
Sem/Money
Sem/Obj
Sem/Obj-el
Sem/Org
Sem/Perc-emo
Sem/Plc
Sem/Sign
Sem/State-sick
Sem/Sur
Sem/Time
Sem/Txt

HUMAN

PROP-ATTR
PROP-SUR

TIME-N-SET

###  Syntactic tags

@+FAUXV
@+FMAINV
@-FAUXV
@-FMAINV
@-FSUBJ>
@-F<OBJ
@-FOBJ>
@-FSPRED<OBJ
@-F<ADVL
@-FADVL>
@-F<SPRED
@-F<OPRED
@-FSPRED>
@-FOPRED>
@>ADVL
@ADVL<
@<ADVL
@ADVL>
@ADVL
@HAB>
@<HAB
@>N
@Interj
@N<
@>A
@P<
@>P
@HNOUN
@INTERJ
@>Num
@Pron<
@>Pron
@Num<
@OBJ
@<OBJ
@OBJ>
@OPRED
@<OPRED
@OPRED>
@PCLE
@COMP-CS<
@SPRED
@<SPRED
@SPRED>
@SUBJ
@<SUBJ
@SUBJ>
SUBJ
SPRED
OPRED
@PPRED
@APP
@APP-N<
@APP-Pron<
@APP>Pron
@APP-Num<
@APP-ADVL<
@VOC
@CVP
@CNP
OBJ
<OBJ
OBJ>
<OBJ-OTHERS
OBJ>-OTHERS
SYN-V
@X

## Sets containing sets of lists and tags

This part of the file lists a large number of sets based partly upon the tags defined above, and
partly upon lexemes drawn from the lexicon.
See the sourcefile itself to inspect the sets, what follows here is an overview of the set types.

### Sets for Single-word sets

INITIAL

### Sets for word or not

WORD
NOT-COMMA

### Case sets

ADLVCASE

CASE-AGREEMENT
CASE

NOT-NOM
NOT-GEN
NOT-ACC

### Verb sets

NOT-V

### Sets for finiteness and mood

REAL-NEG

MOOD-V

NOT-PRFPRC

### Sets for person

SG1-V
SG2-V
SG3-V
DU1-V
DU2-V
DU3-V
PL1-V
PL2-V
PL3-V

### Pronoun sets

### Adjectival sets and their complements

### Adverbial sets and their complements

### Sets of elements with common syntactic behaviour

### NP sets defined according to their morphosyntactic features

### The PRE-NP-HEAD family of sets

These sets model noun phrases (NPs). The idea is to first define whatever can
occur in front of the head of the NP, and thereafter negate that with the
expression **WORD - premodifiers**.

### Border sets and their complements

### Grammarchecker sets

* * *
<small>This (part of) documentation was generated from [tools/grammarcheckers/grammarchecker.cg3](https://github.com/giellalt/lang-vro/blob/main/tools/grammarcheckers/grammarchecker.cg3)</small># Tokeniser for vro

Usage:
```
$ make
$ echo "ja, ja" | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
$ echo "Juos gorreválggain lea (dárbbašlaš) deavdit gáibádusa boasttu olmmoš, man mielde lahtuid." | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
$ echo "(gáfe) 'ja' ja 3. ja? ц jaja ukjend \"ukjend\"" | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
$ echo "márffibiillagáffe" | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
```

Pmatch documentation:
<https://github.com/hfst/hfst/wiki/HfstPmatch>

Characters which have analyses in the lexicon, but can appear without spaces
before/after, that is, with no context conditions, and adjacent to words:
* Punct contains ASCII punctuation marks
* The symbol after m-dash is soft-hyphen `U+00AD`
* The symbol following {•} is byte-order-mark / zero-width no-break space
`U+FEFF`.

Whitespace contains ASCII white space and
the List contains some unicode white space characters
* En Quad U+2000 to Zero-Width Joiner U+200d'
* Narrow No-Break Space U+202F
* Medium Mathematical Space U+205F
* Word joiner U+2060

Apart from what's in our morphology, there are
1. unknown word-like forms, and
2. unmatched strings
We want to give 1) a match, but let 2) be treated specially by
`hfst-tokenise -a`
Unknowns are made of:
* lower-case ASCII
* upper-case ASCII
* select extended latin symbols
ASCII digits
* select symbols
* Combining diacritics as individual symbols,
* various symbols from Private area (probably Microsoft),
so far:
* U+F0B7 for "x in box"

## Unknown handling
Unknowns are tagged ?? and treated specially with `hfst-tokenise`
hfst-tokenise --giella-cg will treat such empty analyses as unknowns, and
remove empty analyses from other readings. Empty readings are also
legal in CG, they get a default baseform equal to the wordform, but
no tag to check, so it's safer to let hfst-tokenise handle them.

Finally we mark as a token any sequence making up a:
* known word in context
* unknown (OOV) token in context
* sequence of word and punctuation
* URL in context

* * *

<small>This (part of) documentation was generated from [tools/tokenisers/tokeniser-disamb-gt-desc.pmscript](https://github.com/giellalt/lang-vro/blob/main/tools/tokenisers/tokeniser-disamb-gt-desc.pmscript)</small>

---

# Grammar checker tokenisation for vro

Requires a recent version of HFST (3.10.0 / git revision>=3aecdbc)
Then just:
```
$ make
$ echo "ja, ja" | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
```

More usage examples:
```
$ echo "Juos gorreválggain lea (dárbbašlaš) deavdit gáibádusa boasttu olmmoš, man mielde lahtuid." | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
$ echo "(gáfe) 'ja' ja 3. ja? ц jaja ukjend \"ukjend\"" | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
$ echo "márffibiillagáffe" | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
```

Pmatch documentation:
<https://github.com/hfst/hfst/wiki/HfstPmatch>

Characters which have analyses in the lexicon, but can appear without spaces
before/after, that is, with no context conditions, and adjacent to words:
* Punct contains ASCII punctuation marks
* The symbol after m-dash is soft-hyphen `U+00AD`
* The symbol following {•} is byte-order-mark / zero-width no-break space
`U+FEFF`.

Whitespace contains ASCII white space and
the List contains some unicode white space characters
* En Quad U+2000 to Zero-Width Joiner U+200d'
* Narrow No-Break Space U+202F
* Medium Mathematical Space U+205F
* Word joiner U+2060

Apart from what's in our morphology, there are
1) unknown word-like forms, and
2) unmatched strings
We want to give 1) a match, but let 2) be treated specially by hfst-tokenise -a
* select extended latin symbols
* select symbols
* various symbols from Private area (probably Microsoft),
so far:
* U+F0B7 for "x in box"

TODO: Could use something like this, but built-in's don't include šžđčŋ:

Simply give an empty reading when something is unknown:
hfst-tokenise --giella-cg will treat such empty analyses as unknowns, and
remove empty analyses from other readings. Empty readings are also
legal in CG, they get a default baseform equal to the wordform, but
no tag to check, so it's safer to let hfst-tokenise handle them.

Finally we mark as a token any sequence making up a:
* known word in context
* unknown (OOV) token in context
* sequence of word and punctuation
* URL in context

* * *

<small>This (part of) documentation was generated from [tools/tokenisers/tokeniser-gramcheck-gt-desc.pmscript](https://github.com/giellalt/lang-vro/blob/main/tools/tokenisers/tokeniser-gramcheck-gt-desc.pmscript)</small>

---

# TTS tokenisation for smj

Requires a recent version of HFST (3.10.0 / git revision>=3aecdbc)
Then just:
```sh
make
echo "ja, ja" \
| hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
```

More usage examples:
```sh
echo "Juos gorreválggain lea (dárbbašlaš) deavdit gáibádusa \
boasttu olmmoš, man mielde lahtuid." \
| hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
echo "(gáfe) 'ja' ja 3. ja? ц jaja ukjend \"ukjend\"" \
| hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
echo "márffibiillagáffe" \
| hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
```

Pmatch documentation:
<https://kitwiki.csc.fi/twiki/bin/view/KitWiki/HfstPmatch>

Characters which have analyses in the lexicon, but can appear without spaces
before/after, that is, with no context conditions, and adjacent to words:
* Punct contains ASCII punctuation marks
* The symbol after m-dash is soft-hyphen `U+00AD`
* The symbol following {•} is byte-order-mark / zero-width no-break space
`U+FEFF`.

Whitespace contains ASCII white space and
the List contains some unicode white space characters
* En Quad U+2000 to Zero-Width Joiner U+200d'
* Narrow No-Break Space U+202F
* Medium Mathematical Space U+205F
* Word joiner U+2060

Apart from what's in our morphology, there are
1) unknown word-like forms, and
2) unmatched strings
We want to give 1) a match, but let 2) be treated specially by hfst-tokenise -a
* select extended latin symbols
* select symbols
* various symbols from Private area (probably Microsoft),
so far:
* U+F0B7 for "x in box"

TODO: Could use something like this, but built-in's don't include šžđčŋ:

Simply give an empty reading when something is unknown:
hfst-tokenise --giella-cg will treat such empty analyses as unknowns, and
remove empty analyses from other readings. Empty readings are also
legal in CG, they get a default baseform equal to the wordform, but
no tag to check, so it's safer to let hfst-tokenise handle them.

Needs hfst-tokenise to output things differently depending on the tag they get

* * *

<small>This (part of) documentation was generated from [tools/tokenisers/tokeniser-tts-cggt-desc.pmscript](https://github.com/giellalt/lang-vro/blob/main/tools/tokenisers/tokeniser-tts-cggt-desc.pmscript)</small>

---

