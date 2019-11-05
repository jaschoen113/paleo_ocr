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
- [x] Trial run with one or two pages

### Part 3. Training

- [x] Split up transcription work and transcribe
- [x] Train
- [ ] Remove extra lines from dataset
- [ ] Deskew and crop all images with Scantailor
- [ ] Retrain in grayscale


### Part 4. Testing

- [ ] Figure out how to properly test model (e.g. how many lines necessary per MS)
- Compile transcriptions for:
  - [x] CC MS 198 ff. 160r-164v (~350 lines) *Gianmarco*
      - [ ] Images processed
  - [ ] Harley MS 7334 ff. 63v-68v (~350 lines) *Gianmarco* [link](http://www.bl.uk/manuscripts/Viewer.aspx?ref=harley_ms_7334_fs001r)
      - [x] Images processed
  - [x] Cambridge Trinity MS B.15.17 ff. 119v-123v (~350 lines) *Jenna* [link](http://trin-sites-pub.trin.cam.ac.uk/james/viewpage.php?index=216)
      - [x] Images processed
  - [ ] Oxford Corpus Christi 201 ff. 82r-86v *Jenna* [link](http://image.ox.ac.uk/show?collection=corpus&manuscript=ms201)
      - [ ] Images processed
  - [x] Cambridge R.3.2 ff. 139v-143r (~700 lines) [link](http://trin-sites-pub.trin.cam.ac.uk/manuscripts/R_3_2/manuscript.php?fullpage=1&startingpage=156)
      - [x] Images processed
- [ ] Test against training data
- [ ] Test against other parts of manuscript
- [ ] Test against other Scribe D manuscripts
- [ ] Test against non-Scribe D manuscripts

### Part 6. Retraining

- [ ] Retrain model using Part 5 manuscripts to get new training error rate
ß
### Part 5. Analysis

- [ ] Data analysis
- [ ] Write up results