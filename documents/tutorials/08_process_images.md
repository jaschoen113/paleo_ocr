---
title: "Tutorial on how to process multiple images at once"
author: G. E. Saretto
date: July 2018
---

- The command to process images for training in _kraken_ is as follows (from the [Docs](http://kraken.re/training.html) website):

    >  `$ ketos transcribe -o output.html image_1.png image_2.png ...`

- To make this instruction run for each .tif (or .png, if necessary) file in a folder, make it part of a `for` command, like in this case:

    > `for i in $(ls *.tif); do ketos transcribe -o ${i/.tif/_transc.html} $i; done`
