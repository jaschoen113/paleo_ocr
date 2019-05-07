---
title: "Notes for Conference Paper"
author: J. Schoen & G. E. Saretto
date: May 2019
---

|Pages|Words|Paragraphs|
|:---|:---|:---|
|8|2000|8|

### Notes

- EEBO does not rely on OCR for transcriptions.

- Hathi Trust and Google Books do.

### Potential Outline

1. Introduction. The background

    - In this talk I will tell you about an experiment with Optical Character Recognition--or OCR--which I attempted in collaboration with a fellow graduate student, Jenna Schoen. Jenna would have gladly co-presented these findings with me, and participated in this exciting panel with all of you. Unfortunately, she has been asked to deliver a paper on the Pearl manuscript at a session that is taking place right at this moment. So, you will have to content yourselves with the lesser half of the team for now. Nevertheless, both our contacts are listed here, and both of us would be quite happy to further discuss these ideas with you on some other occasion--either here at Kalamazoo or by email later. [122]

    - Now, we started this project about a year and a half ago, within Columbia's Group for Experimental Methods in Humanistic Research. We were also funded by Columbia's Data Science Institute to continue it over the summer of 2018. The experiment itself consisted in using a preexistent OCR software--called _Kraken_, like Tennyson's giant squid--to train a model for the automatic recognition and transcription of a Middle English book hand from the early 15th century. In the next few minutes, I will describe this process and these choices in more detail. [94]

    - However, before I do so, I would like to reflect on why we decided to attempt this experiment in the first place. Why should one try to use OCR for medieval manuscripts? What would one gain from teaching computers to transcribe 14th and 15th-century book hands? I mean, apart from upsetting paleographers. Well, jokes aside, the advantages might sound redundant to a room full of medievalists, but it does not hurt to recapitulate them. So, take for instance EEBO--the massive database of Early English Books Online that launched in 1998. Today, EEBO contains digital facsimiles of more than one hundred thousand printed books, adding up to millions of pages. So far, nothing particularly exciting; photographic reproductions of medieval manuscripts are also becoming increasingly accessible. This has happened thanks to numberless digitization projects funded by libraries and universities everywhere, and to several comprehensive databases that facilitate our searches--such as _Digital Scriptorium_, the _Bibliothèque Virtuelle des Manuscripts Médiévaux_ or _Manus Online_. These images appear more and more often in our classrooms when we teach, on our laptops when we do research, and during conference presentations like this one. [192; 338]

    - However, EEBO offers more than a simple catalogue of images. Thanks to the Text Creation Partnership, launched in the early 2000s and based in the library of the University of Michigan, about one third of the books stored on this database can also be searched and manipulated as text. In other words, a large number of the facsimiles that can be accessed through EEBO exists both as a set of photographs and as a complete digital transcription. The two are mapped onto each other. Therefore, when I search the word "cat" in the database, the database allows me to examine not only the verbal context in which the word appears, but also the layout of the page and the presence of images or annotations. So, because of these transcriptions, these early modern books can be searched in their entirety; and they lend themselves to complex and broad-ranging computational analyses concerning their contents, their form, and their language. In short, medievalists feel great envy for EEBO. [166; 504]

    - Now, in spite of the high number of photographic reproductions available online, a Textual Creation Partnership for a medieval EEBO would probably demand far more work than the one involved in the transcription of these printed books from the Early Modern period. The wide diversity of scripts and scribal hands, the countless dialectal and orthographical variants, and the ubiquitous presence of inconsistent abbreviations makes the transcription of medieval _codices_ a great deal more expensive and time-consuming than the one of printed documents. As a consequence, one might argue that training OCR models to transcribe these texts automatically would perhaps facilitate the process. [101; 605]

    - Well, would it truly help? On the website of the Textual Creation Partnership we read that

    > Because of the irregularity and difficulty of early printing, as well as the variable quality of the microfilm-based images from which we are working, optical character recognition cannot reliably “read” the EEBO images to produce an accurate electronic text. The review and correction of the text produced would be so expensive and labor-intensive that it is more efficient to simply key the work from scratch.

    On a different page, the authors explain that "For books printed before 1700, and for images that are blurry, spotty, or have other quality issues, [_OCR_] fails almost entirely." So, how can we expect it to work adequately for _codices_ that were handwritten before the year 1500, and on pages that are often ripped or stained, or heavily annotated and decorated? [144; 749]

    - Despite these odds, we felt that the question warranted an experiment, and for at least two reasons. First, because the software and the technology behind OCR has kept improving. With the rise in the popularity of machine learning, and with the increased availability of faster and more powerful computers, programmers and researchers have managed to train models that can, for instance, estimate the date of a pre-modern manuscript--as researchers Wahlberg, Wilkinson and Brun have shown in 2016--or distinguish between various Latin scripts--as medievalists Kestemont, Christlein, and Stutzmann have described in 2017. Moreover, ... not the only ones ...


2. Preliminary choices. The system

    - In the fall of 2017 we contacted the team behind OpenITI, the Open Islamicate Texts Initiative. This international group of scholars--based in London, Leipzig, and College Park, Maryland--had just managed to successfully perform Optical Character Recognition on a corpus of classical Arabic-script books in print. In particular, the machine that they trained could transcribe texts with an accuracy that fluctuated between 70 and 90 percent. Of course, ... The difference between their goal and ours may seem great at first;

    - We deployed a turn-key OCR system called "Kraken"; this has been developed by Benjamin Kiessling, a scholar who works between Leipzig and Paris. It has been used for Arabic.

        - The ...

    - Open source; applications to Arabic

3. Preliminary choices. The corpus

    - Scribe D.

4. The process /1

    - Reliance on our own transcriptions; need to rewrite them from Furnivall.

        - Relied on a late 19th century transcription whose typographical features differed widely from what we needed.

[5. The process /2

    - Image quality.]

6. Results

    - Surprising?

7. Findings. Diplomatic Transcription

    - No such thing. There exists no consensus concerning what makes a diplomatic transcription a diplomatic transcription.

8. Findings. Should we rely on a dictionary?

    - Occasions when Furnivall gets it wrong.

[9. Findings. Perspectives

    - Multilingual MSs?]

10. Conclusions

    - An effort worth making? In what ways? What decisions concerning the future?

### What else?
