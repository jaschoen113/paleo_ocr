# OCR and Medieval Manuscripts 

This project uses OCR on a corpus of medieval manuscripts. Manuscripts pose significant challenges to automated processing, as they feature elaborate and often cryptic handwriting systems (scripts) which vary dramatically across period, region, and scribe. They also tend to contain extensive marginal elements (such as decorations, annotations, or tears) that an engine should be trained to ignore, or treat differently. Finally, given that the most advanced OCR engines often rely on comprehensive dictionaries to improve accuracy, the inconsistent orthography of medieval languages (like Middle English) poses an additional obstacle to efficient automated transcription.

We use [Kraken](http://kraken.re/index.html), a turn-key OCR system forked from Ocropus. We have begun training Kraken on a select set of 15th century Middle English manuscripts attributed to the same scribe (“Scribe D”), starting with *The Canterbury Tales* Oxford Corpus Christi MS 198. Long-term, we hope to train the system on a much larger corpus of manuscripts of various scripts and quality.   

We have achieved promising results so far: a 2.84% CER (character error rate) on the training set, and a range of 
14.46% to 73.23% CERs on unseen manuscripts. 

In this repository you can find our training data for MS 198, OCR models, full transcriptions of our training and testing manuscripts, and a guide to the abbrevations we used in our transcriptions (with a discussion of these decisions). We also have relevant resources on OCR and paleography. 
