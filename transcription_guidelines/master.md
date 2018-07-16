## Transcription  Questions, Problems, and Current Rules

tl;dr: Our transcription rules are as follows:

1. Our transcription collapses multiple letter forms with identical meaning.
2. Our transcription renders miniscule "should-be" capitals as minuscule letters.
3. Our transcription does not expand abbreviations, but rather marks them with Unicode diacritics.  


### Overview

As we compile our training transcriptions, it is essential that we have consistent rules for rendering letters and abbreviations. However, part of what makes medieval handwriting so challenging for OCR is its various letter forms and obscure abbreviations. We have identified three primary transcriptions "issues" for our manuscript: 1) multiple letter forms 2) lowercase letters used in  uppercase instances 3) extensive abbreviations. We discuss these issues in detail below, and also explain how we will handle them in our transcription.    

### Multiple Letter Forms

Anglicana formata, like other medieval bookhands, has multipe forms for certain letters. For example, the "s" can take either a kidney, sigma, or long shape:

| __Manuscript Image__ | Character Description |  __Furnivall's Transcription__ | __Unicode Option__ | Our Transcription |
|:-----------:|:------------:|:-----------:| :-----------:|:-----------:|
|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/kidney_s.png?raw=true "kidney s") | kidney s | s | none | s |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/sigma_s.png?raw=true "sigma s") | sigma s | s | σ | s |
|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/long_s.png?raw=true "long s") | long s | s | ſ | s|

These different letter forms do not affect meaning in any way, but are either aesthetic or functional; that is, they often depend on the place of "s" in a word or line (e.g. typically long-s can be either word-initial or word-final, whereas the kidney-shape s tends to be word-final, and the sigma only word-initial).

We can either transcribe these forms individually, or collapse them together.

Individually transcribing these forms is preferable if it helps the OCR system identify them correctly, and if our goal is produce a very conservative digital replication of the manuscript. However, if we were to transcribe these forms uniquely, we would use different Unicode characters for each form, and certain forms do not have a matching Unicode characters (see the kidney "s" above); while matching manuscript-character and Unicode-character is not necessary (we could edit machine-made transcriptions manually later), it is still desirable.  

Collectively transcribing these forms is preferable if our goal is to create a digital edition of the manuscript that is accessible to a modern reader. As well, collapsing these forms is easier for creating training data (since it is tedious to insert special characters).

Since Kraken is able to collapse forms, and these varieties do not affect semantics, **we will be collapsing them.**

For more examples of multiple letter forms, see the below chart, as well as our full character [guide](https://github.com/gesaretto/paleo_ocr/blob/master/transcription_guidelines/Scribe%20D%20Letters%20Guide.pdf) for Scribe D:

| __Manuscript Image__ | Character Description |  __Furnivall's Transcription__ | __Unicode Option__ | Our Transcription |
|:-----------:|:------------:|:-----------:| :-----------:|:-----------:|
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/d_looped.png?raw=true "d open loop") | d open loop| d | none | d |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/d_regular.png?raw=true "d closed loop") | d closed loop| d | none | d |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/e_chickpea.png?raw=true "chickpea e") | chickpea e | e | none | e |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/e_regular.png?raw=true "regular e") | regular e | e | e | e |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/f%20tick.png?raw=true "f tick") | f with tick | adds a tick | none | f |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/biting%20fs.png?raw=true "biting fs")| biting f's | ﬀ (connected stroke) | ﬀ (connected stroke) | ff (disconnected strokes) |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/extended%20g.png?raw=true "extended g") | g with extended stroke | adds tick | none | g |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/h%20cross.png?raw=true "h cross") | h with stroke | ħ | ħ | h |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/h_regular.png?raw=true "normal h") | normal h | h | h | h |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/welsh%20l.png?raw=true "welsh l") | Welsh l | ỻ | ỻ | ll |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/biting%20ps.png?raw=true "biting p") | biting p's | pp | none | pp |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/r_2_shaped.png?raw=true "2 r") | 2-shaped r | r | 2 | r |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/r_minuscule.png?raw=true "miniscule r") | miniscule r | r | r | r |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/r_split.png?raw=true "split r") | split r | r | none | r |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/t%20tick.png?raw=true "t tick") | t with tick |  adds a tick | none | t |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/y%20dot.png?raw=true "y dot") | y dot | y | ẏ | y |

### Lowercase and Uppercase

It is often hard to distinguish between lowercase (minuscule) and uppercase (capital) letter forms. At times the scribe uses completely different graphs (for instance **B** and **b**, **R** and **r**, **S** and **s**); but often the distinction seems too subtle to be perceivable (for example, **W** and **w**, **Þ** and **þ**). We may assume from location or semantic context that a letter is "meant" to be a capital, for example in a proper name or at the beginning of a line. And accordingly, our reference, Furnivall, often marks a capital where the manuscript presents a miniscule form.
But it will be difficult (if not impossible) for an OCR system to identify such a distinction, at least without a certain level of language processing. Additionally, the scribe often shades uppercase letters slightly to mark their capital form, but this shading will not be visible to Kraken, which receives a binarized (black and white) photo.  

Here are some examples:

|Letter|Minuscule|Shaded Capital|
|:---|:---:|:---:|
|h|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/h_minuscule.png?raw=true "h minuscule")|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/h_capital.png?raw=true "h capital")|
|l|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/l_minuscule.png?raw=true "l minuscule")|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/l_capital.png?raw=true "l capital")|
|þ|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/thorn_minuscule.png?raw=true "þ minuscule")|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/thorn_capital.png?raw=true "þ capital")|
|v|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/v_minuscule.png?raw=true "v minuscule")|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/v_capital.png?raw=true "v capital")|
|w|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/w_minuscule.png?raw=true "w minuscule")|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/w_capital.png?raw=true "w capital")|
|y|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/y_minuscule.png?raw=true "y minuscule")|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/y_capital.png?raw=true "y capital")|
|ȝ|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/yogh_minuscule.png?raw=true "ȝ minuscule")|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/yogh_capital.png?raw=true "ȝ capital")|

Because these differences appear negligible, and will probably be difficult for the machine to discern, we will be transcribing such characters in their lowercase form.

Note: there are formal capitals for **V** for and **H**, but often the scribe uses the miniscule forms instead. **L**, **Þ**, **Ȝ**, **W**, **Y** (above) do not seem to have distinct capital forms, nor do **J**, **K**, **U**, **X**, or **Z**. For capital **F**, the scribe uses a double f, which we will transcribe ff. An expanded chart of Scribe D's character forms can be found [here](https://github.com/gesaretto/paleo_ocr/blob/master/transcription_guidelines/Scribe%20D%20Letters%20Guide.pdf).

As well, these two forms are somewhat ambiguous:

|Letter| Potential Capital | Note |
|:---:|:---:| :----: |
| h | ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/uppercase%20h2.png?raw=true "big h") | significantly larger and slightly different in shape compared to other **h**s |
| d | ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/uppercase%20D.png?raw=true "extended d") | extended loop compared to other **d**s, and Mooney identifies this as as capital **D** |

Given that these two forms appear exaggerated enough, and especially that this **D** has been identified by paleographers as a capital (see Late Medieval English Scribal Profile of Scribe D), we will be transcribing these two forms as capitals.

**In conclusion, any character that "should" be a capital (semantically or geographically), but *looks* nearly or totally indistinguishable from the the miniscule, will be transcribed as a miniscule**. To see examples of "proper" capitals and miniscules, consult the expanded character [chart](https://github.com/gesaretto/paleo_ocr/blob/master/transcription_guidelines/Scribe%20D%20Letters%20Guide.pdf).

### Abbreviations

Medieval manuscripts have many abbreviations. Usually transcriptions will extend these abbreviations, marking the abbreviated letters with italics. However, since Kraken requires diplomatic transcription (one-to-one characters), we can not extend the abbreviations in our training data. And since abbreviations *do* carry semantic meaning (unlike the various letter forms above), we will be using special characters and diacritics to represent abbreviations.

Certain diacritic choices here are quite obvious: for example, a macron over an **o** can be easily represented with **ō**. Other abbreviations have no corresponding Unicode character (see, for example, **p**s with right hook and left hook suprascripts). For these forms, we use Unicode diacritics that most closely resemble the abbreviations. We have also tried to be as consistent as possible with these abbreviations: for example, we use the same diacritic for the right hook ("er" or "re" abbreviation) over the **p**, **n**, **t**, **þ**, and **u**.  

| __Manuscript Image__ | Abbreviation Description | Abbreviation Extension | __Furnivall's Transcription__ | __Alternative Option__ | Temporary Rule |
|:-----------:|:-----------:|:------------:|:-----------:| :-----------:|:-----------:|
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/us.png?raw=true "us") | character resembling 3 | us (i.e. bus)| b*us* | ꝫ (Latin small et) | ꝫ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/e%20with%20hook.png?raw=true "e with hook") | e with suprascript |  m (i.e. em) | e*m* | ẻ (e with hook diacritic) | ẻ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/e%20with%20macron.png?raw=true "e with macron") | e with macron | n (i.e. en) | e*n* | ē | ē |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/g%20with%20tilde%20.png?raw=true "g with tilde") ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/g%20macron%20balls.png?raw=true "g with macron balls") | g with tilde or with macron and tilde | ra (i.e. gra) | g*ra* | g̃ | g̃ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/macron%20m.png?raw=true "macron over m") | m with macron | m (i.e. mm) | m*m* | m̄ | m̄ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/macron%20over%20on.png?raw=true "macron over on") | macron over on or n| u (i.e. oun) | n̄ | ōn̄ (over o as well)| n̄ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/n%20with%20tilde.png?raw=true "n with tilde") | n with tilde | ra (i.e. ran) | *ra*n | ñ | ñ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/n%20with%20right%20hook.png?raw=true "n with right hook") | n with right hook suprascript | er (i.e. ner) | n*er* | n&#788; (inverted comma diacritic) | n&#788; |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/o%20with%20macron,%20middle%20of%20word.png?raw=true "o with macron middle of word") | macron over o | m (i.e. om) | o*m* | ō | ō |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/o%20with%20tilde.png?raw=true "o with tilde") | o with tilde | ur (i.e. our) | o*ur* | õ | õ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/p%20underscore.png?raw=true "P with underscore")| p with stroke through descender | er or ar (i.e. per or par) | p*er* or p*ar* | ꝑ | ꝑ and Ꝑ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/p%20with%20right%20hook%20.png?raw=true "p with right hook ") | p with right hook suprascript | er (i.e. per) or re (i.e. pre) | p*er* or p*re* | p̔ (inverted comma diacritic)  | p̔ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/p%20with%20left%20hook.png?raw=true "p with left hook")| p with left hook suprascript | pri | p*ri* | p̓ (comma diacritic) p̉ (hook diacritic) | p̉ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/p%20with%20back%20hook%20.png?raw=true "p with back loop") | p with loop on descender | ro (i.e. pro) | p*ro* | ꝓ (p with flourish) | ꝓ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/r%20with%20hook.png?raw=true "r with hook") | r with left hook suprascript | e (i.e. re) | r*e* | r&#777; | r̉ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/s%20with%20diagonal.png?raw=true "s with diagonal") | long s with diagonal stroke | ser | s*er* | ẜ (long s with diagonal stroke) | ẜ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/t%20with%20right%20hook%20.png?raw=true "t with right hook") | t with right hook suprascript | er (i.e. ter) | t*er* | t&#788; | t̔ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/thorn%20with%20right%20hook.png?raw=true "thorn with right hook") | thorn with right hook suprascript | er (i.e. þer) | þ*er* | þ̔ (inverted comma diacritic)| þ̔ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/u%20macron.png?raw=true "u macron")| u with macron | n (i.e. un) | u*n* | ū | ū |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/u%20with%20macron%20and%20balls.png?raw=true "u with macron and balls") | u with macron and tilde | ra (i.e. ura) | u*ra* | ǖ (macron and diaeresis) ũ | ũ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/u%20with%20right%20hook%20.png?raw=true "u with right hook") | u with right hook suprascript | er (i.e. uer) | u*er* | ủ (hook diacritic) u&#788; (inverted comma diacritic) | u&#788; |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/y%20macron.png?raw=true "y macron") | y with macron | n (i.e. yn) | y*n* | ȳ | ȳ |
| ![alt  text](https://github.com/gesaretto/paleo_ocr/blob/master/images/quod%20d.png?raw=true "quod d") | d with endstroke | quod | q*uo*d | qd (add nothing) | qd |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/tironian%20et.png?raw=true "tironian et") | tironian et | and | *and* | ⁊ | ⁊ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/paragraph.png?raw=true "paragraph") | paragraph marker | paragraph | ¶ | ¶ | ¶ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/word%20bar.png?raw=true "word bar") | vertical bar | divides cramped words | nothing (space) | &#124; | &#124; |

"Furnivall's transcription" refers to *The Corpus MS of Chaucer's Canterbury Tales* ed. by Frederick J. [Furnivall](https://babel.hathitrust.org/cgi/pt?id=uva.x030198621;view=1up;seq=25), a print transcription of MS 198 from 1868-79


### Unicode Resources
[MUFI](http://folk.uib.no/hnooh/mufi/)  
[Unicode and Macron](http://www.personal.psu.edu/ejp10/psu/gotunicode/macron.html)  

### Unicode HTML Codes

(add semi-colon to end of codes)

comma diacritic = &#787   
hook diacritic = &#777
reverse comma diacritic = &#788   
double macron = &#862 or &#x35e
