## Transcription Problems and Guidelines


### Multiple Letter Forms

Anglicana Formata, like other medieval bookhands, has multipe forms for certain letters. For example, the "s" can take either a kidney, sigma, or long shape:

| __Manuscript Image__ | Character Description |  __Furnivall's Transcription*__ | __Unicode Option__ | Our Transcription |
|:-----------:|:------------:|:-----------:| :-----------:|:-----------:|
|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/kidney_s.png?raw=true "kidney s") | kidney s | s | none | s |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/sigma_s.png?raw=true "sigma s") | sigma s | s | σ | s |
|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/long_s.png?raw=true "long s") | long s | s | ſ | s|

These different letter forms do not affect meaning in any way, but are either aesthetic or utilitarian; that is, they often depend on the place of "s" in a word or line (e.g. typically long-s can be either word-initial or word-final, whereas the kidney-shape s tends to be word-final, and the sigma only word-initial).

We can either transcribe these forms individually, or collapse them together.

Individually transcribing these forms is preferable if it helps the OCR system identify them correctly, and if our goal is produce a very conservative digital replication of the manuscript. However, if we were to transcribe these forms uniquely, we would use different Unicode characters for each form, and certain forms do not have a matching Unicode characters (see the kidney "s" above); while matching manuscript-character and Unicode-character is not necessary (we could edit machine-made transcriptions manually later), it is still desirable.  

Collectively transcribing these forms is preferable if our goal is create a digital edition of the manuscript that is accessible to a modern reader. As well, collapsing these forms is easier for creating training data (since it is tedious to insert special characters).

Since Kraken is able to collapse forms, and these varieties do not affect semantics, we will be collapsing them.

For more multiple letter forms, see this chart below:

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

### Lowercase and uppercase

It is often hard to distinguish between lowercase (minuscule) and uppercase (capital) letter forms. At times the scribe uses completely different graphs (for instance B and b, R and r, S and s); but often the distinction seems too subtle to be perceivable (for example, W and w, Þ and þ). Our reference, Furnivall's transcription, apparently distinguishes between capital and minuscule characters depending on their position; but we doubt that there are enough formal elements to justify this choice. Here are some examples

|Letter|Minuscule|Capital|
|:---|:---:|:---:|
|h|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/h_minuscule.png?raw=true "h minuscule")|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/h_capital.png?raw=true "h capital")|
|l|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/l_minuscule.png?raw=true "l minuscule")|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/l_capital.png?raw=true "l capital")|
|þ|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/thorn_minuscule.png?raw=true "þ minuscule")|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/thorn_capital.png?raw=true "þ capital")|
|v|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/v_minuscule.png?raw=true "v minuscule")|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/v_capital.png?raw=true "v capital")|
|w|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/w_minuscule.png?raw=true "w minuscule")|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/w_capital.png?raw=true "w capital")|
|y|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/y_minuscule.png?raw=true "y minuscule")|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/y_capital.png?raw=true "y capital")|
|ȝ|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/yogh_minuscule.png?raw=true "ȝ minuscule")|![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/yogh_capital.png?raw=true "ȝ capital")|

## Abbreviations

Medieval manuscripts have many abbreviations. Usually transcriptions will extend these abbreviations, marking the abbreviated letters with italics. Since Kraken requires diplomatic transcription (one-to-one characters), and abbreviations *do* carry semantic meaning (unlike the various letter forms above), we will be using special characters and diacritics to represent abbreviations. Certain choices here are quite obvious: for example, a macron

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
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/r%20with%20hook.png?raw=true "r with hook") | r with right hook suprascript | e (i.e. re) | r*e* | r&#777; | r̉ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/s%20with%20diagonal.png?raw=true "s with diagonal") | long s with diagonal stroke | ser | s*er* | ẜ (long s with diagonal stroke) | ẜ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/t%20with%20right%20hook%20.png?raw=true "t with right hook") | t with right hook suprascript | er (i.e. ter) | t*er* | t&#788; | t̔ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/thorn%20with%20right%20hook.png?raw=true "thorn with right hook") | thorn with right hook suprascript | er (i.e. þer) | þ*er* | þ̉ (hook diacritic) þ̔ (inverted comma diacritic)| þ̔ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/u%20macron.png?raw=true "u macron")| u with macron | n (i.e. un) | u*n* | ū | ū |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/u%20with%20macron%20and%20balls.png?raw=true "u with macron and balls") | u with macron and tilde | ra (i.e. ura) | u*ra* | ǖ (macron and diaeresis) | ǖ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/u%20with%20right%20hook%20.png?raw=true "u with right hook") | u with right hook suprascript | er (i.e. uer) | u*er* | ủ (hook diacritic) | ủ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/y%20macron.png?raw=true "y macron") | y with macron | n (i.e. yn) | y*n* | ȳ | ȳ |
| ![alt  text](https://github.com/gesaretto/paleo_ocr/blob/master/images/quod%20d.png?raw=true "quod d") | d with endstroke | quod | q*uo*d | qd (add nothing) | qd |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/tironian%20et.png?raw=true "tironian et") | tironian et | and | *and* | ⁊ | ⁊ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/paragraph.png?raw=true "paragraph") | paragraph marker | paragraph | ¶ | ¶ | ¶ |
| ![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/word%20bar.png?raw=true "word bar") | vertical bar | divides cramped words | nothing (space) | &#124; | &#124; |

## Temporary rules

1. If there's a unicode character, and the abbreviation definitely affects the word, use unicode character
2. If there's a unicode character, and the abbreviation does not affect the word, unclear
3. If there's not a unicode character, and the abbreviation affects the word, unclear
4. If there's not a unicode character, and the abbreviation does not affect the word, don't use anything


Useful Links:   
MUFI[http://folk.uib.no/hnooh/mufi/]  
Unicode and Macron[http://www.personal.psu.edu/ejp10/psu/gotunicode/macron.html]   

## Unicode HTML codes

(add semi-colon to end of codes)

comma diacritic = &#787   
hook diacritic = &#777
reverse comma diacritic = &#788   
double macron = &#862 or &#x35e
