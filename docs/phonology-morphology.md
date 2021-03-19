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

 **%^Y7:õ**  This appears for syna = s%^Y7na and is rendered as õ in the norm
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









* *viska%^WGStem%>aq*
* *vis0a0%>aq*
* *füüsiga%^StrGStem%^VowRM%>i%>dõ*
* *füüsik000%>i%>dõ*






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
* *tah%{tØ%}%{ae%}%^Pen%^WGStem%^PSS%>t%{uü%}*
* *tah0e000%>tu*

**%{aõ%}:õ**

**%{äe%}:e**


### VOWEL LOWERING

**u:o**
* *lugõ%^Pen%^VOWLower%^Pen%^WGStem%^VowRM%>i*
* *lo0000000%>i*

**ü:ö**
* *pügä%^VOWLower%^WGStem%^VowRM%>e%>t*
* *pö00000%>e%>t*
* *süü%^VOWLower%^WGStem%>nüq*
* *söö00%>nüq*

**o2õ**
* *joo%^OO2Õ%>i*
* *jõ00%>i*
* *aigo%^OO2Õ*
* *aigõ0*

**u2õ**
* *laulu%^OO2Õ*
* *laulõ0*

**ö2e**
* *söö%^OO2Õ%>i*
* *se00%>i*

**Delabializing o and ö**

### VOWEL RAISING
**Delabializing o and ö**
* *hä%^V70ö%^StrGStem%>i*
* *hävvü0%>0*

### PALATALIZATION
**n2ń palatalization all**


akaŕ+A+Sg+Nom
* *a%{kg%}a%{rŕ%}%{back%}%^Pen%^G2%^PAL*
* *akaŕ0000*

asi+N+Sg+Gen:
* *a%{sś%}%{jiØ%}%^PAL%^VowRM%>%{aä%}*
* *aś000%>a*


**{dd́n}:d́ palatalization for 3-way**

andma+V+Act+Ind+Prs+Sg3
* *an%{dd́n%}%{back%}%^PAL*
* *and́00*

**{dd́n}:n weaken 3-way**

andma+V+Act+Ind+Prs+Sg1
* *an%{dd́n%}%{back%}%^WGStem%>%{aä%}*
* *ann00m%a*

püüdmä+V+Act+Ind+Prs+Sg1
* *pü%{üv%}%{dd́v%}%{front%}%^WGStem%>%{aä%}*
* *püvv00%>ä*



**%{pṕb%}:p**
* *loro%{pṕb%}%{back%}%^G2%>*
* *loroṕ00%>*

**%{tt́d%}:t**


hainatama+V+Inf/mA
* *haina%{tt́d%}a%{back%}%^Pen%^VOWRaise%>m%{aä%}*
* *hainata000%>ma*

**%{kḱg%}:k**
* *pisla%{kḱg%}%{back%}%^G2%>*
* *pislaḱ00%>*



**%{pṕb%}:ṕ**
* *loro%{pṕb%}%{back%}%^G2%^PAL*
* *loroṕ000*

**%{tt́d%}:t́**

**%{kḱg%}:ḱ**
* *pisla%{kḱg%}%{back%}%^G2%^PAL*
* *pislaḱ000*

kõiḱ+Pron+Sg+Nom
* *kõi%{kØ%}%{kḱg%}%^CC2C%^PAL*
* *kõi0ḱ00*



### VOWEL CHANGE WITH PLURAL



**e2i̬**
* *keel%^VOWRaise%^PAL*
* *ki̬i̬ĺ00*
tegemä+V+Act+Ind+Prs+Sg1: **do**
* *teg%{front%}%^WGStem%>e*
* *ti̬000%>i̬*

tegemä+V+Act+Ind+Prs+Sg1: **do**
* *teg%^WGStem%>%{eõ%}*
* *ti̬00%>i̬*


* *k%{ei%}%{ei%}l%^VOWRaise%^PAL*
* *ki̬i̬ĺ00*


**õ2õ̭**
* *sõda%^WGStem*
* *sõ̭0a0*


**o2u̬**

**Vx%{ou%}:Vyo**
hoolas+A+Sg+Nom:
* *h%{ou%}%{ou%}la%{sØ%}%{back%}%^Pen%^VOWLower%^Pen%^G1*
* *hoolas00000*

**Vx%{ou%}2Vyu̬**
nuuĺ+N+Sg+Nom: **arrow**
* *n%{ou%}%{ou%}l%^VOWRaise%^PAL*
* *nu̬u̬ĺ*
* *k%{ei%}%{ei%}r%{dØ%}%{eØ%}%{lĺ%}%{front%}%^Pen%^VOWRaise%^Pen%^VowRM%>%{eõ%}%>m%{aä%}*
* *ki̬i̬rd0l00000%>e%>mä*

**i2e**
* *pin0i%^StrGStem%^PLPRT*
* *pinne00*
* *kiil%^VOWLower%>e*
* *keel0%>e*
* *leib%^ÄI2ÄÄ%^WGStem%>ä*
* *leev0%>ä*
* *pi%{tdØ%}ä%{front%}%^Pen%^VOWLower%^Pen%^WGStem%^VowRM%{eõ%}%>t%{aä%}s*
* *pe0000000e%>täs*


**i:ä**
* *päiv%^ÄI2ÄÄ%>ä*
* *pääv0%>ä*


**a2o**
```
* *kan0a%^StrGStem%^PLPRT*
* *kanno00*
```

**{ao}o**
```
* *ka%{nØ%}n%{ao%}%^G3%^PLPRT*
* *kanno00*
```



### VOWEL LOSS
**a:0**
       a _ (HarmDummies:) %>  i  ;  
* *saa%>i*
* *sa0%>i*
* *sõima0%^VowRM%>si*
* *sõim0s0%>si*
* *puhkas%^Pen%^VowRM%>a%>ma*
* *puhk0s00%>a%>ma*
sõda+N+Pl+Par:
* *sõ%{tØ%}%{tdØ%}a%^Pen%^G3%^VowRM%>o*
* *sõ0t0000%>o*

**ä:0**
* *jää%^VOWRaise%^VowRM%>i*
* *jä000%>i*
* *elä%>et*
* *el0%>et*
* *tütär%^Pen%^VowRM%>e*
* *tüt0r0%>e*

**u:0**
```
* *hirnu%{back%}%^Pen%^CC2C%^VowRM%>m%{aä%}*
* *hirn00000%>ma*
* *tervüs%^VowRM%^CnsRM%>i%>t*
* *terv0000%>i%>t*
juusk+N+Sg+Nom: ____
* *j%{ou%}%{ou%}s%{kØ%}u%^VOWRaise%^VowRM*
* *juusk000*

* *kuu%^VowRM%>i%>d*
* *ku00%>i%>d*
```

**ü:0**
```
* *tüü%^VowRM%>hüq*
* *tü00%>hüq*
* *tervüs%^VowRM%^WGStem%>i%>t*
* *terv0000%>i%>t*
```

**e:0**
* *herne%{hØ%}%{front%}%^VowRM%^WGStem%>id%{eõ%}*
* *hern00000%>ide*

**o:0**
* *joo%^VOWRaise%^VowRM%>vv%>aq*
* *ju000%>vv%>aq*

**Vx%{ou%}:0**
* *joo%^VOWRaise%^VowRM%>vv%>aq*
* *ju000%>vv%>aq*

**Vx%{äe%}:0 Passive stem vowel**


**ö:0**

**i:0**
hüdsi+N+Sg+Par:
* *hüdsi%^TS2S%^VowRM%>t*
* *hü0s000%>t*
* *aigo%^Pen%^WGStem*
* *a00o00*

* *va%^I7o%^StrGStem%>i*
* *vaio0%>0*
* *hä%^V70ö%^StrGStem%>i*
* *hävvü0%>0*


**õ:0**
* *tapõl%^Pen%^VowRMõ%>ma*
* *tap0l0õ%>ma*
* *kannõl%^StrGStem%^Pen%^VowRM%>õ*
* *kand0l00%>õ*
* *kogõr%^StrGStem%^Pen%^VowRM%>õ*
* *kok0r00%>õ*
* *hammõ%^WGStem%^VowRM%>ihe*
* *ham0000%>ihe*

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
* *kan%{dn%}õ%{lĺ%}%^Pen%^VowRM%^NoPAL%>%{XV%}*
* *kand0l000%>õ*

**%{XV%}:e**
käskmä+V+Act+Ind+Prs+Neg **command/käskeä**
* *käs%{kØ%}%{front%}%^WGStem%>%{eõ%}%-%{XV%}iq*
* *käs000%>e%-eiq*

**%{XV%}:i**


**i2j**
* *asi%^I2J%>a*
* *asj0%>a*
* *elläi%^Pen%^WGStem%^I2J%>ä*
* *el0äj00%>ä*

**%{ij%}:j**


**%{jiØ%}:j**

**%{jiØ%}:0**
vari+N+Sg+Gen: **shadow/varjo**
* *va%{rŕ%}%{jiØ%}o%^Pen%^PAL%^Pen%^WGStem*
* *vaŕ0o0000*

**%{jØ%}:0**
vari+N+Sg+Gen: **shadow/varjo**
* *va%{rŕ%}%{jiØ%}o%^Pen%^PAL%^Pen%^WGStem*
* *vaŕ0o0000*


**u2v**
* *juud%^WGStem%>a*
* *juvv0%>a*

**%{uv%}:v**
* *ju%{uv%}%{dv%}%^WGStem%>a*
* *juvv0%>a*
joudma+V+Act+Ind+Prt+Sg1
* *jõ%{uv%}%{dd́v%}back%^WGStem%>i*
* *jõvv00%>i*

**%{üv%}:v**
* *pü%{üv%}%{dd́v%}%^WGStem%>et*
* *püvv0%>et*
* *sü%{üv%}%{dv%}%^WGStem%>ä*
* *süvv0%>ä*

**%^I7:i**
* *va%^I7o%^StrGStem%>i*
* *vaio0%>0*

**%^I7:i**
* *hä%^V70ö%^StrGStem*
* *hävvü0*

CONSONANT
**%{pṕØ%}:ṕ**
* *pap%{pṕØ%}%{back%}%^G2%^PAL*
* *papṕ000*

**%{tt́Ø%}:t́**
* *täh%{tt́Ø%}%{front%}%^StrGStem%^PAL*
* *täht́000*

**%{kḱØ%}:ḱ**



SECONDARY CONSONANT LENGTHENING


**%{pØ%}:p**
```
* *hä%{pØ%}%{pbØ%}ü%^Pen%^XStrGStem*
* *häppü00*
* *tõ%{pØ%}%{pbv%}%{back%}%^XStrGStem%>%{eõ%}*
* *tõpp00%>õ*
* *se%{pØ%}p%^StrGStem*
* *sepp0*
* *nu%{pØ%}pu%{back%}%^Pen%^VOWRaise%^Pen%^StrGStem%^VowRM*
* *nupp0000000*
```

**%{tØ%}:t**
* *sõ%{tØ%}da%^XStrGStem%^PLPRT*
* *sõtto00*
* *si%{tØ%}t%{front%}%^StrGStem*
* *sitt00*
* *ü%{tØ%}te%^Pen%^StrGStem*
* *ütte00*
* *mü%{tØ%}tü%{front%}%^Pen%^VOWRaise%^Pen%^StrGStem%^VowRM*
* *mütt0000000*
sõda+N+Sg+Ill:
* *sõ%{tØ%}%{tdØ%}a%^Pen%^G3*
* *sõtta00*


**%{Øk%}:k**
* *ig0ä* `%^Pen%^XStrGStem`
* *ikkä0*
* *mak0õ%^StrGStem%^VowRM%>i%>dõ*
* *makkõ00%>i%>dõ*
* *mä%{Øk%}%{kgØ%}%{front%}%^XStrGStem%>%{eõ%}*
* *mäkk00%>e*


**%{XC%}:s**

**%{XC%}:l**

**%{XC%}:ĺ**

**%{XC%}:k**

**%{kḱ%}:ḱ**
kakma
* *ka%{kØ%}%{kḱ%}u%^VowRM%^PAL*
* *kakḱ000*


### Consonant weakening 

**kToZero**  
* *puhkas%^WGStem%>taq*
* *puh0as0%>taq*

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
* *su%{sØ%}śo%^Pen%^WGStem*
* *su0śo00*
* *ham%{bm%}a%{sØ%}%^Pen%^VOWRaise%^Pen%^StrGStem%^WGStem*
* *hamba000000*


**%{rØ%}:0**  
* *a%{rØ%}ro%^Pen%^G2*
* *a0ro00*





**%{nØ%}:0**  
* *su%{nØ%}ńo%^Pen%^WGStem*
* *su0ńo00*




**%{lØ%}:0**  
* *ta%{lØ%}lo%^Pen%^G2*
* *ta0lo00*



**%{mØ%}:0**  
* *su%{sØ%}śo%^Pen%^WGStem*
* *su0śo00*



**%{kØ%}:0**  
* *puhkas%^WGStem%>taq*
* *puh0as0%>taq*
nätsk+A+Sg+Gen
* *nä%{td%}s%{kØ%}%{front%}%^G1%>%{aä%}*
* *näds000%>ä*



* *i%{kØ%}kõ%{back%}%^Pen%^CC2C%^VowRM%>m%{aä%}*
* *i0k00000%>ma*

kakma:
* *ka%{kØ%}%{kḱ%}u%{back%}%^Pen%^CC2C%^VowRM%>m%{aä%}*
* *ka0k00000%>ma*

kõiḱ+Pron+Sg+Nom
* *kõi%{kØ%}%{kḱg%}%^CC2C%^PAL*
* *kõi0ḱ00*
* *ri%{kØ%}ka%{sØ%}%{back%}%^Pen%^VOWLower%^Pen%^WGStem*
* *ri0kas00000*
jõgi+N+Sg+Gen: **river/joki**
* *jõ%{kØ%}%{kgØ%}%{back%}%^G1%>%{eõ%}*
* *jõ0000%>õ*


**pToZero**
* *tapp%{back%}%^CC2C%>m%{aä%}*
* *tap000%>ma*

**%{pØ%}:0**
* *se%{pØ%}p%^WGStem*
* *se0p0*

* *tap%{pØ%}%{back%}%^CC2C%>m%{aä%}*
* *tap000%>ma*


**XØToZero**
agras+A+Sg+Gen
* *a%{kg%}ra%{sØ%}%{back%}%^Pen%^VOWRaise%^Pen%^G2%^WGStem*
* *akra0000000*
* *ve%{rØ%}rev%{front%}%^Pen%^WGStem%>%{aä%}*
* *ve0rev000%>ä*
elläi+N+Sg+Gen
* *e%{lØ%}lä%{ij%}%^Pen%^WGStem%^I2J%>ä*
* *e0läj00%>ä*
* *ha%{mØ%}mõ%{hØ%}%{back%}%^Pen%^WGStem*
* *ha0mõh%{back%}%^Pen%^WGStem*

**XØToSelf**
villui+A+Sg+Nom
* *vi%{lØ%}lui%{back%}%^Pen%^G3*
* *villui000*


kevväi+N+Sg+Gen: **spring**
* *ke%{vØ%}vä%{ij%}%^Pen%^WGStem%>ä*
* *ke0väj00%>ä*


**%{sØ%}:s**
ratas+N+Sg+Nom
* *ra%{tØ%}ta%{sØ%}%^Pen%^VOWLower%^Pen%^WGStem%^StrGStem*
* *ra0tas00000*

agras+A+Sg+Nom
* *a%{kg%}ra%{sØ%}%{back%}%^Pen%^VOWLower%^Pen%^WGStem%^StrGStem*
* *agras000000*

**%{hØ%}:h**
* *ha%{mØ%}mõ%{hØ%}%^Pen%^WGStem*
* *ha0mõ0%>h*


**%{kØ%}:k**
* *as%{kØ%}o%^Pen%^G2*
* *asko*

**%{pb%}:p**
* *kau%{pb%}%{õØ%}%{lĺ%}%{back%}%^Pen%^VOWRaise%^Pen%^StrGStem%^Pen%^VowRM%>%{eõ%}%>m%{aä%}*
* *kaup0l0000000%>õ%>ma*

* *li%{pb%}õ%^Pen%^G2*
* *lipõ00*


**%{t́d́%}:d́**

**%{t́d́%}:t́**


**%{td%}:t**
nätsk+A+Sg+Nom
* *nä%{td%}s%{kØ%}%{front%}%^G2*
* *nätsk00*
hõrts+N+Sg+Nom
* *hõr%{td%}so%^Pen%^VOWRaise%^Pen%^StrGStem%^VowRM*
* *hõrts000000*

**%{kg%}:k**
akaŕ+A+Sg+Nom
* *a%{kg%}a%{rŕ%}%{back%}%^Pen%^G2%^PAL*
* *akaŕ0000*
* *rän%{kg%}%{back%}%^G3*
* *ränk00*

* *avali%{kØ%}%{kg%}%{back%}%^G2*
* *avali0k00*

**%{kg%}:g**
apteḱ+N+Sg+Gen:
* *apte%{kØ%}%{kḱg%}%^VOWLower%^G1*
* *apte0g00%>i*
agras+A+Sg+Nom:
* *a%{kg%}ra%{sØ%}%{back%}%^Pen%^VOWLower%^Pen%^WGStem*
* *agras00000*
* *hõl%{kg%}a%{sØ%}%{back%}%^Pen%^G2*
* *hõlgas000*
* *rän%{kg%}%{front%}%^G2%{aä%}*
* *räng00ä*

nõkõś+N+Sg+Ill
* *nõ%{kg%}õ%{sś%}%^Pen%^WGStem%{XC%}%>õ%>he*
* *nõgõs00s%>õ%>he*

* *a%{kg%}ra%{sØ%}%{back%}%^Pen%^WGStem*
* *agras000*


**%{td%}:d**

kaotama+V+Act+Ind+Prs+Sg1:
* *kao%{td%}a%^Pen%^G2*
* *kaoda0*

**%{tt́d%}:d**
kergütämä+V+Act+Ind+Prs+Sg1:
* *kergü%{tt́d%}ä%^Pen%^WGStem*
* *kergüdä00*



**tToZero**
hüdsi+N+Sg+Par:
* *hüdsi%^TS2S%^VowRM%>t*
* *hü0s000%>t*

* *att%{back%}%^CC2C%>m%{aä%}*
* *at000%>ma*


**%{tØ%}:0**
* *puh%{tØ%}a%{sØ%}%^Pen%^WGStem*
* *puh0as*
ratas+N+Sg+Nom
* *ra%{tØ%}ta%{sØ%}%^Pen%^VOWLower%^Pen%^WGStem%^StrGStem*
* *ra0tas0000*

sõda+N+Sg+Gen:
* *sõ%{tØ%}%{tdØ%}a%^Pen%^G1*
* *sõ00a00*


### CONSONANT QUALITY CHANGE



**%{pṕb%}:b**
* *loro%{pṕb%}%^G2%>i*
* *lorob0%>i*

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


**%{kgØ%}:g**
jõgi+N+Sg+Nom
* *jõ%{kØ%}%{kgØ%}%{back%}%^G2%>i*
* *jõ0g00%>i*

**%{pbv%}:b**
* *tõ%{pØ%}%{pbv%}%{back%}%^G2i*
* *tõ0b00i*


hammas
* *ham%{bm%}a%{sØ%}%^Pen%^WGStem*
* *hammas00*

**%{bm%}:m**
* *ham%{bm%}a%{sØ%}%{back%}%^Pen%^VOWLower%^Pen%^WGStem%^StrGStem*
* *hammas0000*

**%{bm%}:b**
* *ham%{bm%}a%{sØ%}%^Pen%^VOWRaise%^Pen%^G2%^WGStem*
* *hamba000000*

**%{bv%}:v**
* *när%{bv%}ä%{sØ%}%^Pen%^VOWLower%^Pen%^WGStem*
* *närväs0000*
* *lei%{bv%}%^ÄI2ÄÄ%^G1%>ä*
* *leev0%>ä*



**%{dn%}:n**
kannõĺ+N+Sg+Nom: **kantele**
* *kan%{dn%}õ%{lĺ%}%^Pen%^WGStem%^PAL*
* *kannõĺ000*


**%{dl%}:l**
* *tul%>%{dl%}aq%^Pen%^WGStem*
* *tul%>laq00*
* *kõnõl%>%{dl%}aq%^Pen%^WGStem*
* *kõnõl%>laq00*
* *val%{dl%}%{back%}%^G1%>n*
* *vall00%>n*


**%{dv%}:v**
* *pü%{üv%}%{dv%}%^G1%>et*
* *püvv0%>et*
* *ju%{uv%}%{dv%}%^G1%>a*
* *juvv0%>a*
* *sü%{üv%}%{dv%}%^G1%>ä*
* *süvv0%>ä*



**dTot**
* *käd%^StrD2T%>t*
* *kät0%>t*
* *hüdsi%^StrD2T%>l*
* *hütsi0%>l*


**dTos**


**tTos**

**tTod**
kaotama+V+Act+Ind+Prs+Sg1: 
* *kaota%^Pen%^WGStem*
* *kaoda0*

There should always be a trigger



**%{dn%}:d**

* *kan%{dn%}õl%{back%}%^Pen%^G2%^Pen%^VowRM%>õ*
* *kand0l0000%>õ*


**j2i**

**{kḱg}:g**

kõiḱ+Pron+Sg+Gen
* *kõi%{kØ%}%{kḱg%}%{back%}%^G1%>%{eõ%}*
* *kõi0g00%>õ*


**k2g**
* *hõrak%^G1%>a*
* *hõrag0%>a*
* ★*hõrak%^G1%>a* (is not standard language)
* ★*hõrak0%>a* (is not standard language)
* *kisk%^G1%>%{uü%}%>t%{aä%}v*
* *kis0%>u%>tav*

* *süküs%^Pen%^WGStem%>e*
* *sügüs0%>e*



**gTok**
* *ig0ä%^XStrGStem*
* *ikkä0*
* *kogõr%^StrGStem%^Pen%^VowRM%>õ*
* *kok0r00%>õ*

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
* *kirotus%^CnsRM%>isi*
* *kirotu00%>isi*

usś+N+Sg+Par **door**
* *uss%^TS2S%>t*
* *us00%>t*

* *vassi%{back%}%^CC2C%^I2%^PAL%>m%{aä%}*
* *vaś00000%>ma*

**%{bv%}:b**
närväs+A+Sg+Gen:
* *när%{bv%}ä%{sØ%}%^Pen%^VOWLower%^Pen%^StrGStem%^WGStem*
* *närbä000000*

**%{gØ%}:g**
liig+A+Sg+Nom:
* *lii%{gØ%}%{back%}%^StrGStem*
* *liig00*
huug


**d20**
* *hüdsi%^TS2S%^VowRM%>te*
* *hü0s000%>te*

**%{dØ%}:0**


**g20**
* *särg%^WGStem%>#*
* *sär0e0%>0*
* *aig%^WGStem%>o*
* *a000%>o*
* *igä%^Pen%^WGStem*
* *i0ä00*
lugõma+V+Pss+PrfPrc **read/lukea**
* *lugõ%^Pen%^WGStem%^Õ2E%>t*
* *lo0e000%>t*
argnõma+V+Inf
* *arg%{back%}%{eõ%}%^Pen%^WGStemd%{aä%}q*
* *ar00õ00daq*

**%{gØ%}:0**
* *sär%{gØ%}%^WGStem%>e*
* *sär00%>e*
* *aig%^WGStem%>o*
* *a000%>o*
* *i%{kgØ%}ä%^Pen%^WGStem*
* *i0ä00*
lugõma+V+Pss+PrfPrc **read/lukea**
* *lu%{kgØ%}õ%^Pen%^WGStem%^Õ2E%>t*
* *lo0e000%>t*
argnõma+V+Inf
* *arg%{back%}%{eõ%}%^Pen%^WGStemd%{aä%}q*
* *ar00õ00daq*


* *palgõ%^WGStem%>h*
* *pal0õ0%>h*

**%{pbv%}:v**
* *tõ%{pØ%}%{pbv%}%{back%}%^G1%>%{eõ%}*
* *tõ0v00%>õ*


**%{pbØ%}:0**


**%{tdØ%}:0**
* *hüdsi%^TS2S%^VowRM%>te*
* *hü0s000%>te*


**%{kgØ%}:0**
* *mä%{kØ%}%{kgØ%}%{front%}%^G1%>%{eõ%}*
* *mä0000%>e*


* *u%{jØ%}jo%{back%}%^Pen%^WGStem%>m%{aä%}*
* *u0jo000%>ma*










püüdmä+V+Act+Ind+Prs+Sg3
* *pü%{üv%}%{dd́v%}%{front%}%^PAL*
* *püüd́00*


pereq
* *pe%{rØ%}re%^WGStem%>h*
* *pe0re0%>h*

naŕma
* *na%{rØ%}%{rŕ%}%{back%}%^CC2C%^PAL%>m%{aä%}*
* *na0r000%>ma*


### Other marks
* *ki%{pb%}õ%{nń%}%>a*
* *kipõn%>a*

**Disallow %^ErrorBack:0 in BHARM**

**Disallow %^ErrorBack:0 in BHARM**

