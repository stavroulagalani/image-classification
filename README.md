# Brain Tumor Classification with Convolutional Neural Networks

This project is a deep learning model that classifies brain MRI images into two categories: tumor or no tumor. 
It was developed using TensorFlow and trained on a dataset of MRI scans stored in two folders: one for images with tumors and one for images without.

The goal of the project is to demonstrate how Convolutional Neural Networks (CNNs) can be used for binary image classification in a medical imaging context.
The model is trained to detect whether a tumor is present in an MRI scan, based on patterns it learns during training.

## Dataset

The dataset contains brain MRI images categorized into two folders:
- `data yes`: MRI scans that show a tumor
- `data no`: MRI scans without a tumor

Images are filtered for supported formats and resized to a consistent shape. They are also normalized to ensure efficient training.

## Preprocessing

Before training, the data is cleaned to remove unsupported or corrupt images. The images are then scaled from pixel values of 0–255 to a range of 0–1, which helps the model train more effectively.

## Model

The model is a CNN built using TensorFlow's Sequential API. It consists of several convolutional and pooling layers to extract image features, followed by dense layers for classification.
A sigmoid activation function is used in the final layer to output a probability between 0 and 1.

## Training and Evaluation

The dataset is split into training, validation, and test sets. The model is trained for 25 epochs, and its performance is evaluated using accuracy, precision, and recall metrics.
Visualizations of accuracy and loss over time help assess the model's learning progress.

## Prediction

After training, the model can be used to make predictions on new MRI images. A probability above 0.5 is classified as "tumor", while a probability below 0.5 is classified as "no tumor".

## Saving the Model

The trained model is saved in HDF5 format (`.h5`) so it can be loaded later for predictions without retraining.

## Using the Pretrained Model (`.h5`)

This project includes a pretrained brain tumor classification model saved in `models/brain_tumor_model.h5`.

## Summary

This project demonstrates how a deep learning model can be trained to classify medical images with high accuracy using a relatively simple CNN architecture.
It can serve as a starting point for more advanced projects, such as multi-class tumor classification or deployment in a web application.
