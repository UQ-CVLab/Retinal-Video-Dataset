---
layout: page
# title: Dataset
permalink: /docs/en/dataset
key: docs-dataset
article_header:
  type: overlay
  theme: dark
  height: 60vh
  background_color: '#203028'
  background_image:
    gradient: 'linear-gradient(135deg, rgba(34, 139, 87 , .4), rgba(139, 34, 139, .4))'
    src: /docs/assets/images/RVD_title.png
aside:
  toc: true
---
      


<br/> 
<div style="text-align:center;">
    <b><a style="font-size: 25px;" href="LINK_TO_ARXIV_PAPER">[Arxiv]</a></b>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    <b><a style="font-size: 25px;" href="https://drive.google.com/drive/folders/1rPbRKBS-28yu7AlMJksbrOQ6bGhNkqL1?usp=sharing">[Download]</a></b>
</div>
<div>&nbsp;</div>


<!-- ## Download

<button style="font-size:20px">Retinal Vessel Dataset [<i class="fa fa-download"></i>](https://drive.google.com/drive/folders/1rPbRKBS-28yu7AlMJksbrOQ6bGhNkqL1?usp=sharing)</button> -->

<!-- <i style="font-size:24px" class="fa">&#xf019;</i> [Download Dataset](https://drive.google.com/drive/folders/1rPbRKBS-28yu7AlMJksbrOQ6bGhNkqL1?usp=sharing) -->

## Data Structure
```bash
├── Videos
│   └── 1080_crop
├── Sptatial Annotations
│   └── images
│   └── masks
│   └── statistics
├── Temporal Annotations
│   └── images
│   └── masks
└── Metadata
```

## Citation
If you find our RVD dataset is useful in your research, please consider cite:


```latex
@article{MD2023RVD,
  title={RVD: A Handheld Device-Based Fundus Video Dataset for Retinal Vessel Segmentation},
  author={MD WAHIDUZZAMAN KHAN, Hongwei Sheng, Hu Zhang, Heming Du, Sen Wang, Minas Theodore Coroneo, 
  Farshid Hajati, Sahar Shariflou, Michael Kalloniatis, Jack Phu, Ashish Agar, Zi Huang, Mojtaba Golzan, Xin Yu},
  journal={arXiv preprint arXiv},
  year={2023}
}
```

<!-- ## Dataset Collection


The dataset was collected in compliance with the guidelines of the Tenets of Helsinki and with written consent from all participants. Data collection involved the use of hand-held fundus imaging devices made by attaching smartphones to fundus camera lenses. These devices were operated by clinicians to capture fundus videos from patients during their routine medical examinations. -->




<!-- ## What we provide


&nbsp; - 415 participants (264 males and 151 females, age range: 50-75 years).

&nbsp; - 635 RGB videos with a frame rate of 25 frames per second.

&nbsp; - Duration varies between 2 to 30 seconds.

&nbsp; - Videos were collected over five years using different smartphones.

&nbsp; - Spatial and temporal annotations annotated by trained experts. -->


## Annotations
### Spatial Annotations


The spatial annotations help to understand the structure of vessels, the differences between retinal arteries and veins, and the characteristics of each vein and artery.


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

**Binary vessel masks:** Binary vessel masks describe the main structures of retinal vessels. They are frequently used in retinal vessel segmentation. They do not distinguish between arteries and veins.

**General vein-artery masks:** This type of annotation helps to distinguish between retinal arteries and veins, which is essential as many diseases have different effects on arterial and venous structures.

**Fine-grained vein-artery masks:** We further divide each artery or vein into four segments based on its width, resulting in the final eight-class masks. These masks precisely reflect the granularities of retinal vessels and are highly demanded when detecting ocular diseases.

<!-- The vessel diameters were automatically measured and segments were categorized into different levels (0 to 3) based on ratios to the largest diameter. Clinicians validated the quality of these fine-grained segmentation masks. -->



### Temporal Annotations
Spontaneous retinal Venous Pulsations (SVPs) play a crucial role as a biomarker in retina assessments. This type of annotations helps to study SVPs.

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



**Existence of SVPs:** We provide the annotations to indicate the presence or absence of SVPs in each video, resulting in 335 “SVP-present” videos and 300 “SVP-absent” videos. 

**Temporal duration of SVPs:** We further provide temporal emergence annotations of SVP by indicating the starting and ending frames of retinal vessel fluctuation. The detailed duration of SVP serves two purposes: it acts as a valuable signal to improve the performance of SVP detection tasks and sets a new task for SVP temporal localization.

**“Peak” and “Trough” annotations of SVPs:** For each ''SVP-present'' video, masks for frames with the maximal dilation (''peak'') or maximal contraction (''trough'') are provided.



## Tools
<button style="font-size:20px">[<i class="fa fa-download"></i>](https://drive.google.com/drive/folders/1rPbRKBS-28yu7AlMJksbrOQ6bGhNkqL1?usp=sharing)</button> : We provide some codes for data preprocessing, which can be used to generate the split files. 


 <button style="font-size:20px">[<i class="fa fa-download"></i>](https://drive.google.com/drive/folders/1rPbRKBS-28yu7AlMJksbrOQ6bGhNkqL1?usp=sharing)</button> : We also provide the codes to obtain the benchmark results.

## Ethics

<!-- All protocols for data collection adhered to the Tenets of Helsinki. Written informed consent was obtained from all participants. -->

RVD dataset is collected in accordance with the guidelines of the Tenets of Helsinki. Written consent was obtained from all participants prior to any data collection, and all examination protocols adhered to the tenets of the Declaration of Helsinki.


<!-- ## Data Split

The dataset is partitioned considering patient-wise splits to reduce inter-set similarity. 517 videos are used for training and validation, and 118 videos are used for testing. The data split is performed based on patient IDs to ensure videos from the same patient are in the same subset. -->




<!-- [Code A]():
[Code B]():  -->
<!-- ## Acknowledgements

We thank the participating clinicians and patients for their invaluable contribution to this study. -->


<!-- ## Annotations -->


<!-- 
## Dataset Format






## Download -->