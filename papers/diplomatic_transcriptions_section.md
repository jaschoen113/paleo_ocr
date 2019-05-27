---
title: "Notes on Diplomatic Transcription"
author: G. E. Saretto & J. Schoen
date: May 2019
---

##### Article

|word limit|paragraphs|pages|
|:---|:---|:---|
|4000|16|16|

##### Section

|word limit|paragraphs|pages|
|:---|:---|:---|
|2000|8|8|

---

### Draft

#### Diplomatic Transcription

1. Having chosen a suitable manuscript for our project, and having selected an adequate range of pages and images for the training portion of our experiment, we then proceeded to produce our own transcriptions of the text contained in it. As we have mentioned, _kraken_ needs to be fed a relatively small collection of manual transcriptions, alongside the images from which these transcriptions are drawn. In our case, these transcriptions amounted to about 1,330 lines, distributed across 40 pages[^note_pages_lines]. By analyzing both these images and these transcriptions simultaneously, the software is supposed to develop its own set of instructions on how to extract editable strings of writing from sheer photographic reproductions. Accordingly, these training transcriptions must be prepared with great care. As expected, not only did the preparation of these manual transcriptions ultimately constitute the bulk of our work, but it also posed the largest number of challenges. More specifically, even though the manuscript on which the machine was trained--_Corpus Christi 198_--had already been edited by Frederick Furnivall in 1869, his 19th-century transcription proved unfit for our purposes. This happened because _kraken_--like most contemporary OCR systems--demands a "diplomatic transcription"; in other words, a transcription where every letter form represented on the page corresponds to a single character--or glyph--of plain text, abiding by a strict one-to-one correlation. On the contrary, Furnivall's transcription systematically expands most scribal abbreviations, causing incongruities between image and text that would inevitably compromise the training process.

[^note_pages_lines]: When compared with other contemporary OCR systems deployed for similar purposes, the training of a model through _kraken_ demands relatively few pages. The guidelines of _Transkribus_, for instance, recommend a training data set of about 100 pages.

2. As a consequence, even though we relied on Furnivall's work to verify the accuracy of our transcriptions, we assembled these 1,330 lines of training data from scratch, together with some 1,400 additional lines which we transcribed for testing purposes. Besides the obvious paleographical labor, this step entailed a great deal of preparatory planning and deliberation. These preliminary decisions revolved around the problematic delineation of what counts as a proper "diplomatic transcription" within this context. In particular, we needed a consistent set of instructions to specify how to render the letter forms represented on the page--and reproduced on the digital images--into a precise sequence of plain text characters; in other words, a reliable system of correspondences between handwritten letter forms and typographical glyphs. Given the current increase in the digitization of medieval manuscripts, and the proliferation of digital editions derived from them, one would be inclined to take the existence of such a standard for granted. Nevertheless, a precise and consistent set of guidelines concerning how to prepare a "diplomatic transcription" does not seem to exist yet--not even among paleographers[^note_lack_standard]. For this reason, every contemporary edition of a Middle English manuscript--either online or in print--must reinvent its own rules anew. This necessity becomes more prominent the more closely an editor strives to reproduce the original aspect of the handwritten page. Among the numberless features and distinctions that characterize the original codex, which ones should be preserved in this typographical reproduction, and how?

[^note_lack_standard]: Compare, for instance,  ...

3. Therefore, considering the ostensible lack of a consistent standard for "diplomatic transcriptions," and because of the restrictions imposed by the OCR system, we were faced with the question of how to translate these late medieval letter forms into plain text characters--preserving the one-to-one ratio demanded by _kraken_. Moreover, we decided to limit our selection of characters to the set that had been proposed in the guidelines of the Medieval Unicode Font Initiative[^note_mufi]. In particular, we followed their recommendations to render less common characters and abbreviations through dependable Unicode encodings, thus ensuring that these could be displayed adequately across different systems and applications. We sense that the decisions made during this phase of the training matter a great deal, since they are meant to inform the resulting model. For instance, should the machine learn the distinction between a long "s" (ſ) and a kidney-shaped "s" (ß)? Should it preserve the difference between an ampersand (&) and a tironian "et" (⁊)? Should it reproduce the contrast between a plain double "l" (ll) and a crossed--or "Welsh"--double "l" (ỻ)? Maintaining these distinctions may complicate the training and hinder the legibility of the final product; but ignoring them may cause a loss of information that the resulting model will replicate in every subsequent implementation. In other words, the scholars who develop a model decide not only how the OCR system will acquire and interpret the training data, but also how every subsequent text processed by it will be read in the future.

[^note_mufi]: MUFI ...

4. Taking into account the lasting impact of all these future implementations, and the fact that individual models may become increasingly versatile as the research behind OCR advances, these decisions should be discussed thoroughly and openly, and involve the participation of specialists from all the adjacent fields that rely on the analysis of such materials--not only paleographers and codicologists, but also linguists and literary critics. The potential scalability of this technology suggests that the outcome of these discussions will ultimately affect our study of these documents--including their script and their language--for a very long time. From this standpoint, the current technological limitations of OCR may have caused an almost unprecedented disciplinary shift in the way we approach the relationship between medieval handwriting and contemporary typography. The training of these models should rest on the establishment of a shared and sustainable standard for "diplomatic transcription"; and this standard demands a ... 

 may affect the way that scholars and students approach not only these documents, but also their scripts and their language for a very long time.

way we approach these documents, their script, and their language for a very long time.

    - ...

these

the OCR system will every other text processed by the OCR will be read in the future.

 Certainly, given its relatively small number of ligatures and abbreviations, a contemporary reader might find _Corpus Christi 198_ generally legible when compared with other handwritten documents from its period. To the human eye, its neatly arranged pages and generally distinct letter forms might recall the alleged tidiness of contemporary typesetting more than the _horror vacui_ popularly associated with the medieval book. Nevertheless, in spite of its ostensible legibility, the adaptation of this text into a digital "diplomatic transcription" entailed a number of choices ...

[^note_mufi]

into a digital "diplomatioc transcription" prompted us to reflect on the ...

...

#### Results

1. ...

2. ...

#### Future Experiments

1. ...

2. ...

#### Conclusions

1. Our results prove that OCR technology has the capability to transcribe Middle English texts.
Before we can produce fully automatic transcriptions, we will need significantly more training data and better training algorithms. But medievalists have a unique role to play in building this tool, and we hope that our promising, if preliminary, results might encourage more scholars to get involved with similar projects.

Awareness of the choices involved in these processes;

Larger claim about the fact that OCR allows us to restart/rethink the conversation (makes us aware of the stakes of the conversation) about:
What goes into a transcription/a facsimile (massaging; exclusion of languages; exclusion of borders and decoration--”problems”)
The conventions of transcription (diplomatic transcription, standard for abbreviations)
Lacking a standard for diplomatic transcriptions and the rendering of specific letter froms

2. ...

---

### Previous Draft

Jenna Schoen and Gianmarco Saretto
28 February 2019
Article draft

Optical Character Recognition and Middle English Manuscripts

Note: We’re currently intending to submit this article to Digital Philology (or a similar journal—Manuscript Studies might also work). This is a medievalist journal with a bent towards the digital humanities, which means the audience is largely medievalists who are interested in medieval digital projects. They’ve never had an article on OCR, but they’ve had articles on digital databases and tools (for example, this is an article on database for medieval Catalan songbooks). We’re assuming that the audience hasn’t heard of OCR but has familiarity with paleography.

To-Do List
[ ] Find out who has defined “diplomatic transcription” and how;
[ ] Find three examples of “diplomatic transcription,” show how it is inconsistent
[ ] Email KKF?
[ ] Look into the “data massaging” problem
[ ] Look at Ralph Hanna working on the Ellesmere (cutting away parts of the MS)
[ ] Look at Ker working on the Harley lyrics (multilingual transcr.)
[ ] Prepare preliminary draft / fleshed out outline

Brainstorming

Example from medieval MSs; turn to OCR as a similarly difficult yet productive moment (tihnking about it as data manipulaton) https://search.proquest.com/docview/304669850?accountid=10226&pq-origsite=summon
Scholarly drive to consider it as an English text -- the transcription highlights a bias that already existed within the field -- Harley MS; Middle English over Anglo Norman …
We are at another stage of data transfer … “remediation” (McLuhan … who else? Careful because remediation has not been used properly in the past … find the right reference to place here; or, offer new definition of concept that you allude to) … In the most recent years projects -- including our own -- have sprung up attempting to automate transcription. These automatic transcriptions present another set of transcription questions; they allow us to reflect on transcription decisions that we have been making for longer than this period …
We see many similar experiments happening at this time. But we do not see conversations happening around the preservation of bias and the decisions that should go into these processes ...
Discuss problems, but applying them to MS history--not OCR yet
In this paper, we will discuss an experiment which we have performed … we have achieved relatively satisfying results … Moreover, we have uncovered … findings concerning the decisions that should go into these experiments …
… Description of the experiment …
Highlight the decisions that went into the *massaging* of the image and the manuscript
Will OCR prompt us to use MSs that are deemed more “readable”? Moving away from decoration, stains, rips…? (bias)
What order should we use to present findings and method (that is, do we discuss diplomatic transcription extensively before turning to the results)? Or do we return to diplomatic transcriptions later?
---
Diplomatic transcription
...
Discussion of the results; other ways to process imperfect data beyond “search”
Deploying topic modelling to identify patterns beyond the exact/inexact transcription;
Make something out of the error
Future experiments and future perspectives
Addressing the “bias”
Multiple scripts/scribes/language
Technology must go hand in hand with the needs of critics; technology must develop under the supervision of critics
Conclusion

FRAME? Do we really need to introduce digitized Mss?

    Start with the experiments that have already been attempted;
Highlight the fact that has been some processing and selection involved
Highlight the diplomatic transcription involved

Start with an example from traditional MS studies? Ker or Hanna?
Editorial choice as a moment of transition that posed interesting questions; OCR does something similar …
Treat OCR (and digitization) as an exciting moment in textual/book history; a moment that demands the involvement of medievalists

OCR is inevitable. Recent developments in OCR for medieval texts … need to investigate the decisions that are made … Decisions involved in the training … like all sorts of AI experiment … what are we trying to produce? These decisions should involve medievalists … “importation of bias” (example of training AI, AI turns out to maintain human error/human prejudice) … awareness of bias … prevent decisions from becoming the norm … someone will have to decide how to deal with abbreviations …

***
Loss of information is inevitable; translation from one system to another …

What kind of UNICODE should be adopted?
The “glyph” is turned into a sequence of characters that are in turn rendered as a letter form on screen --- what is a glyph and what is a sequence of characters?
Collapsing equivalent letter forms (long s, short s)

Is diplomatic transcription always necessary? Will it be necessary in the future?
We are constricted by diplomatic transcription right now; this makes this an important moment for decisions of this kind
We might foresee a future where diplomatic transcriptions are no longer necessary; this model would have advantages and disadvantages (loss of information, increase in readability)
***


1.1 Problem of Limited Manuscript Transcriptions
In the past few decades, the field of medieval studies has been greatly affected by the rise of digital editions and the increased availability of online facsimiles. Thanks to comprehensive databases, students and scholars of the Middle Ages can now easily access hundreds of digitized manuscripts and thousands of high-quality images. The number of digital preservation projects are steadily increasing, with libraries and universities scanning and uploading new images every year. On a smaller scale, the proliferation of portable photographic devices, particularly in the form of digital cameras and smartphones, has enabled researchers to photograph, upload and share manuscript pages almost effortlessly, resulting in the informal -an latent circulation of archival material that has similarly affected the field. We look at these images constantly; they appear on the screens of our classrooms, in those of conference rooms, and on our own laptops. However, in spite of these technological advancements and of this steady increase in digital preservation, the dissemination of these images has not radically transformed the way we approach them. Since the inception of digitization, critics have repeatedly speculated on how technology would allow us to challenge the artificial dichotomy between manuscript and text—they predicted that medievalists would soon complement their reliance on reconstructed critical editions with a constant perusal of digitally available primary sources. So far, this prediction has not been fulfilled. On most occasions, we still treat these images as facsimiles—items that we look at rather than texts that we read.
The distinction between looking and reading has been overcome more easily in other fields. For instance, comprehensive databases of printed materials—such as HathiTrust, the Internet Archive, or Google Books—allow scholars to look up strings of text across millions of digitized books. Such opportunities are not limited to modern texts; on the contrary, databases such as EEBO—Early English Books Online—allow scholars to perform analogous searches and inquiries on thousands of printed materials published between 1473 and 1700. Since the search engine can locate the specific paragraph and line where a string appears on a facsimile, users can then seamlessly examine the actual layout of the page, verify the presence of illustrations or annotations, and perhaps flip the book back and forth.
With corresponding transcriptions for digital medieval manuscripts, researchers could search and read digital facsimiles with relative ease, closing the gap between looking and reading. Producing transcriptions for a large corpus of medieval manuscripts would serve additional purposes beyond the digital facsimile experience. It would allow us to compare manuscripts across a single textual tradition, create digital editions for lesser-known texts, and conduct large-scale data analysis (such as topic modelling and text mining) across historical documents. Projects like the Piers Plowman Electronic Archive, which has produced digital transcriptions of eight B-Text manuscripts, attest to the usefulness of an easily accessible, readable, and usable digital archive. However, human transcription is time-consuming and expensive: it requires a trained paleographer and hours of labor per manuscript.
Fortunately, machine learning can help solve this problem by producing automatic transcriptions en-masse. Specifically, Optical Character Recognition (OCR), a method of turning print or handwriting into digital text, can allow researchers to automatically convert images of manuscripts into digital transcriptions. In the past two years, researchers have begun training OCR models on medieval scripts: most notably, Tobias Hodel and his Transkribus team have been using OCR technology to transcribe German and Latin Gothic scripts. Our team wanted to determine whether we could train a machine to transcribe a Middle English script and understand the challenges involved with this kind of project.
 Using an open-source OCR system called Kraken, developed by Ben Kiessling at the University of Leipzig, our team has promisingly trained an OCR system to transcribe manuscripts of the 14th century Middle English Scribe D. While much work remains to be done before this technology can accurately transcribe most medieval scripts, these initial results at least indicate that with more training data and more advanced machine learning systems, OCR may very well have an immense impact on medieval studies. In this article, we discuss our methodology, results, and important considerations for future manuscript OCR projects.

2. Methodology

2.1 OCR

Optical Character Recognition (OCR) transforms a text-image—for example a scanned book or a photograph of a document—into machine-readable text. This conversion process allows print and handwritten texts to be digitally searched, edited, stored, and otherwise manipulated by a computer. OCR technology already underlies many of the digital texts we read: it is what enables Project Gutenberg to easily digitize printed texts and Google Books to perform keyword-searches on scanned books. OCR models are built through machine learning, meaning that the machine executes tasks through inferred rules rather than explicit instruction. For example, in the case of manuscript transcription, a machine is first given images of a manuscript alongside corresponding digital transcriptions, the machine next “trains” on the images and transcriptions and “learns” the transcription rules on its own, and the machine then produces its own transcriptions on new, previously unseen images.
MUnfortunately, medieval manuscripts pose significant challenges to automated processing. Unlike printed texts, medieval handwriting often contains non-discrete characters, for example in the conjoined letters of cursive scripts or the disconnected minims of Gothic script; machines cannot simply be taught individual letter forms, but must learn tothe transcribe larger segments of text. Compared to modern handwritten documents, medieval manuscripts feature elaborate and often cryptic handwriting systems which vary intensely across period, region, and scribe. Accordingly, distinct OCR systems must be trained on distinct medieval scripts, which means compiling training data on tens, if not hundreds, of manuscripts per script. Furthermore, medieval manuscripts often have extensive marginal notes, decorations, and damage, making it difficult to distinguish text from other information in a digital image. Finally, given that the most advanced OCR engines often rely on comprehensive dictionaries and natural language processing to improve accuracy, the inconsistent orthography of medieval languages (like Middle English or Old French) poses an additional obstacle to efficient automated transcription.
In order to assess the feasibility and scalability of automatic transcription for medieval manuscripts, we decided to experiment with a pre existent OCR software—Kraken—on a small corpus of Middle English manuscripts. Kraken is a turn-key OCR software developed by Ben Kiessling, originally created to transcribe Arabic texts. Conventional OCR systems operate by learning individual letter forms, but since Arabic is a connected script, it requires a system that transcribes larger strings of text. Kraken uses a neural network to recognize text without first segmenting it into words and letters, and has proven very effective at transcribing Arabic. Since medieval handwriting often features  non-discrete letter forms, and therefore poses similar challenges as connected scripts, we decided that Kraken would be a fitting program to use. Kraken has the added benefit of being completely open-source, so we could experiment with our models without waiting for another team or company to run the training for us.

2.2 Corpus

When selecting manuscripts for training and testing, we aimed for a script that was both widespread and exemplary. That is, we sought a handwriting system which was used to write many of the manuscripts in Middle English that survive to this day, which shared individual traits with other scripts, and whose general aspect—or ductus—could serve as a medial point between several chronologically adjacent scripts. Anglicana Formata suited this description..As is well known, this script was developed in the second half of the 13th century as a sort of functional yet relatively elegant book hand; it could be written more easily and rapidly than Gothic textualis, but it looked more legible and polished than a documentary cursive. For this reason, Anglicana Formata became a standard for medium and high-end Middle English manuscripts; after 1375, it proved instrumental for the exponential increase in the insular production of vernacular books. Moreover, it encompassed letter forms drawn from older scripts, such as Gothic and documentary, and from newer scripts, such as Secretary. Finally, the automatic transcription of its ductus poses challenges shared with other scripts; for instance, it combines the loops and slants of documentary with the minims and compressions of Gothic.
Having chosen Anglicana Formata, we then selected the manuscripts that would comprise our small corpus. We decided to focus this corpus around a particular scribe and to his professional circle: "Scribe D"—possibly John Marchaunt—and the scribes involved in the production of the Trinity Confessio Amantis (Cambridge, Trinity College, MS R.3.2). In particular, we trained the machine on a manuscript that was attributed to Scribe D (Oxford, Corpus Christi Coll., MS 198), which is particularly clean document with a neat script  (see “Conclusions 4.3” for further discussion). For resting manuscripts, we aspired to concentrate on scribal differences alone; to minimize the effect of other factors, these hands should have shared a common script, and a similar historical and geographical background. We tested the resulting model on four other manuscripts: two attributed to him (the Trinity Confessio Amantis itself; and London, Brit. Lib., MS Harley 7334), one attributed to Scribe B—possibly Adam Pinkhurst—(Cambridge, Trinity College, B.15.17), and one by an Anonymous scribe (Corpus Christi 201). We selected these particular manuscripts because we hoped to assess extent a machine trained on the hand of one scribe could also satisfactorily transcribe texts written in a different hand. Because of the well-attested collaboration within the group of scribes to which Scribe D belonged, we could assume a spatial and chronological proximity between him and Scribe B, and—perhaps—an attempt to uniform their script. We also decided to experiment with a scribe outside this professional circle whose hand is still Anglicana Formata; therefore we added Corpus Christi 201, whose scribal hand is significantly different from Scribe D and his professional circle, even if he is writing in the same time period in the same general script.
2.2 Training Procedure
    After selecting our training manuscript (Corpus Christi MS 198), we first compiled our training data—1,330 lines from the manuscript transcribed in plain text. These lines were selected from a range of the manuscript with no major damage or decoration. We consulted a print transcription for reference and thoroughly double-checked our transcriptions. Since Kraken requires fully diplomatic transcriptions, we also had to devise systematic Unicode characters for abbreviations (this step will be further discussed in our “Conclusions”). We then trained our model by providing Kraken with scans of the manuscript pages alongside our digital transcriptions.

3. Results

3.1 First Round

After Kraken had completed its training, we tested our model on the training pages, new pages from the same manuscript, and pages from additional manuscripts (see Table 1). Our model did better than expected on the training pages (9.83% error rate), as well as on unseen pages from the same manuscript (14.64% error rate). Our model also did relatively well on other manuscripts from Scribe D. As to be expected, it performed better on Scribe D’s Harley 7334 (another Canterbury Tales manuscript) than his pages of Trinity R.3.2 (a Confessio Amantis manuscript).
Our model performed poorly on manuscripts from other scribes. It performed particularly poorly (82.56% error rate) with the scribal hand of Corpus Christi 201 (a scribe outside D’s professional circle) and relatively better (41.45%) with Scribe B (a scribe in his professional circle). Nevertheless, our Scribe D model appears to be constrained to Scribe D forms and cannot produce significantly accurate transcriptions of other scribes.
When we examine the model’s success at transcribing individual characters, we find that, for the most part, the model does best with high frequency characters—this is to be expected, since the model will better learn characters that appear more often. For example, the model does relatively poorly with capitals (“B” has a 31.82% error rate, “O” has a 36.84% error rate, “S” has a 33.33% error rate), and relatively well with minuscules (“b” has a 13.9% error rate, “o” has a 13.23% error rate, and “s” has a 13.17% error rate). Characters that are typically difficult for humans to discern also prove difficult for our machine. For example, the model does relatively poorly with characters prone to minim confusion: “i” has a 26.94% error rate (even though it occurs very frequently) and “m” has a 29% error rate. Looking at the individual character error rates may also reveal certain training biases: for example, our model does unusually well with “P” (9.09% error rate) compared to other capitals (average error rate), perhaps because we trained the model on a selection from the Knight’s Tale, in which Palamon is a titular character. Training models on a more diverse selection of texts may even out some of these training biases.

Table 1: Error Rates of Scribe D Model







Manuscript
Scribe
Folio Numbers
Lines
Date
Error Rate
Corpus Christi 198 (Canterbury Tales)
Scribe D
16r-35v
1330
c. 1410-1420
9.83%
Corpus Christi 198 (Canterbury Tales)
Scribe D
160r-164v
280
c. 1410-1420
14.64%
Harley 7334 (Canterbury Tales)
Scribe D
4v, 54v, 58v, 72r, 86r, 86v, 180r, 200r, 200v, 203v
370
c. 1410
20.21%
Trinity R.3.2
(Confessio Amantis)
Scribe D
139v-143r
720
c. 1408-1426
32.60%
Trinity B.15.17
(Piers Plowman)
Scribe B
119v-123v
243
c. 1375-1415
41.45%
Corpus Christi 201
(Piers Plowman)
Anonymous
82r-84r
180
c. 1400-1415
82.56%


4. Conclusions

When we started this project, we knew of no other team working on medieval script recognition. Since we’ve been working on the project, other teams have been successfully training OCR models on medieval scripts, such as the Transkribus team headed by Tobias Hodel, which works on German and Latin scripts. Even though other research teams have been achieving similar results, we think it’s important to discuss the challenges we faced in throughout this project.

4.1 Abbreviations

During training, Kraken and other OCR programs require diplomatic transcriptions which reproduce all the characters in a manuscript image. As a result, abbreviations in medieval scripts pose a significant challenge for generating training transcriptions. Even if a digital transcription of a manuscript is available (which is often not the case), most “diplomatic” transcriptions extend abbreviations in italics, which the machine cannot recognize. Therefore researchers must compile transcriptions manually. In addition, digital transcriptions must be in Unicode, and there is currently no Unicode standard for medieval abbreviations, nor are medieval abbreviations typically rendered in Unicode at all. Researchers therefore need to decide how to render each abbreviation in Unicode (for example, “d̉ ” instead of “der”). This is particularly difficult for Middle English, which has no paleographic handbook for abbreviations (such as Capelli serves for medieval Latin). Therefore not only did we have to select Unicode characters for each abbreviation, we also had to categorize the abbreviations in the first place. We currently have a working abbreviation guide (available on GitHub) that outlines our abbreviation categories and corresponding Unicode characters. In order for this technology to accurately and optimally render medieval scripts, researchers and paleographers will need to collaborate to decide on universal Unicode characters for abbreviations. As a universal tool will require consistent training data from different research teams, it is necessary that we decide on standard transcription decisions, such as abbreviations.

4.2 Different Scribe, Script, and Language Models

We trained our model on a single scribe and a single manuscript, but future projects should experiment with models trained on different manuscripts and different scribes. A useful automatic transcription tool will need to successfully read different scribes; it will be too time consuming to have models for every single Middle English scribe.

Additional experiments can also be performed with multi-script models (for example, Anglicana Formata and Secretary). However, it is more reasonable to have models for individual scripts than models for individual scribes. Researchers have already been experimenting with using OCR to identify script types. It is therefore not hard to imagine a machine that first uses OCR to recognize the script type, selects the relevant script model, and finally uses that OCR model to transcribe the image.
CB highlights that multi-script models would be useful for the same MS as well; perhaps it would be useful to train model on the “hierarchy of scripts” of a single MS.

Finally, experiments should be performed with multilingual models. We limited our model to Middle English by training with a Canterbury Tales manuscript, but many “Middle English” manuscripts are actually multilingual (e.g. with Latin glosses). We hypothesize that script is the primary limiting factor for models; in other words, that as long as both Latin and Middle English are written in Anglicana Formata, a machine can learn the graphs in both languages simultaneously. But multilingual training may pose new challenges and lower accuracy rates, which would be critical hurdles to overcome.

More emphasis on multiple languages?

4.3 Script and Manuscript Quality

We also trained our model on an especially neat scribe and a clean manuscript with little decoration and damage. But most medieval manuscripts have either sloppier handwriting, difficult minim sequences, marginalia, illuminations, rips, stains, or other non-textual features. Since Kraken automatically recognizes and segments lines in a manuscript image, these features can prevent or confuse line recognition and ultimately prevent accurate transcription. Future experiments should be performed with manuscripts containing these non-textual features and with programs that can distinguish text from other features in a manuscript image.

4.3 Different OCR Systems

Since Kraken is open-source, it is easy for researchers to use and allows flexibility in training. This allows you to easily experiment with amount of training data, different models generated from training, color, manuscripts, etc (fix).  But we also plan to experiment with different OCR systems. Another OCR project, Transkribus, is working to build a large corpus of training data and incorporate many different scripts and languages. They also have a separate team which handles the training, which means medievalists need to do even less computer-work. The drawback of this workflow is that it makes it harder for individual researchers to experiment with training.

4.4 Open-source and open-access  

Most importantly, it’s essential that all researchers working on automatic transcription projects make their training data and OCR models freely available online. This way researchers can experiment with new OCR systems, collectively generate a large corpus of training manuscripts, and use trained OCR models for various transcription projects.

Relatedly, training a transcription machine requires digital images of manuscripts. Luckily thousands of medieval manuscripts are fully digitized, and future digitization projects will provide more candidates for training and transcriptions. However, even though many manuscripts are digitized and available to view online in high-resolution, most libraries do not allow these images to be downloaded in high-resolution, which is required for the training process. Even in our relatively small experiment, we were extremely limited by the manuscript images freely available to download and those which libraries agreed to send us. While institutions may not want to make these images publically available, they will need to share them with researchers if they want a tool which will significantly improve their digital editions in the long run.

4.5 Final Notes


Works Cited

Capelli, Roberta. "Practical and Theoretical Implications of Digitizing the Middle Ages." CLCWeb: Comparative Literature and Culture 15.3 (2013): <https://doi.org/10.7771/1481-4374.2248>
Doyle, A.I. and M.B. Parkes. "The production of copies of the Canterbury Tales and the Confessio Amantis in the early fifteenth century." in Medieval Scribes, Manuscripts, and Libraries: Essays Presented to N.R. Ker. London: Scolar Press, 1978.

Furnivall, Frederick J. The corpus ms (Corpus Christi Coll., Oxford) of Chaucer’s Canterbury Tales. London: N. Trübner & co., 1868-1879.

Hodel, Tobias. “Sending 15th-Century Missives through Algorithms: Testing and Evaluating HTR with 2,200 Documents.” Paper presented to IMC Leeds Conference, July 3 2017. Published online at solascriptum.wordpress.com  

Kestemont, Mike, Vincent Christlein, and Dominique Stutzmann. "Artificial Paleography: Computational approaches to identifying Script Types in Medieval Manuscripts." Speculum. October 2017.

Kiessling, Benjamin, Matthew Thomas Miller, Maxim G. Romanov, and Sarah Bowen Savant. "Important New Developments in Arabographic Optical Character Recognition (OCR)." _Al-ʿUṣūr al-Wusṭā_ vol 25, 2017.

Mooney, Linne and Estelle Stubbs. Scribes and the city: London Guildhall clerks and the dissemination of Middle English literature, 1375-1425. Suffolk: York Medieval Press, 2013.

Yang, Ying, et al. “Automatic single page-based algorithms for medieval manuscript analysis.” Journal on Computing and Cultural Heritage. 10.2 (2017): 9.
