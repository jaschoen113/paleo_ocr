## Methods

[make this into a table? problem/decision]

Medieval manuscripts present many unique challenges which make automatic transcriptions difficult to produce:

1. Handwriting varies greatly across period, region, scribe, and purpose, meaning that many OCR models will be necessary to transcribe all manuscripts.

2. Manuscripts often present extensive marginal elements (e.g. decoration, annotations, rips, stains) that an engine should be trained to ignore or treat differently.

3. Scribes use extensive abbreviations whose precise meaning can very across contexts.

4. Characters are often indistinguishable and require knowledge of the language to discern.

5. Medieval languages like Middle English have wildly inconsistent orthographies, making it difficult to use natural language processing or comprehensive dictionaries.

Since our goal was to show that OCR could produce legible transcriptions, our project aimed to minimize the above problems in our initial training. Thus:

1. We trained our model on a single scribe (Scribe D) who has notoriously consistent handwriting, as well as a single manuscript (Oxford Corpus Christi 198, 15th century England).

2. This particular manuscript is very neat, well-rubricated, and has little marginal decoration.

3. While Scribe D still uses extensive abbreviations, he uses less than other scribes.

4. The manuscript's script (Anglicana Formata) has more unique and distinguishable characters than other medieval scripts (such as Gothic).

5. We did not use any dictionaries or natural language processing for this initial experiment.

Note: in the future, additional methods should be explored in order to address all these OCR challenges (e.g. training a model on extremely formal Gothic script with the help of natural language processing).

After selecting our training scribe and manuscript according to the criteria above, we proceeded with the following training and testing steps:

1. Produced training data (manual transcriptions of 1400 lines from MS 198). This step involved solving several challenges [could also make a chart with pictures here]:
    - Our scribe uses multiple forms for certain letters. For example, the "s" can take either a kidney, sigma, or long shape [insert picture]. We had to decide whether to individually transcribe these forms, or collapse them; we decided to collapse them for easier transcription and readability.  
    - It is often hard to distinguish between lowercase (minuscule) and uppercase (capital) letter forms; often the scribe has no perceivable uppercase form. Modern transcriptions usually transcribe uppercase letters according to location or semantic context, but it will be difficult (if not impossible) for an OCR system to identify such a distinction, at least without a certain level of language processing. We decided to use lowercase letters with lowercase-seeming forms.
    - Modern transcriptions usually extend abbreviations, marking abbreviated letters in italics. However, since Kraken (our OCR system) requires diplomatic transcription (one-to-one characters), we can not extend the abbreviations in our training data. Most abbreviations have no Unicode equivalent, and so we had to manually assign Unicode diacritics and compile an abbreviation/Unicode chart.

2. Trained OCR system (Kraken, a system developed by Benjamin Kiessling at Leipzig) and acquired initial training results (error rate on training set).

3. Compiled ground-truth transcriptions for 4 additional manuscripts (~2000 lines)

4. Tested OCR model on these new manuscripts and collected corresponding accuracy results.
