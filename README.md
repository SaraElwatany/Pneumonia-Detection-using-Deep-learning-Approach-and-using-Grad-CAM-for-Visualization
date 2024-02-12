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

## Evaluation of our models used

![Screenshot 2024-02-12 210537](https://github.com/SaraElwatany/Pneumonia-Detection-using-Deep-learning-Approach-and-using-Grad-CAM-for-Visualization/assets/93448764/8ebd3a90-9e36-41d5-99d0-ddb5c989559c)

![Screenshot 2024-02-12 210614](https://github.com/SaraElwatany/Pneumonia-Detection-using-Deep-learning-Approach-and-using-Grad-CAM-for-Visualization/assets/93448764/1a24dcd7-69ae-4f44-b047-719e02049171)

![Screenshot 2024-02-12 210624](https://github.com/SaraElwatany/Pneumonia-Detection-using-Deep-learning-Approach-and-using-Grad-CAM-for-Visualization/assets/93448764/e4d3afb9-c20f-42ea-b959-40fcbb830d05)

## Comparison between our output & the paper's

![Screenshot 2024-02-12 210712](https://github.com/SaraElwatany/Pneumonia-Detection-using-Deep-learning-Approach-and-using-Grad-CAM-for-Visualization/assets/93448764/b292dba7-a4ec-4d27-86a7-328ac7a5d832)

![Screenshot 2024-02-12 210719](https://github.com/SaraElwatany/Pneumonia-Detection-using-Deep-learning-Approach-and-using-Grad-CAM-for-Visualization/assets/93448764/33d976b8-99a2-498a-8139-1ee581b2c9ab)

## Snapshots

![Screenshot 2024-02-12 210643](https://github.com/SaraElwatany/Pneumonia-Detection-using-Deep-learning-Approach-and-using-Grad-CAM-for-Visualization/assets/93448764/7e66ca4c-26fc-4104-b6d1-a2b22a9a9d27)

![Screenshot 2024-02-12 210655](https://github.com/SaraElwatany/Pneumonia-Detection-using-Deep-learning-Approach-and-using-Grad-CAM-for-Visualization/assets/93448764/4b679613-cc4d-45d4-9186-3e78d8dce9fc)

## Related Links
- https://www.researchgate.net/publication/352471445_Clinical_Decision_Support_Systems_for_Pneumonia_Diagnosis_Using_Gradient-Weighted_Class_Activation_Mapping_and_Convolutional_Neural_Networks
