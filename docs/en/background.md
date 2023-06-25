---
layout: page
title: Why do we need Retinal Video Dataset?
permalink: /docs/en/background
key: docs-background
---



## ⭐ Video-based


Existing methods for retinal vessel segmentation are designed on image-based datasets. Although these datasets have contributed valuable vessel annotations for studying retinal segmentation, the static nature of images inherently limits their ability to portray dynamic retinal characteristics, e.g., vessel pulsations. These dynamic phenomena play a vital role in facilitating comprehensive and in-depth understanding of retinal functionality and vasculature structure.

The sequential frames in our RVD dataset capture the continuous changes in retinal vessels and thus significantly facilitate the analysis of subtle fluctuations in the retinal structure.


<head>
    <style>
        .container {
            display: flex;
            /* justify-content: space-between; Creates space around items */
            justify-content: center;
        }

        .image-container-0 {
            width: 40%;
            flex-shrink: 0; /* Prevents the images from shrinking */
            text-align: center; /* Center the caption */
            margin: 0 50px; /* Adds 10px of space on the left and right of each image */
        }

        .image-container-0 img {
            width: 100%;
            height: auto;
        }

        .caption {
            margin-top: 10px; /* Creates space between image and caption */
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="image-container-0">
            <img src="../assets/images/image_based_dataset.png" alt="Description of Image 1">
            <p class="caption">Image-based Data</p>
        </div>
        <div class="image-container-0">
            <img src="../assets/images/video_based_dataset.gif" alt="Description of Image 2">
            <p class="caption">Video-based Data</p>
        </div>
    </div>
</body>




## ⭐ Hand-held


In recent years, advances in imaging technology have enabled the usage of smartphone-based devices for retinal observation. They offer better flexibility and portability, allowing for scalable data collection. 
However, existing image-based datasets are captured by expensive bench-top ophthalmic equipment, which is operated by professionally trained clinicians. 
Such requirements potentially limit the scale of the datasets and data diversity, thereby adversely affecting the generalization ability of the models trained on these datasets.

 

Therefore, the provision of the video modality and the use of portable devices for data acquisition and remarkably overcome the limitations of existing datasets.
To the best of our knowledge, RVD is the first mobile-device based and video based dataset for retinal vessel segmentation.

<head>
    <style>
        .container {
            display: flex;
            /* justify-content: space-between; Creates space around items */
            justify-content: center;
        }

        .image-container-1 {
            width: 45%;
            flex-shrink: 0; /* Prevents the images from shrinking */
            text-align: center; /* Center the caption */
            margin: 0 50px; /* Adds 10px of space on the left and right of each image */
        }

        .image-container-1 img {
            width: 100%;
            height: auto;
        }

        .caption {
            margin-top: 5px; /* Creates space between image and caption */
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="image-container-1">
            <img src="../assets/images/traditional_device.png" alt="Description of Image 1">
            <p class="caption">Bench-top Device</p>
        </div>
        <div class="image-container-1">
            <img src="../docs/assets/images/handheld_device.png" alt="Description of Image 2">
            <p class="caption">Handheld Device</p>
        </div>
    </div>
</body>




