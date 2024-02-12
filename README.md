# Pneumonia-Detection-using-Deep-learning-Approach-and-using-Grad-CAM-for-Visualization (Explainable AI)

![Screenshot 2024-02-06 191208](https://github.com/SaraElwatany/Pneumonia-Detection-using-Deep-learning-Approach-and-using-Grad-CAM-for-Visualization/assets/93448764/8939342d-3ce0-490e-a5ee-9612ab9d84ae)

## About
Pneumonia Detection from X-ray images using several pretrained Deep learning Models as VGG16, VGG19, Resnet50, MobileNetV2 in addition to a proposed CNN Architecture.
We used the "Chest X-Ray Images (Pneumonia)" Dataset from Kaggle. In this repository we implemented the "Clinical Decision Support Systems for Pneumonia Diagnosis Using Gradient-Weighted 
Class Activation Mapping and Convolutional Neural Networks Thao Minh Nguyen" paper (link of the paper will be included at the end of the README File).

## Objective

The input is a chest x-ray image in jpeg format, where the input is either diagnosed with pneumonia or not, and then the output is used to get the derivative of it with respect to the feature maps from the convolutional layers (to get the gradients), where gradients are used to get the weighted features after performing global average pooling on them, the weighted features are then aggregated to end up with just one feature map and RELU activation function is used to eliminate any negative values, the resulting heatmap is then upsampled to match the original input's size, where both (original input image & the heatmap) are summed/added to end up with the visual interpretation of the model's output.

## Approaches

We combined both The training & validation images for training our models, just like the linked paper.
In Our Implemetation 2 Approaches could've been used:
1. Using Augmentation
2. Without Augmentation

However Due to the memory overflow in colab notebooks, we weren't able to run using all mentioned forms of augmentation (described in the paper) at a time, and instead our obtained results were on the original dataset only, without using any augmentations.

## Our used parameters

![Screenshot 2024-02-12 210553](https://github.com/SaraElwatany/Pneumonia-Detection-using-Deep-learning-Approach-and-using-Grad-CAM-for-Visualization/assets/93448764/fdca8e6c-c935-40a1-b693-d644c023c14a)

## Snapshots


## Related Links
- https://www.researchgate.net/publication/352471445_Clinical_Decision_Support_Systems_for_Pneumonia_Diagnosis_Using_Gradient-Weighted_Class_Activation_Mapping_and_Convolutional_Neural_Networks
