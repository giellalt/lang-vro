

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

* @CVP = Conjunction or subjunction that conjoins finite verb phrases.
* @CNP = Local conjunction or subjunction.






















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











* MOD-ASP = auxilaries














































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
<small>This (part of) documentation was generated from [../src/cg3/disambiguator.cg3](http://github.com/giellalt/lang-vro/blob/main/../src/cg3/disambiguator.cg3)</small>