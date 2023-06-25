---
layout: page
title: Dataset
permalink: /docs/en/dataset
key: docs-dataset
---


## Dataset Collection


The dataset was collected in compliance with the guidelines of the Tenets of Helsinki and with written consent from all participants. Data collection involved the use of hand-held fundus imaging devices made by attaching smartphones to fundus camera lenses. These devices were operated by clinicians to capture fundus videos from patients during their routine medical examinations.



## Dataset Composition


&nbsp; - 415 participants (264 males and 151 females, age range: 50-75 years).

&nbsp; - 635 RGB videos with a frame rate of 25 frames per second.

&nbsp; - Duration varies between 2 to 30 seconds.

&nbsp; - Videos were collected over five years using different smartphones.

&nbsp; - Spatial and temporal annotations provided by trained clinicians.


## Annotation
### Spatial Annotations


This type of annotation helps to distinguish between retinal arteries and veins, which is essential as many diseases have differential impacts on arteries and veins.


<head>
    <style>
        .container {
            display: flex;
            justify-content: space-between; Creates space around items
        }

        .image-with-caption {
            width: 70%;
            margin: auto;
        }

        .image-with-caption img {
            width: 100%;
            height: auto;
        }

        .image-with-caption figcaption {
            text-align: center;
        }
    </style>
</head>
<figure class="image-with-caption">
    <img src="../assets/images/spatial_annotation.gif">
    <!-- <figcaption>Spatial Annotation</figcaption> -->
</figure>


<!-- <div>{%- include extensions/youtube.html id='fMUa1jN0GUY' -%}</div> -->

**Binary Vessel Masks:** Annotations include binary masks that highlight the main structures of vessels.

**General Vein-Artery Masks:** This type of annotation helps to distinguish between retinal arteries and veins, which is essential as many diseases have differential impacts on arteries and veins.

**Fine-Grained Vein-Artery Masks:** Eight-class masks for both arteries and veins based on vessel widths. The vessel diameters were automatically measured and segments were categorized into different levels (0 to 3) based on ratios to the largest diameter. Clinicians validated the quality of these fine-grained segmentation masks.



## Temporal Annotations


<head>
    <style>
        .container {
        display: flex;
            /* justify-content: space-between; */
            justify-content: center;
        }

        .video-container {
            width: 32%;
            flex-shrink: 0; /* Prevents the images from shrinking */
            text-align: center;
            margin: 0 10px; /* Adds 10px of space on the left and right of each image */
        }

        .video-container video {
            width: 100%;
            height: auto;
        }

        .caption {
            margin-top: 10px;
        }
    </style>
</head>
<div class="container">
  <div class="video-container">
    <div>{%- include extensions/youtube.html id='zrrk7tHIhAU' -%}</div>
    <p class="caption">SVP Classification</p>
  </div>
  <div class="video-container">
    <div>{%- include extensions/youtube.html id='-DGihnkzzXg' -%}</div>
    <p class="caption">Temporal Localization</p>
  </div>
  <div class="video-container">
    <div>{%- include extensions/youtube.html id='yYtIow7Pq-M' -%}</div>
    <p class="caption">Peak and Trough</p>
  </div>
</div>



**Existence of Spontaneous Venous Pulsations (SVPs):** Clinicians annotated the presence or absence of SVPs in each video, resulting in 335 “SVP-present” videos and 300 “SVP-absent” videos. SVPs serve as a crucial biomarker in retina assessments.

**Temporal Duration of SVPs:** To eliminate ambiguity, the starting and ending frames of retinal vessel fluctuations (SVPs) were indicated for videos where SVPs were not visible throughout the whole video.

**“Peak” and “Trough” Annotations of SVPs:** Selected frames corresponding to the “peak” (maximal dilation) and “trough” (maximal contraction) states from each “SVP-present” video were annotated.






## Data Split:

The dataset is partitioned considering patient-wise splits to reduce inter-set similarity. 517 videos are used for training and validation, and 118 videos are used for testing. The data split is performed based on patient IDs to ensure videos from the same patient are in the same subset.



## Ethics

All protocols for data collection adhered to the Tenets of Helsinki. Written informed consent was obtained from all participants.


## Acknowledgements

We thank the participating clinicians and patients for their invaluable contribution to this study.


## Download Link:

[Google Drive Download Link](https://drive.google.com/drive/folders/1rPbRKBS-28yu7AlMJksbrOQ6bGhNkqL1?usp=sharing)





<!-- ## Annotations -->


<!-- 
## Dataset Format






## Download -->