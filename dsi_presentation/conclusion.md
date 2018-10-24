## Conclusions

Our project showed that OCR can successfully transcribe medieval handwriting within a 10-X% error rate. While these results are still rather preliminary, and more experiments should be run with many different scripts, scribes, and manuscripts, OCR appears to be a promising tool for future medieval studies.

After encountering various challenges compiling our training data and running the OCR system, we have several recommendations for similar research projects:

1. **Create an abbreviation and character standard which is crowd-sourced and easily accessible online.** Such a standard is essential for producing consistent training data, especially if future transcription projects are crowd-sourced across universities and scholars. We have begun such a guide on our GitHub page (link), but look forward to working with other medievalists to edit and develop it in the future.

2. **Experiment with the training data and OCR system**. We plan to retrain the OCR system with new or modified training data in order to see whether can get better training results. For example, our next training will use grayscale rather than binary images. We will also experiment with different OCR systems, for example Transkribus (an OCR engine run by a team at the University of Innsbruck).

3. **Generate models based on different scripts, scribes, languages, and manuscripts.** While our current OCR model is solely trained on one manuscript (Corpus Christi MS 198), one scribe (Scribe D), one language (Middle English), and one script (Anglicana Formata), there are many more variations which we hope to experiment with, and encourage other scholars to try as well.

4. **Push for more digitized manuscripts whose images are publicly available**. Perhaps the greatest obstacle confronting this and similar research projects remains the lack of digitized manuscript images. The vast majority of manuscripts are not digitized and therefore cannot be used for either OCR training or transcription. Researchers should encourage institutions to digitize their manuscripts and make their images freely available to the public (or at least to researchers). Otherwise, these manuscripts are even more likely to vanish from intellectual and cultural history.
