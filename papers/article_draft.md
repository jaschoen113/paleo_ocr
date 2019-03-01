---
title: "Outlines for Article Draft"
date: Spring 2019
author: J. Schoen & G. E. Saretto
---

1. Summary of results before everything else? Sort of an abstract?

1. Background section;

    - [Introduction to OCR;]
        - machine learning for OCR;
    - previous attempts;
        - main problems (for now hint at them, then treat in the following sections);
    - the choice of Kraken; advantages.

2. Method.

    - Selection of scribe and MSS. Previous work on the scribe.

    - Main problems that have been encountered.

    -

2. Training and transcription.

3. Tests; choice of additional MSS.

4. Retraining.

---

### New Outline (Feb. 19)

1. Introduction to OCR for medieval MSs (Jenna)

    - Work done so far; challenges encountered; changes in technology

    - Purposes of the project; stakes of the project;

        - How many documents have not been edited? How many documents are not available in digital form?

        - What else would the technology allow to do? (E.g.: make .pdfs searchable)

2. Introduction to Scribe D as a model/test subject (Gianmarco)

    - Several MSs, some of which digitized

    - Work done so far on Scribe D?

    - “Quintessential anglicana cursiva hand”

3. Selection of texts for corpus (Gianmarco)

    - Description of MSs in the corpus; challenges

4. Process (steps involved) (Jenna)

    - Hint at abbreviations

5. Results

    - Interpreting the results?

6. Challenges? (<---)

    - The problem of abbreviations; getting medievalists involved ...?

### Hypothetical Outline

|words|paragraphs|pages|
|:---|:---|:---|
|4,000|13|16|

1. Introduction. The context; the challenge; the purpose.

    - In the past few decades, the field of medieval studies has been greatly affected by the rise of digital editions and the increased availability of on-line facsimiles. Thanks to comprehensive databases like--among others--Digital Scriptorium (...Footnote...), the Bibliothèque Virtuelle des Manuscripts Médiévaux (...Footnote...), or Manus Online (...Footnote...), students and scholars of the Middle Ages can now easily access hundreds of digitized manuscripts and thousands of high-quality images, from virtually any room where an Internet connection can be established. In addition to this, the number of projects committed to the digital preservation of premodern documents seems to increase steadily, with libraries and universities scanning and uploading new images every year (...Footnote...). On a smaller scale, the proliferation of portable photographic devices, particularly in the form of digital cameras and smartphones, has enabled researchers to photograph, upload and share manuscript pages almost effortlessly, resulting in an latent circulation of archival material that has similarly affected the field (...Footnote...). We look at these images constantly; they appear on the screens of our classrooms, in those of conference rooms, and on our own laptops. However, in spite of these technological advancements and of this steady increase in digital preservation, the dissemination of these images has not radically transformed the way we approach them. Since the inception of digitization, critics have repeatedly speculated on how technology would allow us to challenge the artificial dichotomy between _manuscript_ and _text_; put otherwise, they predicted that medievalists would soon manage to complement their reliance on reconstructed critical editions with a constant perusal of digitally available primary sources (...Footnote...). So far, this prediction has not been fulfilled. On most occasions, we still treat these images as facsimiles--items that we _look at_--rather than as texts--items that we _read_.

    2. The distinction between looking and reading has been more easily overcome in other fields. For instance, comprehensive databases of printed materials--such as HathiTrust (...Footnote...), the Internet Archive (...Footnote..), or Google Books (...Footnote...)--allow scholars to look up strings of text across millions of digitized books. Having found a match, the users of these platforms can seamlessly turn from text to image. The search engine shows them the specific paragraph and line where these words appear; as a consequence, they can then examine the actual layout of the page, verify the presence of illustrations or annotations, and perhaps flip back and forth through the facsimile. In short, looking and reading overlap because image and text overlap. Such opportunities are not limited to modern texts; on the contrary, EEBO...

     from there, they can examine the layout of the page,  

 and to seamlessly start flipping through their page

 flip through the pages


    - Imagine this... You are browsing a collection of texts... You can look up a word and immediately locate the corresponding part of a manuscript. Or, while looking at a manuscript, you can highlight a portion of text and be given an (automatic?) transcription ---

        - This happens on EEBO, Google Books, Amazon. It does not happen for medieval MSs.


How electronic reproductions and online databases have pushed us to _see_ but not to _read_; we peruse collections of images as such--objects that are meant to be seen but not read. However, technology can help us overcome this obstacle by adding a layer of text onto the image. Picture this: a collection of images where the text is searchable; a collection of images where a transcription can be immediately perceived beyond the image itself.

    - Argument made by D. Wakelin somewhere?

    - If this was possible, the boundaries between archival/paleographic research and textual/critical analysis would

3. But the transcription of MSs is a laborious and highly specialized task. Projects that invest in the digitization of manuscripts tend to dismiss transcription, and particularly the automatic transcription to which we refer (the one that would allow you to _look at_ and _read_ the text at once). For this reason, the instruments provided by OCR could yield interesting results.

    - How many MSs have been digitized? How expensive and time consuming is this kind of labor?

4. What OCR has accomplished so far. The involvement of artificial intelligence and language recognition; neural networks. Great progress in a relatively short time. The work that has been done on medieval manuscripts. Different languages and different outcomes.

5. A description of our experiment. What did we set out to establish? How much time did we have? Potential framing: Establish how well a preexistent turn-key OCR system--non-dedicated, designed for a different purpose--can transcribe a limited corpus of Middle English MSs. Also: Establish how much time and effort it takes, and make assumptions about its potential scalability. Also: Establish the potential challenges which a medievalist might encounter, and the different ways to improve the system (e.g.: is it better to work with one text or with multiple texts?)

6. The collaboration with OpenITI and Kraken. A tool used for a different purpose--the transcription of Arabic texts in print--with interesting overlaps; in particular, the fact that it is designed to read the text not letter-by-letter, but word-by-word. This is a good fit for medieval handwriting, and a feature that is missing from other tools. Their accomplishments; other features of Kraken.

7. The choice of a corpus. The increase in book production in the century that goes from 1375 until 1475. The transition from Gothic to Cursive in this period. Anglicana Formata as the "bookhand" standard for writing these materials in medieval Britain. Anglicana Formata as a slightly more consistent and "bookish" script than Anglicana Cursiva and secretary.

8. The choice of Scribe D. At the center of a collaboration among scribes; the hypothesis being that his version of Anglicana would be more easily transferrable to other MSs.

    - Doyle & Parkes:

    > The handwriting of scribe D (pl. 49) is based upon a version of anglicana formata, which is particularly common in manuscripts containing vernacular texts produced in the first half of the fifteenth century. D is one of the most prolific copyists from this period, presumably a full-time scribe, and so far we have found his hand in the following manuscripts. __(They list 10; L. Mooney might have more.)__

9. The process.

10. The results.

11. The challenges.

    - Multi-lingualism as a challenge?

12. Future applications. Searchable .pdfs. Comparison with EEBO. Role of language recognition and implementation of dictionaries. More scans available; lower resolution images as an aid.

13. Conclusion. Feasibility of the process on a larger scale. Need to involve paleographers and medievalists. Decisions that will have a lasting impact on the way we consume these texts.

    - Also, need to maintain this work transparent, publicly available, and open source.

    - Need to spread a culture of partial reliance and partial skepticism surrounding the tool. Compare it with the subtitles (close captions) that can be activated on YouTube. They are an aid, not an authority. How can we spread this awareness, while the technology improves and more medievalists get on board?
