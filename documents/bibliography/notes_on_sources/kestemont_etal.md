Kestemont, Mike, Vincent Christlein, and Dominique Stutzmann.	"Artificial Paleography: Computational approaches to identifying Script Types in Medieval Manuscripts." _Speculum_. October 2017.

- Useful introduction on state of digital paleography  
- Interested in identifying script types, specifically distinguishing between two scripts (not transcribing).
- This kind of software will be useful for machine learning because a machine can first identify the kind of script, then apply the OCR model corresponding to that script for transcription.
- Mentions an conference called International Conference in Handwriting Recognition.
- "Conventional OCR applications still have huge difficulties in processing continuous script forms and their ligatures." (p. 89)
- Also good model for crowdsourcing the problem.
- They point to two programs, FAU (Bag of Words, SIFT keypoints) and DeepScript (neural network).
- FAU did better at identifying script in single script images, DeepScript did better at identifying two separate scripts in mixed script images.
- Main takeaways: AI recognition is fuzzy because paleography itself is fuzzy. The programs were better at identifying discrete scripts, as opposed to hybrid scripts. We might then reconsider "ground truths" in paleography to begin with (that is, script classifications). For machine learning, might mean merging script types for models.
- Also worth noting: neural network layers seem to be identifying primary morphological features (loops and ascenders). Sensitivity of higher level patterns might relate to regularity of script. Visualizations of t-SNE descriptors can illustrate similarities between scripts.
