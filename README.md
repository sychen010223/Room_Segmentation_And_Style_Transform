# Room_Segmentation_And_Style_Transform
This repository contains the code and models for a deep learning-based approach to accurate furniture segmentation and effective style transformation in room images. By combining a segmentation module with an arbitrary image stylization model, our hypothesis is to enhance and stylize images through advanced machine learning techniques.

## Overview

Our approach utilizes two key models:
1. **Semantic Segmentation Model**: We employ a semantic segmentation model based on the "resnet50dilated" architecture, pretrained on the ADE20K dataset for object recognition. This model consists of a network encoder and decoder, producing a segmentation map with 150 classes. We leverage pretrained weights to enhance accuracy.
2. **Arbitrary Image Stylization Model**: We utilize the "arbitrary-image-stylization-v1-256" model from TensorFlow Hub for style transfer. This model allows us to apply artistic styles from given style images to content images, enabling dynamic and customizable image stylization.

## Evaluation

To validate the effectiveness of our segmentation model, we conducted an evaluation by comparing its outputs with ground truth annotations. We selected a diverse subset of 10 images from the validation set for this analysis. Our evaluation focused on assessing consistency and accuracy by measuring the percentage of matching pixels between the model's predictions and the ground truth annotations.

## Usage

1. **Installation**: Start by cloning this repository to your local machine.  
    `git clone` https://github.com/sychen010223/Room_Segmentation_And_Style_Transform  
    `cd Room_Segmentation_And_Style_Transform`
2. **Run the Test Code**: Locate the `Demo.ipynb` file in `Segmentation_Process/` directory and execute it. This file contains the code to load the provided pre-trained models and weights. It applies the segmentation module and style transformation to a sample set of images.
3. **View the Results**: After running the `Demo.ipynb` file, the results will be generated, the  you can view the segmented images and the stylized versions with applied artistic styles.
4. **Evaluation**: You can find example outputs and accuracy table in the `results/` directory.

## Future Work

We believe that the integration of these models offers significant utility in interior design and related creative fields. However, there are several avenues for future improvement and exploration:

- Fine-tuning the segmentation model on domain-specific datasets to improve accuracy on furniture segmentation.
- Experimenting with different style transfer models and techniques to achieve even more visually appealing style transformations.
- Extending the approach to handle other types of objects or incorporate additional semantic information for more detailed scene understanding.
