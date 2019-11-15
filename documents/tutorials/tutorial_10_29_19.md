---
title: "Tutorial for OCR workshop at Columbia"
author: G. E. Saretto & J. Schoen
date: October 29 2019
---

## Steps

1. Having downloaded and installed it (follow the instructions [here](http://kraken.re/index.html)), activate the kraken environment through anaconda by typing `conda activate kraken`.
2. Create a folder containing the images on which you intend to train the software.
    - The images must be prepared beforehand (you can use software like ScanTailor).
3. Run `ketos transcribe` on the images in the folder; the command creates the .html page that serves as an environment for the transcription process leading to the training.
    - Note: the command takes a long time on .tif images; consider switching to .png.
    - Note: if one enters the default command the binarization does not work.
    - Note: one can binarize by using the `kraken -i [SOURCEIMAGE] [OUTPUTIMAGE] binarize` command. Might be worth running it on the whole set of images beforehand.
    - Note: to binarize the whole set of images, use: `for i in $(ls *.tif); do kraken -i $i "bina_${i/.tif/.png}" binarize; done`.
4. Once you have the .html files ready, start inserting your transcriptions.
    - Note: remember that when the system frames multiple lines incorrectly, you should ignore the section.
5. Once you have inserted your transcriptions, extract the lines using the command `ketos extract --output output_directory *.html`.
    - Note: one can normalize whitespaces by using the option `-s`.
    - Note: one can choose not to binarize the images by using the option `--no-binarize`.
    - Note: one can normalize the transcriptions by using the option `-u` followed by a specification concerning the Unicode form (`NFD`, `NFC`, `NFKD`, `NFKC`).
6. To begin the training, use the command `ketos train [TRAININGFOLDER]/*.png`.
    - Note: Kraken has options to establish for how long the training should go on.
