1. Kestemont, Mike, Vincent Christlein, and Dominique Stutzmann. “Artificial Paleography: Computational Approaches to Identifying Script Types in Medieval Manuscripts.” *Speculum* 92, no. S1 (October 2, 2017): S86–109. https://doi.org/10.1086/694112.

    - work on the automatic identification of Manuscripts
    - contains a breakout of the distinctions between OCR and HTR (S89-90); they distinguish between OCR and HTR on the basis of **function**.

2. Grusin, Richard. “Radical Mediation.” *Critical Inquiry* 42, no. 1 (September 1, 2015): 124–48. https://doi.org/10.1086/682998.

    - Discuss the "immediacy of mediation"

    > Mediation is not opposed to immediacy but rather is itself immediate. It names the immediacy of middleness in which we are already living and moving: Where do we find ourselves ... (129)

    - uses the notion of "transparency":

    > As half of the double logic of remediation, transparent immediacy holds that the subject's contact with the real depends upon the erasure of the medium, which correlates and thereby obscures the relationship between subject and world. [...] By using *remediation* I emphasize the point that both logics are at play in mediation, that the double logic of remediation entails both the transparency of media correlationism and the obscurity of radical mediation, and that these two different concepts of mediation are just as contradictory as immediacy and hypermediacy are. [...] immediacy is also used in remediation to refer to the embodied, affective experience that comes both from the direct encounter with the real provided by transparent mediation and from the immediate encounter with mediation provided by hupermediated modes of mediation ... (131)

3. Stutzmann, Dominique. “Clustering of Medieval Scripts through Computer Image Analysis: Towards an Evaluation Protocol.” *Digital Medievalist* 10, no. 0 (June 4, 2016). https://doi.org/10.16995/dm.61.

    - addresses--again--the question of how to cluster scripts together using artificial intelligence;

    - asks whether the system developed by computer scientists to identify scripts should work as a "black box for the use of paleographers" (providing useful results that we do not understand)

    - questions whether the problem with script identification may not lie with the humans who first devised these categories; deploys the software as a heuristic tool that helps paleographers

4. Bamford, Heather, and Emily C. Francomano. “On Digital-Medieval Manuscript Culture: A Tentative Manifesto.” *Digital Philology: A Journal of Medieval Cultures* 7, no. 1 (August 7, 2018): 29–45. https://doi.org/10.1353/dph.2018.0002.

    - Makes some claims that we could easily agree with:

    > As Christopher Flüeler has recently noted, it is surprising how little the relationship between physical and digital manuscripts has been examined, at least in published work. (31)

    > Yet, in his plenary to the Medieval Academy of America in 2016, William Noel cautioned against our collective implicit equating of digitizations with manuscripts: digitizations are curated and therefore mediated objects, each carrying a history of technological and interpretive decisions that led to their presentation as digital objects. (32)

    > By way of conclusion, what we are essentially arguing is that as digital philologists, we should be aware that we are creating, not reproducing or straightforwardly representing, manuscript cultures. (41)

5. Michael Widner. “Toward Text-Mining the Middle Ages.” In *The Routledge Research Companion to Digital Medieval Literature*. Routledge, 2017. https://doi.org/10.4324/9781315696041-9.

    - offers a survey of OCR approaches; explains that they are quite hard because of the difficulty posed by medieval manuscripts

    > Even if we set aside the substantial investments in time, equipment, and expertise needed to create high quality scans of medieval manuscripts, problems remain. Medieval manuscripts are practically impervious to contemporary OCR. (132)

    - Also, argues that there is much material that could be scanned and analyzed rapidly thanks to OCR.

    > Julie Orlemanski, in a similar vein, writes: "the 'great unread' of the Middle Ages is for the most part in manuscripts. Even when manuscripts are digitized ant thus potentially more accessible, their texts are rarely machine-readable." (133)

    - Examines difference between OCR and HTR (133-34)

    - Argues that digitizations and digital editions should be performed by small groups of scholars scattered around the world and collaborating thanks to the Internet

6. Orlemanski, Julie. “Scales of Reading.” *Exemplaria* 26, no. 2–3 (June 1, 2014): 215–33. https://doi.org/10.1179/1041257314Z.00000000051.

    - In short, offers a critique of "distant reading" and a reassessment of what is gained through "close reading." She also argues that medieval studies are both prone to reject distant reading (because so many texts remain inaccessible, in manuscript form) and strangely akin to it (because of their reliance on "peripheral" disciplines--codicology, paleography, and so on).

    > For scholars of medieval literature, Moretti’s experiments in scale may appear either irrelevant or old hat. Their seeming irrelevance stems from the fact that the “great unread” of the Middle Ages is for the most part in manuscripts. Even when manuscripts are digitized and thus potentially more accessible, their texts are rarely machine-readable. More seriously, Moretti’s aggregation of scholarship on various national literatures to form his sweeping data sets relies on certain shared characteristics of those literatures, like the capitalistic market for printed books. Given the relatively small and eclectic discourse communities characteristic of manuscript culture, it is not clear that more “distant” analysis is needed. On the other hand, distant reading loses its novelty for medieval literature insofar as the “other skills” Moretti recommends for a “larger literary history” — “statistics; work with series, titles, concordances, incipits” — are not dissimilar from the skills of medieval studies itself, with its subdisciplines of paleography, codicology, bibliography, dialect study, and philology (“Slaughterhouse” 209). Scholars of medieval literature have long operated at scales of reading other than close — a tendency that has sometimes isolated them within the field of literary study. (223)

7. Hawk, Brandon W., Antonia Karaisl, and Nick White. “Modelling Medieval Hands: Practical OCR for Caroline Minuscule.” *Digital Humanities Quarterly* 013, no. 1 (April 26, 2019).

    - have worked "on a total of 88 medieval manuscripts ranging from the ninth through thirteenth centuries."

    - Describe the relationships between OCR and HTR; argue that "there is a significant point to using OCR software--rather than other tools for handwritten text recognition (HTR)--because of the relative regularity of medieval hands and scripts overall, which may be analogous in some ways to print typefaces in a general way. [...] The differences between OCR (a long-established technology) and HTR (in an early phase of development) are subtle but substantial. The biggest difference lies with layout analysis and segmentation for processing: this stage is usually built into the OCR engine, while it is a separate stage in HTR. [...] Yet OCR and HTR technologies and processes have recently converged to some degree. Major OCR engines are also used on handwritten texts in various ways. Indeed, there is now some amount of overlap between OCR and HTR in practice because of developments in machine learning. .."

    - They also discuss Artificial Neural Networks in great detail; and they use OCropus

    - the goal of their experiment was to establish whether "the size and diversity of the training pool would be directly proportional to the quality of the resulting model when tested on 'seen' and 'unseen' manuscripts within the realm of Caroline minuscule scripts."

    - They bracket "the expansion of medieval abbreviations" as a "post-processing problem"; they argue that future research should expect "LSTM models to be trained" to correctly expand ambiguous abbreviations."

    - they argue that some combinations of manuscripts can yield surprisingly effective results:

    > A careful conclusion would have it that a variety of two or more manuscripts does not yield a better foundation for an OCR model for either target manuscript as a rule, but that specific combinations of manuscripts can yield exceptional results.

    - their ambition is to build "a turn-key OCR model applicable to as large a range of unseen manuscripts as possible"

    - their results apply mostly to Caroline

8. Committee, Association of College and Research Libraries Rare Books and Manuscripts Section Bibliographic Standards. *Descriptive Cataloging of Rare Materials (Books)*. Washington, D.C.: Cataloging Distribution Service, 2007.

    - they prescribe the normalization of spelling and the expansion of contractions (34-45, 187-193).

9. McGrady, Deborah. “Textual Bodies, the Digital Surrogate, and Desire: Guillaume de Machaut’s Judgment Cycle and His Protean Corpus.” *Digital Philology: A Journal of Medieval Cultures* 5, no. 1 (June 1, 2016): 8–27. https://doi.org/10.1353/dph.2016.0002.

    - examines how digital surrogates "reignite nostalgia for the *real*, understood here as a physical and material body that one might experience multi-sensorially and intimately" (9)

    - she explores remediation in terms of "surrogate" and the medieval manuscript; useful recapitulation on p. 21

    > That is, in dealing with remediated texts, we oscillate between believing we have an unmediated relationship with the original object--here the handwritten manuscript--at the same time that we recognize that a new medium--the digital realm--negotiates our encounter with the original mediated object. (21)

10. Edwards, A. S. G. “Chaucer From Manuscript to Print: The Social Text and the Critical Text.” *Mosaic: A Journal for the Interdisciplinary Study of Literature* 28, no. 4 (1995): 1–12.

    - a discussion of how early printed editions of Chaucer's works affected the long history of his reception and his placement in the canon, from the early modern period to the present.

11. Dahllöf, Mats. “Automatic Scribe Attribution for Medieval Manuscripts.” *Digital Medievalist* 11, no. 1 (December 24, 2018): 6. https://doi.org/10.16995/dm.67.

    - offers an automated system for attribution that still strives to be readable (accessible) for a human reader; works against the pitfalls of a "black box" approach

12. Ciula, Arianna. “Digital Palaeography: Using the Digital Representation of Medieval Script to Support Palaeographic Analysis.” *Digital Medievalist* 1, no. 0 (April 20, 2005). https://doi.org/10.16995/dm.4.

    - seminal article in the development of automatic methods for the study of premodern handwriting; she argues that paleography seeks discrete differences (seeks to systematize and quantify discrete differences); we can argue that, on the contrary, OCR often works in the direction of standardization: it removes differences, it tries to ignore differences; her work concentrates on the identification and quantification of discrete paleographic differences.

13. Stansbury, Mark. “The Computer and the Classification of Script.” In *Kodikologie Und Paläographie Im Digitalen Zeitalter - Codicology and Palaeography in the Digital Age*, edited by Malte Rehbein, Torsten Schaßan, and Patrick Sahle, 2:237–49. Norderstedt: BoD, 2009.

    - examines the turn  towards "measurement" and quantification in the study of paleography; argues that technology enables a paradigmatic shift (238), and that in fact "palaeography was made possible by two technological innovations in the fifteenth century: printing and engraving. Engraving and later etching and lithography made possible the mass reproduction of identical facsimiles of scripts." (241)

    - cites Ludwig Traube on Photography;

14. Traube, Ludwig. *Zur Paläographie Und Handschriftenkunde*. München: C.H. Beck, 1965.

    - argues that the dissemination of cheap photographic facsimiles changed the field of paleography (57)

15. Arabnejad, Ehsan, Reza Farrahi Moghaddam, and Mohamed Cheriet. “PSI: Patch-Based Script Identification Using Non-Negative Matrix Factorization.” *Pattern Recognition* 67 (July 1, 2017): 328–39. https://doi.org/10.1016/j.patcog.2017.02.020.

    - offers a method base on neural networks for the automatic recognition and classification of script  

16. Stokes, Peter A. “Palaeography and the ‘Virtual Library’ of Manuscripts.” In *Digitizing Medieval and Early Modern Material Culture*, edited by Brent Nelson and Melissa M. Terras, 137–69. New Technologies in Medieval and Renaissance Studies, v. 3. Toronto, Ontario, Canada : Tempe, Arizona: Iter, Inc. ; ACMRS (Arizona Center for Medieval and Renaissance Studies), 2012.

    - examines problems in the circulation and availability of digital facsimiles; identifies questions "of access and 'democratization,' of copyright and reproduction rights" (159) as some of the most urgent that the field faces right now; images are copyrighted and often made inaccessible (this has changed with the introduction of IIIF, by the way)

17. Burrows, Tony. “Medieval Manuscripts and Their Digital Afterlives.” In The Routledge Research Companion to Digital Medieval Literature. Routledge, 2017. https://doi.org/10.4324/9781315696041-9.

    - explains that the number of manuscripts that are still to be digitized is very high:

    > Fabian and Schreiber estimate that only 7.5 percent of Germany's 60,000 medieval manuscripts have been digitized; this is a in country that has invested significant amounts already in digitization and has developed a national strategy for future work. There is no reason to think that the proportion is any higher across the rest of Europe and North America.

    - covers the kind of potential opened up by mass digitization

18. Roberts, Jane. *Guide to Scripts Used in English Writings up to 1500*. London: British Library, 2005.

    - Offers some interesting clarifications concerning her transcriptions.

    > The transcriptions present, as far as it is practicable, the letter-shapes, punctuation, and layout of the manuscript pages reproduced. Every attempt is made to avoid editorial interference. Yet, because it is incumbent on any transcriber to understand the text as it is read, no attempt is made to reproduce the spaces (or indeed lack of spaces) between words or parts of words. Instead the word divisions that might be expected in a modern critical edition are presented, and <-> is used at line endings where necessary to identify divided words. As far as possible, capitals and other distinctive letter-forms are represented in the transcription, with attention drawn to further significant features in the commentaries. (8)

    - She also explains the importance that some stylistic features (letter forms and their placement, abbreviations, use of tironian et or ampersand) might have on paleographic assessments (quality and status of the document or book, date of production, influence, region).
