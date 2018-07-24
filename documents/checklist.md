---
title: "To-do list for OCRMEMS"
date: May 2018
---

## Tasks for the summer

### Part 1. Preliminary transcriptions

- [x] Manually transcribe 40 pages of CC MS 198 (ff. 16r-35v)

    - [x] Develop Transcription Standard
        - [x] Find Unicode Latin abbreviation stuff, collect manuscript weird stuff
    - [x] Complete Scribe D Guide (letters plus abbreviations)
    - [ ] Complete MS 198 description (after reading various sources)
    - [x] Figure out what to do about book transcription/"gold standard"

- [x] Double check transcriptions

### Part 2. Trial run

- [X] Crop all images (find efficient way)
- [ ] Trial run with one or two pages

### Part 3. Training

- [ ] Split up transcription work and transcribe
- [ ] Train

### Part 4. Testing

- Compile transcriptions for:
  - [ ] CC MS 198 ff. 160r-164v
  - [ ] Harley MS 7334 ff. 63v-68v [link](http://www.bl.uk/manuscripts/Viewer.aspx?ref=harley_ms_7334_fs001r)
  - [ ] Cambridge Trinity MS B.15.17 ff. 121r-123v  [link](http://trin-sites-pub.trin.cam.ac.uk/james/viewpage.php?index=216)
  - [ ] (not sure) Huntington Library HM 114  [link](http://hdl.huntington.org/cdm/compoundobject/collection/p15150coll7/id/31197/rec/1)
  - [ ] Cambridge R.3.2 ff.140v-145r [link](http://trin-sites-pub.trin.cam.ac.uk/manuscripts/R_3_2/manuscript.php?fullpage=1&startingpage=156)
- [ ] Test against training data
- [ ] Test against other parts of manuscript
- [ ] Test against other Scribe D manuscripts
- [ ] Test against non-Scribe D manuscripts

### Part 5. Analysis

- [ ] Data analysis
- [ ] Write up results

#### Questions

1. What's the status of the User Interface? Should we wait before we input the transcription for the training, or can we go ahead? What are the advantages of using the new interface? Can we start by using one interface and finish the job by using the other?

2. Transcription conventions.

    - Multiple forms for the same letter: long s, kidney-shaped s, sigma-shaped s; should we have different characters for different letter forms, or will the software be able to work with radically different letter forms associated with the same character?

    - Opposite case: letter forms that feature very small differences: the __h__ with a cross stroke and the dotted __y__; would it be better for the software if we associated slightly different letter forms with the same character?

    - Another problem we have is the distinction between upper-case and lower-case letters; at times it is very hard to distinguish between the two (although the edition we are using does); at times it is just a matter of shading behind the letter. Do you have any advice about this?

    - We have tried to find ways to match each special letter form--letter forms that signify abbreviations (superscript vowels and consonants, curls and hooks)--with a specific Unicode character. It has worked well so far, but we were wondering if it is the best approach. Do you have any suggestions? Have you encountered anything similar?

3. What are the next steps? How do we decide on what other parts of the text to transcribe manually? How much of the document should we transcribe manually? How do we determine how accurate the software is?
