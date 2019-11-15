---
author: G. E. Saretto & J. Schoen
date: November 2019
title: "List of revisions for article submission"
---

### Guy #2


#### Preliminary Remarks

- [ ] Change the framing of the essay; stress that we are articulating a **low-overhead workflow** (small budget, few people involved); explain why this approach might ultimately prove more sustainable (involving more scholars, more independent projects working simultaneously on a larger, more diverse archive of training data, sharing results and strategies) than vast, oversized projects.

    - [ ] International collaboration; open-source, open-access; training data made available online.

        - He identifies two concerns in the essay:

            - "practical workflow steps": "challenges faced when preparing our training data"; "defining a **low-overhead workflow** for scholars";

            - change the terminology and the framing accordingly; ours would be the "low-overhead workflow," the small group, small budget approach; what is the value of this approach? Why is this approach more viable? (e.g., why would it be better to keep the number of manuscripts and researchers contained, and so on)

            - "broader consideration of bias and initial choices": "decisions made accordingly," "bias ad initial choices."

- [ ] Place ourselves within the preexisting conversation by highlighting how we provide the point of view of a "more general humanities scholarship."

    - He attributes to us the "point of view of a more general humanities scholarship effort deriving from a practical use-case."

    - Again, underline the fact that this story is meant for "researchers beginning to engage with HTR tools across med. studies."

- [ ] Understand how to frame the error of **overfitting**, especially in relation to "Modelling Medieval Hands."

    - Our results are not satisfying on "unseen" data ("variable accuracy rate on non-training data") because they are "a result of **overfitting** to a particular model."

- [ ] Give more emphasis to the important questions we ask (according to him);

    - are scribal hands generalizable and susceptible to OCR/HTR/ML techniques?

        - (*Seems to be a version of: Does OCR work on medieval MSs? To which our answer is: Yes.*)

    - **Is it useful to pursue overfitting to try to address or recognize an individual scribal stint or distinguish between stints?**

        - (*Unsure about this one. Did we do anything that could be defined as __pursuing overfitting__? And, do our results help us "address or recognize a stint" or "distinguish between stints"? Perhaps we could eventually argue that the fact that our model failed to do so well on unseen MSs placed outside the scribal circle proves that the people in the scribal circle were striving to develop a shared standard.*)

    - **What are the goals of text extraction in a given project or across the field?**

        - (*Another question which we may want to ask explicitly; perhaps in terms of--what if OCR cannot do better than 90-95%? What possibilities does this lower degree of accuracy open up for us?*)

#### Detailed issues to address

- [ ] Include "more careful consideration of recent literature focused on approaches to medieval texts": Ciula 2005, Stutzmann 2016, Stansbury 2009, Schomaker 2004, Dahllöf 2018.

    - [ ] Perhaps explicitly pose the question of: Is OCR the appropriate method for text extraction from images of medieval MSs?

        - (*As opposed to what?*)

- [ ] Clarify the distinction between OCR ("character recognition"), HTR (not so focused on individual characters), Machine Learning... In other words, provide "a definition of terms" to distinguish this "character-recognition approach" from other text-recognition approaches.

    - The reviewer highlights that our approach **goes beyond standard character recognition** (in other words, it is somewhat fused with HTR).

- [ ] Create a DOI for transcription guidelines and training data.

- [ ] Allude to the additional problems that would be posed by non-Western scripts and right-to-left scripts. Also, on p. 14 we allude to "most medieval MS" and to "medieval MS"; we should clarify that we are talking about Western Europe--not limit oneself to Western medieval manuscripts in Latin alphabet.

- [ ] Define what we mean by "high-resolution" (p. 15); the reviewer explains that the various databases to which we allude allow one to download their images in different formats. So, we should specify what image resolution works well with our system, and clarify how we have encountered problems when dealing with these institutions.

- [ ] Also, perhaps offer a nod to IIIF and how it has vastly increased the amount of images made available (65,000 MSs on Biblissima).

- [ ] Create a section for "lessons learned" and "things to consider" at the end of the article, to generalize the results and the methodological repercussions of our experiment.

    - "summarizing the questions we consider or synthesizing a set of standard questions or trade-offs would be immensely helpful to the field"

- [ ] On p. 14 we speculate on the possibility of integrating OCR engines with other forms of analysis; we might want to reflect on the question of how to "chain data preparation steps in a workflow"; the reviewer recommends looking at Arabnejad et. al. 2016 and the White Paper of Global Currents.
