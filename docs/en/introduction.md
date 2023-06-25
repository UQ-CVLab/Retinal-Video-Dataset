---
layout: page
title: Introduction
permalink: /docs/en/introduction
key: docs-introduction
---

The observation of the retinal vasculature patterns serves as a reliable approach to tracking the morphological changes of eyes over time. 
These morphological changes have been found to be closely associated with a spectrum of ocular diseases, e.g., diabetic retinopathy, age-related macular degeneration, and glaucoma. 
Retinal vessel segmentation aims to provide pixel-level extraction of the visible vasculature from a fundus image. 
It is the initial yet fundamental step in objectively assessing vasculature in fundus images and quantitatively interpreting associated morphometrics. 
Thus, this task plays a pivotal role in understanding and diagnosing ocular diseases.


Research in retinal vessel segmentation fundamentally relies on the availability of relevant datasets.
The datasets used in existing methods for retinal vessel segmentation are all image-based. 
The static nature of images inherently limits their ability to portray dynamic retinal characteristics, e.g., vessel pulsations. 
These dynamic phenomena play a vital role in facilitating comprehensive and in-depth understanding of retinal functionality and vasculature structure. 
Moreover, image-based datasets are captured by expensive bench-top ophthalmic equipment, which is operated by professionally trained clinicians. 
Such requirements potentially limit the scale of the datasets and data diversity, thereby adversely affecting the generalization ability of the models trained on these datasets.


Here, we introduce the first video-based retinal vessel dataset (RVD), a collection of 635 smartphone-based videos with detailed vessel annotation. 
All captured videos have a frame rate of 25 frames per second, with the duration varying between 2 to 30 seconds.
The total number of frames in our dataset is over 130,000.
These videos are recorded from four clinics, including patients from 50 to 75 years old.
More specifically, 264 males and 151 females are included here.


The annotations provided in our dataset span two dimensions: spatial and temporal. 
In the spatial dimension, we offer three distinct levels of annotations: binary vessel masks, general vein-artery masks, and fine-grained vein-artery masks.
Each kind of annotation is tailored to specific clinical purposes. 
In the temporal dimension, we focus on the optic disk regions of videos where the retinal vessel fluctuation normally occurs.
We select and annotate frames with the maximal and minimal pulse widths as well as label the existence of spontaneous retinal venous pulsations (SVP).


The usage of smartphone-based devices offers better flexibility and portability, allowing for scalable data collection. 
The sequential frames capture the continuous changes in retinal vessels and thus significantly facilitate the analysis of subtle fluctuations in the retinal structure. 
To the best of our knowledge, RVD is the first mobile-device based and video based dataset for retinal vessel segmentation.
