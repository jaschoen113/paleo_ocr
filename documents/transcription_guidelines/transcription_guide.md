# Transcription Guidelines

Our transcription rules in brief:

1. Our transcription collapses multiple letter forms with identical meaning.
2. Our transcription renders miniscule "should-be" capitals as minuscule letters.
3. Our transcription does not expand abbreviations, but rather marks them with Unicode diacritics.  


### Overview

As we compile our training transcriptions, it is essential that we have consistent rules for rendering letters and abbreviations. However, part of what makes medieval handwriting so challenging for OCR is its various letter forms and obscure abbreviations. We have identified three primary transcriptions "issues" for our manuscript: 1) multiple letter forms 2) lowercase letters used in uppercase instances 3) extensive abbreviations. We discuss these issues in detail below, and also explain how we handle them in our transcription.    

## Multiple Letter Forms

Anglicana formata, like other medieval bookhands, has multiple forms for certain letters. For example, the "s" can take either a kidney, sigma, or long shape:

| __Manuscript Image__ | Character Description |  __Furnivall's Transcription__ | __Unicode Option__ | Our Transcription |
|:-----------:|:------------:|:-----------:| :-----------:|:-----------:|
|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/kidney_s.png?raw=true "kidney s") | kidney s | s | none | s |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/sigma_s.png?raw=true "sigma s") | sigma s | s | σ | s |
|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/long_s.png?raw=true "long s") | long s | s | ſ | s|

These different letter forms do not affect meaning in any way, but are either aesthetic or functional; that is, they often depend on the place of "s" in a word or line (e.g. typically long-s can be either word-initial or word-final, whereas the kidney-shape s tends to be word-final, and the sigma only word-initial).

We can either transcribe these forms individually, or collapse them together.

Individually transcribing these forms is preferable if it helps the OCR system identify them correctly, and if our goal is produce a very conservative digital replication of the manuscript. However, if we were to transcribe these forms uniquely, we would use different Unicode characters for each form, and certain forms do not have a matching Unicode characters (see the kidney "s" above); while matching manuscript-character and Unicode-character is not necessary (we could edit machine-made transcriptions manually later), it is still desirable.  

Collectively transcribing these forms is preferable if our goal is to create a digital edition of the manuscript that is accessible to a modern reader. As well, collapsing these forms is easier for creating training data (since it is tedious to insert special characters).

Since Kraken is able to collapse forms, and these varieties do not affect semantics, **we will be collapsing them.**

For more examples of multiple letter forms, see the below chart, as well as our full character [guide](https://github.com/gesaretto/paleo_ocr/blob/master/transcription_guidelines/Scribe%20D%20Letters%20Guide.pdf) for Scribe D:

| __Manuscript Image__ | Character Description |  __Furnivall's Transcription__ | __Unicode Option__ | Our Transcription |
|:-----------:|:------------:|:-----------:| :-----------:|:-----------:|
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/d_looped.png?raw=true "d open loop") | d open loop| d | none | d |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/d_regular.png?raw=true "d closed loop") | d closed loop| d | none | d |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/e_chickpea.png?raw=true "chickpea e") | chickpea e | e | none | e |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/e_regular.png?raw=true "regular e") | regular e | e | e | e |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/f%20tick.png?raw=true "f tick") | f with tick | adds a tick | none | f |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/biting%20fs.png?raw=true "biting fs")| biting f's | ﬀ (connected stroke) | ﬀ (connected stroke) | ff (disconnected strokes) |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/extended%20g.png?raw=true "extended g") | g with extended stroke | adds tick | none | g |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/biting%20ps.png?raw=true "biting p") | biting p's | pp | none | pp |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/r_2_shaped.png?raw=true "2 r") | 2-shaped r | r | 2 | r |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/r_minuscule.png?raw=true "miniscule r") | miniscule r | r | r | r |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/r_split.png?raw=true "split r") | split r | r | none | r |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/t%20tick.png?raw=true "t tick") | t with tick |  adds a tick | none | t |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/y%20dot.png?raw=true "y dot") | y dot | y | ẏ | y |

## Lowercase and Uppercase

It is often hard to distinguish between lowercase (minuscule) and uppercase (capital) letter forms. At times the scribe uses completely different graphs (for instance **B** and **b**, **R** and **r**, **S** and **s**); but often the distinction seems too subtle to be perceivable (for example, **W** and **w**, **Þ** and **þ**). We may assume from location or semantic context that a letter is "meant" to be a capital, for example in a proper name or at the beginning of a line. And accordingly, our reference, Furnivall, often marks a capital where the manuscript presents a miniscule form.
But it will be difficult (if not impossible) for an OCR system to identify such a distinction, at least without a certain level of language processing. Additionally, the scribe often shades uppercase letters slightly to mark their capital form, but this shading will not be visible to Kraken, which receives a binarized (black and white) photo.  

Here are some examples:

|Letter|Minuscule|Shaded Capital|
|:---|:---:|:---:|
|h|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/h_minuscule.png?raw=true "h minuscule")|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/h_capital.png?raw=true "h capital")|
|l|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/l_minuscule.png?raw=true "l minuscule")|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/l_capital.png?raw=true "l capital")|
|þ|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/thorn_minuscule.png?raw=true "þ minuscule")|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/thorn_capital.png?raw=true "þ capital")|
|v|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/v_minuscule.png?raw=true "v minuscule")|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/v_capital.png?raw=true "v capital")|
|w|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/w_minuscule.png?raw=true "w minuscule")|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/w_capital.png?raw=true "w capital")|
|y|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/y_minuscule.png?raw=true "y minuscule")|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/y_capital.png?raw=true "y capital")|
|ȝ|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/yogh_minuscule.png?raw=true "ȝ minuscule")|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/yogh_capital.png?raw=true "ȝ capital")|

In addition, there *are* formal capitals for certain letters like **V**, **H** and **D**, but often the scribe uses the miniscule forms instead. By contrast, **Þ**, **Ȝ**, **W**, **Y** (above) do not seem to have distinct capital forms, nor do **J**, **K**, **U**, **X**, or **Z**. For capital **F**, the scribe uses a double f, which we will transcribe ff. An expanded chart of Scribe D's character forms can be found [here](https://github.com/gesaretto/paleo_ocr/blob/master/transcription_guidelines/Scribe%20D%20Letters%20Guide.pdf).

Because such differences between miniscule and capital appear negligible, and will probably be difficult for the machine to discern, we will be transcribing such characters in their lowercase form. **Moreover, any character that "should" be a capital (semantically or positionally), but *looks* nearly or totally indistinguishable from the miniscule, will be transcribed as a miniscule**. To see examples of "proper" capitals and miniscules, consult the expanded character [chart](https://github.com/gesaretto/paleo_ocr/blob/master/transcription_guidelines/Scribe%20D%20Letters%20Guide.pdf).

Note: We have also found one example of a **V** occuring in **v** position, and in align with our rule above, are transcribing it as **V** ("aVys" on folio 26v, line 35).

## Abbreviations

Medieval manuscripts have many abbreviations. Usually transcriptions will extend these abbreviations, marking the abbreviated letters with italics. However, since Kraken requires diplomatic transcription (one-to-one characters), we can not extend the abbreviations in our training data. And since abbreviations *do* carry semantic meaning (unlike the various letter forms above), we will be using special characters and diacritics to represent abbreviations.

Certain diacritic choices here are quite obvious: for example, a macron over an **o** can be easily represented with **ō**. Other abbreviations have no corresponding Unicode character (see, for example, **p**s with right hook and left hook suprascripts). For these forms, we use Unicode diacritics that most closely resemble the abbreviations. We have also tried to be as consistent as possible with these abbreviations: for example, we use the same diacritic for the right hook ("er" or "re" abbreviation) over the **p**, **n**, **t**, **þ**, and **u**.  

### Middle English Abbreviations

#### Uniform Middle English Abbreviations:

##### "er" loop abbreviation  
hook diacritic = &#777

This symbol resembles the certain variations of the medieval Latin abbreviation for "er/ar/re." In our manuscripts, it mainly stands in for "er," though occasionally takes on other meanings (noted below. For a discussion of its Latin counterpart, See Capelli pp. 19-29, specifically sections 4.3-4.35.

| Manuscript Image | Character | Notes |
| :----: | :----: | :---: |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/d%20with%20left%20hook.png?raw=true) | d&#777; |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/e%20with%20hook%20.png?raw=true "e with right hook") | e&#777; |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/g%20with%20left%20hook%20.png?raw=true "g with left hook") | g&#777; |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/m_right_hook.png?raw=true "m with hook")| m&#777; M&#777;| also *ir* |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/n%20with%20right%20hook.png?raw=true "n with right hook") | n&#777; |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/p%20with%20right%20hook%20.png?raw=true "p with right hook ") | p&#777; | also *re* |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/r%20with%20hook.png?raw=true "r with hook") | r̉ | mainly just *e* |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/s%20with%20right%20hook%20.png?raw=true "s with left hook") ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/s%20with%20diagonal.png?raw=true "s with diagonal loop") | s̉ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/t%20with%20right%20hook%20.png?raw=true "t with right hook") | t&#777; |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/thorn%20with%20right%20hook.png?raw=true "thorn with right hook") | þ&#777; |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/u%20with%20right%20hook%20.png?raw=true "u with right hook") | u&#777; |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/v_right_hook.png?raw=true "v right hook") | v&#777; |
| ![alt text](https://raw.githubusercontent.com/gesaretto/paleo_ocr/master/abbreviation_images/y_right_hook.png "y with right hook") | y&#777; |

##### "ri" small 2-shaped abbreviation  

zig zag diacritic = &#859  

This symbol most closely resembles the Latin 2-shaped abbreviation, often used for *u* or *a* (see Capelli pages 29-30, section 4.4-4.41). However in our manuscripts it almost always stands for "ri."  

| Manuscript Image | Character | Notes |
| :----: | :----: | :---: |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/c_2.png?raw=true "c with 2") | c&#859; |
| missing image? | g&#859; |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/p%20with%20left%20hook.png?raw=true "p with left hook")| p&#859; |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/t_2.png?raw=true "t with 2") | t&#859; | also ir or er |

##### "ra" upward facing wavy line

diaeresis diacritic = &#776

This symbol closely resembles the Latin "r/re/ra/ar" wavy line abbreviation. As Capelli notes, in the 14th and 15th century this symbol develops into a broken bar or two dots closely spaced, and we see a similar ball-type form in some instances below (see Capelli pp. 13-16, specifically sections 3.4-3.42). Given limited wavy-line options in Unicode, we have chosen to represent the abbreviation by its late form, with two balls.

| Manuscript Image | Character |
| :----: | :----: |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/g%20with%20tilde%20.png?raw=true "g with tilde") ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/g%20macron%20balls.png?raw=true "g with macron balls") | g&#776; |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/n%20with%20tilde.png?raw=true "n with tilde") | n&#776; |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/p_balls.png?raw=true "p with balls") | p&#776; |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/u%20with%20macron%20and%20balls.png?raw=true "u with macron and balls") ![alt text](https://raw.githubusercontent.com/gesaretto/paleo_ocr/master/abbreviation_images/u_with_balls.png "u with balls")| u&#776; |


##### "ur" downward facing wavy line

tilde diacritic = &#771

This symbol most closely resembles a version of the Latin "ur/tur/er" abbreviation, which Capelli describes as a "2" or "S" on its side (see Capelli pp.13-117, 3.5). In our English manuscripts, this symbol looks more like an inversion of the "ra" symbol (above) than a "2" or "S." We have chosen to represent this abbreviation with a tilde, which is closest to its form.

| Manuscript Image | Character |
| :----: | :----: |
| ![alt text](https://raw.githubusercontent.com/gesaretto/paleo_ocr/master/abbreviation_images/e_with_tilde.png "e with tilde") | ẽ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/o%20with%20tilde.png?raw=true "o with tilde") | õ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/t_tilde.png?raw=true "t tilde") | t&#771; |  

##### "n/m" macron

macron = 	&#772

In most, the macron is used, as in Latin, to represent a missing "m" or "n." In some cases, it represents "u" (for example when placed over an "n").   

| Manuscript Image | Character |
| :----: | :----: |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/e%20with%20macron.png?raw=true "e with macron") | ē |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/macron%20m.png?raw=true "macron over m") | m̄ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/o%20with%20macron,%20middle%20of%20word.png?raw=true "o with macron middle of word") | ō |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/macron%20over%20on.png?raw=true "macron over n") | n̄ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/u%20macron.png?raw=true "u macron")| ū |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/y%20macron.png?raw=true "y macron") | ȳ |

#### Discrete Middle English Abbreviations

| Manuscript Image | Description | Meaning  | Character | Unicode |
|:-----------:|:-----------:|:------------:|:-----------:| :------: |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/d_downstroke.png?raw=true "d downstroke")| d with downstroke | is (e.g. d*is*) or e (e.g. d*e*)| ɖ | &#598 |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/h%20cross.png?raw=true "h cross stroke") | h with cross stroke | et (e.g. h*et*) | ħ | &#295 |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/e%20with%20hook.png?raw=true "e with hook") | e with small stroke |  m or n (e.g. e*m*) | e&#700; | e&#700 |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/g_dot.png?raw=true "g with dot") | g with dot | ro (g*ro*) | g&#730; | g&#730 |
|![alt text](https://raw.githubusercontent.com/gesaretto/paleo_ocr/master/abbreviation_images/l_with_cross_stroke.png "l with cross stroke")|l with cross stroke| ett (e.g. l*ett*) or is (e.g. l*is*) or e (e.g. *e*l or l*e*)| ꝉ | &#42825 |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/welsh%20l.png?raw=true "welsh l")| welsh l | e (e.g. ll*e*) | ỻ | &#7931 |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/p%20underscore.png?raw=true "P with underscore")| p with stroke through descender | er or ar (e.g. p*er* or p*ar*) | ꝑ and Ꝑ | &#42833 &#42832 |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/p%20with%20back%20hook%20.png?raw=true "p with back loop") | p with loop on descender | ro (e.g. p*ro*) | ꝓ | &#42835 |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/thorn_u.png?raw=true "thorn with u") | thorn with u diacritic | þou | þ&#871; | þ&#871 |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/w%20with%20t.png?raw=true "w with t") | w with t suprascript | with | w&#877; | w&#877 |

### Latin Abbreviations

| Manuscript Image | Description | Meaning  | Character | Unicode |
|:-----------:|:-----------:|:------------:|:-----------:|:-----:|
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/a_dot.png?raw=true "a with dot") | a with dot | ?  | a&#730; | a&#730 |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/c%20wih%20macron%20.png?raw=true "c with macron") | c with macron | an - t (e.g. *an*c*t*)| c̄ | c&#772 |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/d_shoulder.png?raw=true "d with shoulder") | d with shoulder | aui (e.g. d*aui*d) | d&#702; | d&#702 |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/d_um.png?raw=true "d with line") | d with vertical line | um  (e.g. d*um*) | ? |?  |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/h_dot.png?raw=true "h with dot") | h with dot | hoc | h&#778; | h&#778 |
| missing image? | h with comma? | es (i.e. Ih*es*u) |  h&#777; | h&#777 |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/macron%20i.png?raw=true "macron i")| macron i | mn (e.g. *mn*i) | ī | i&#772 |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/p%20tilde.png?raw=true "p tilde") | p with tilde | ur (e.g. p*ur*)| p̃ | p&#771 |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/t_2again.png?raw=true "Latin t with 2") | t with 2-shaped tilde | ur (e.g. t*ur*)| t&#771; | t&#771 |
| missing image? | t with macron | us (e.g. t*us*) | t̄ | t&#772 |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/Latin%20con.png?raw=true "con") | character resembling 9 | con | ꝯ | &#42863 |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/Latin%20um%20.png?raw=true "Latin rum") | character resembling 4 or y with strike through | rum | ɏ | &#591 |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/us.png?raw=true "us") | character resembling 3 | us (e.g.  b*us*) | ꝫ | &#42859 |
| ![alt  text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/quod%20d.png?raw=true "quod d") | q plus d with endstroke | quod | qɖ | qd&#598 |
| ![alt text](https://raw.githubusercontent.com/gesaretto/paleo_ocr/master/abbreviation_images/q_for_quod.png "quod q") | q with right hook | quod | ꝙ | &#42841 |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/tironian%20et.png?raw=true "tironian et") | tironian et | and | ⁊ | &#8266 |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/et%20cetera%20.png?raw=true "et cetera") | tironian et + c with left hook | et cetera | ⁊c&#777; | ⁊c&#777 |

### Additional Abbreviations

| Manuscript Image | Description | Meaning  | Character |
|:-----------:|:-----------:|:------------:|:-----------:|
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/paragraph.png?raw=true "paragraph") | paragraph marker | new paragraph| ¶ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/abbreviation_images/word%20bar.png?raw=true "word bar") | vertical bar | divides cramped words | &#124; |
| missing image? | punctus elevatus (looks like inverted semi-colon) | pause | ؛ |

### Citations  

"Furnivall's transcription" refers to *The Corpus MS of Chaucer's Canterbury Tales* ed. by Frederick J. [Furnivall](https://babel.hathitrust.org/cgi/pt?id=uva.x030198621;view=1up;seq=25), a print transcription of MS 198 from 1868-79


### Unicode Resources

[MUFI](http://folk.uib.no/hnooh/mufi/)  
[Unicode and Macron](http://www.personal.psu.edu/ejp10/psu/gotunicode/macron.html)  
[Unicode Table](https://unicode-table.com/en/#ipa-extensions)

### Unicode HTML Codes

(add ; to end of code to create character)

comma diacritic = &#787   
hook diacritic = &#777  
reverse comma diacritic = &#788   
double macron = &#862 or &#x35e    
macron = &#772  
small t diacritic = &#877  
