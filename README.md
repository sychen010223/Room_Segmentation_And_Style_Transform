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
    git clone https://github.com/your-username/your-repo.git
    cd your-repo
2. **Segmentation**: Run the segmentation module on your input images using the pretrained weights. The module will generate segmentation maps for each image, indicating the location of furniture objects.
3. **Style Transformation**: Utilize the TensorFlow Hub model to apply artistic styles from style images to the segmented furniture objects. This step enables dynamic and customizable image stylization.

5. **Results**: Evaluate the segmentation accuracy and visually assess the style transformations. You can find example outputs in the `results/` directory.

## Future Work

We believe that the integration of these models offers significant utility in interior design and related creative fields. However, there are several avenues for future improvement and exploration:

- Fine-tuning the segmentation model on domain-specific datasets to improve accuracy on furniture segmentation.
- Experimenting with different style transfer models and techniques to achieve even more visually appealing style transformations.
- Extending the approach to handle other types of objects or incorporate additional semantic information for more detailed scene understanding.
