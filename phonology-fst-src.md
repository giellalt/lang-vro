# The Võro morphophonological/twolc rules file 






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
 %^XStrGStem:0  — This extra-strengthens "sõda" to "sõtta"
 %^ShortGStem:0   — This shortens "pu%{tØ%}tu" to "putma", an orthographic convension
 %^LongGStem:0     — This lengthens "pu%{tØ%}tu" to "puttuq"


 %^Pen:0        — This moves us to penultimate coda
 %^PAL:0	       — Palatalization
 %^NoPAL:0	       — NoPalatalization


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
* *pü%{kgØ%}ä%{front%}%^VOWLower%^WGStem%^VowRM%>e%>t*
* *pö000000%>e%>t*
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


akaŕ+A+Sg+Nom
* *a%{kg%}a%{rŕ%}%{back%}%^Pen%^G2%^PAL*
* *akaŕ0000*

asi+N+Sg+Gen:
* *a%{sś%}%{jiØ%}%{back%}%^PAL%^VowRM%>%{aä%}*
* *aś0000%>a*

alostama+V+Act+Ind+Prt+Sg3:
* *alos{tt́}a^Pen^VOWRaise^Pen^PAL^VowRM*
* *alost́000000*

**n2n no palatalization all**


rehksämä+V+Inf/mA:
* *reh{kØ}ä{sś}{front}^Pen^StrGStem^Pen^VowRM^NoPAL>{aä}>m{aä}*
* *rehk0s000000>ä>mä*


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



**%{pṕb%}:p**
loroṕ+N+Sg+Par:
* *loro{pṕb}{back}^StrGStem^NoPAL>i*
* *lorop000>i*

**%{tt́d%}:t**


hainatama+V+Inf/mA
* *haina%{tt́d%}a%{back%}%^Pen%^VOWRaise%>m%{aä%}*
* *hainata000%>ma*

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



**e2i̬**
kiiĺ+N+Sg+Gen: **tongue/kieli**
* *k%{ei%}%{ei%}{lĺ}%{front%}%^VOWRaise%^PAL*
* *ki̬i̬ĺ000*
tegemä+V+Act+Ind+Prs+Sg1: **do**
* *teg%{front%}%^WGStem%>e*
* *ti̬000%>i̬*

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

**Vx%{ou%}2Vyu̬**
nuuĺ+N+Sg+Nom: **arrow**
* *n%{ou%}%{ou%}%{lĺ%}%{back%}%^VOWRaise%^PAL*
* *nu̬u̬ĺ000*
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
       a _ (HarmDummies:) %>  i  ;  
* *saa%{back%}%>i*
* *sa00%>i*
sõimama+V+Act+Ind+Prt+Sg1
* *sõima%{back%}%^Pen%^VOWLower%^Pen%^WGStem%^VowRM%>ssi*
* *sõim0000000%>ssi*
* *puhkas%{back%}%^Pen%^VowRM%>a%>ma*
* *puhk0s000%>a%>ma*
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
* *tütä%{rŕ%}%{front%}%^Pen%^VowRM%>e*
* *tüt0r000%>e*

**U:0 Vx**
```

* *hirnu{back}^Pen^CC2C^VowRM>m{aä}*
* *hirn00000>ma*
* *tervüs{front}^VowRM^CnsRM>i>t*
* *terv00000>i>t*
juusk+N+Sg+Nom: ____
* *j{ou}{ou}s{kØ}u{back}^VOWRaise^VowRM*
* *ju̬u̬sk0000*


* *kuu{back}^VowRM>i>d*
* *ku000>i>d*
```

 [ Cns: |ArchCns:| Vow: ] _ (s:) (HarmDummies:) [(%^Pen: %^CC2C:|%^Pen: %^G3:|%^Pen: %^G4:|PenVOWHite %^Pen: %^G1:) %^VowRM: ]( CnsInZero: (%^Pen: %^CC2C:) %^VowRM: %^CnsRM: )  ; 
* *tüü%{front%}%^VowRM%>hüq*
* *tü000%>hüq*
* *tervüs%{front%}%^VowRM%^WGStem%>i%>t*
* *terv00000%>i%>t*

**e:0**
* *herne%{hØ%}%{front%}%^VowRM%^WGStem%>id%{eõ%}*
* *hern00000%>ide*

**o:0**
juuma+V+Inf
* *j{ou}{ou}{back}^VOWRaise^VowRM>vv>{aä}q*
* *ju̬0000>vv>aq*

**Vx%{ou%}:0**
juuma+V+Inf
* *j{ou}{ou}{back}^VOWRaise^VowRM>vv>{aä}q*
* *ju̬0000>vv>aq*

**Vx%{äe%}:0 Passive stem vowel**


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
* *kan%{dn%}õ%{lĺ%}%{back%}%^Pen%^VowRM%^NoPAL%>%{XV%}*
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

**%{üv%}:v**
* *pü%{üv%}%{dd́v%}%{front%}%^WGStem%>et*
* *püvv00%>et*
* *sü%{üv%}%{dv%}%{front%}%^WGStem%>ä*
* *süvv00%>ä*

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

**%{kḱØ%}:ḱ**



SECONDARY CONSONANT LENGTHENING


**%{pØ%}:p**
```
* *hä%{pØ%}%{pbØ%}ü%{front%}%^Pen%^XStrGStem*
* *häppü000*
* *tõ%{pØ%}%{pbv%}%{back%}%^XStrGStem%>%{eõ%}*
* *tõpp00%>õ*
* *se%{pØ%}p%{front%}%^StrGStem*
* *sepp00*
* *nu%{pØ%}pu%{back%}%^Pen%^VOWRaise%^Pen%^StrGStem%^VowRM*
* *nupp0000000*
```

**%{tØ%}:t**
* *sõ%{tØ%}da%{back%}%^XStrGStem%^PLPRT*
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


**%{Øk%}:k**
igä+N+Sg+Ill
* *i{kØ}{kgØ}ä{front}^Pen^G4*
* *ikkä00*
* *mä%{Øk%}%{kgØ%}%{front%}%^XStrGStem%>%{eõ%}*
* *mäkk00%>e*


**%{XC%}:s**

**%{XC%}:l**

**%{XC%}:ĺ**

**%{XC%}:k**

**%{kḱ%}:ḱ**
kakma
* *ka%{kØ%}%{kḱ%}u%{back%}%^VowRM%^PAL*
* *kakḱ0000*


### Consonant weakening 

**kToZero**  
* *puhkas%{back%}%^WGStem%>taq*
* *puh0as00%>taq*

* *ikkõ%{back%}%^Pen%^CC2C%^VowRM%>m%{aä%}*
* *ik000000%>ma*

**%{pṕØ%}:0**  

**%{tt́Ø%}:0**  

**%{kḱØ%}:0**  

* *j{ou}{ou}s{kḱØ}{back}^VOWLower^WGStem>{eõ}*
* *joos0000>õ*
* ★*j{ou}{ou}s{kḱØ}{back}^VOWLower^WGStem>{eõ}* (is not standard language)
* ★*joosk000>õ* (is not standard language)

**%{sØ%}:0**  
vaśma+V+Inf/mA: **answer/vastata**
* *va{sØ}{sś}{back}^VOWRaise^WGStem^PAL>m{aä}*
* *va0ś0000>ma*
* *su%{sØ%}śo%{back%}%^Pen%^WGStem*
* *su0śo000*
* *ham%{bm%}a%{sØ%}%{back%}%^Pen%^VOWRaise%^Pen%^StrGStem%^WGStem*
* *hamba0000000*


**%{rØ%}:0**  
* *a%{rØ%}ro%{back%}%^Pen%^G2*
* *a0ro000*





**%{nØ%}:0**  
* *su%{nØ%}ńo%{back%}%^Pen%^WGStem*
* *su0ńo000*




**%{lØ%}:0**  
* *ta%{lØ%}lo%{back%}%^Pen%^G2*
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
makḱ+N+Pl+All
* *ma{kØ}{kḱ}{back}^StrGStem^NoPAL>{eõ}>l{eõ}*
* *makk000>õ>lõ*

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

* *avali%{kØ%}%{kg%}%{back%}%^G2*
* *avali0k00*

**%{kg%}:g**
apteḱ+N+Sg+Gen:
* *apte{kØ}{kḱg}{back}^VOWLower^G2>i*
* *apte0g000%>i*
agras+A+Sg+Nom:
* *a%{kg%}ra%{sØ%}%{back%}%^Pen%^VOWLower%^Pen%^WGStem*
* *agras00000*

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
* *kergü%{tt́d%}ä%{front%}%^Pen%^WGStem*
* *kergüdä000*



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


**%{tdØ%}:d**

**%{dØ%}:d**
väärdlemä+V+Inf/mA
* *väär{dØ}{eØ}{lĺ}{front}^Pen^VOWRaise^Pen^StrGStem^Pen^VowRM^NoPAL>{eõ}>m{aä}*
* *väärd0l00000000>e>mä*

kaardas+N+Sg+Nom
* *kaar%{dØ%}a%{sØ%}%{back%}%^Pen%^VOWLower%^Pen%^StrGStem%^StrGStem*
* *kaardas000000*


**%{kgØ%}:g**
jõgi+N+Sg+Nom
* *jõ%{kØ%}%{kgØ%}%{back%}%^G2%>i*
* *jõ0g00%>i*

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
* *kõi%{kØ%}%{kḱg%}%{back%}%^G1%>%{eõ%}*
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
* *tõ%{pØ%}%{pbv%}%{back%}%^XStrGStem%>%{eõ%}*
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
hanǵ+N+Sg+Gen: **snow pack/hanki**
* *han{gǵØ}{back}^WGStem^NoPAL>%{eõ%}*
* *hang000>e*
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

