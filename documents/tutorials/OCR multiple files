---
title: "Tutorial on how to OCR multiple files at once"
---

- Place the model in the folder that contains the images that you intend to OCR;
- To OCR:

```
for i in $(ls *.tif); do kraken -i $i ${i/.tif/_ocrd.txt} binarize segment ocr -m model_best.mlmodel; done
```

- To combine the files into a single .txt file (works if they are in the right order):

```
cat *.txt > ocr_combined.txt
```
