# Batik-Classification

## Overview 
This project aims to address the challenge of classifying various Indonesian batik motifs using deep learning techniques. By leveraging deep neural networks, which have proven effective in pattern recognition and image classification tasks, we aim to develop an automated system capable of accurately identifying and classifying different batik motifs, including Batik Bali, Batik Keraton, and Batik Betawi.

## Workflow

### Collecting Data 
Data collection for this project is conducted through Kaggle, an online repository that provides a variety of public datasets. The dataset used, titled 'Indonesian Batik Motifs' curated by DionisiusDH, contains 20 folders of high-resolution Indonesian batik motif images. For this project, we specifically utilize three folders, each containing 50 images representing Batik Bali, Batik Keraton, and Batik Betawi, which symbolize the rich textile cultural heritage of Nusantara. The dataset can be accessed via the following link: [Indonesian Batik Motifs on Kaggle](https://www.kaggle.com/datasets/dionisiusdh/indonesian-batik-motif).

### Data Preprocessing
The data preprocessing phase begins with verifying the distribution of images to ensure the quantity and presence of data are accurate. All images are then resized to 256x256 pixels. We apply normalization by setting the pixel values to a range of 0 to 1 (rescale = 1./255). Additionally, a series of random transformations are applied to the training data to enhance diversity and prevent overfitting. These transformations include random rotation within a 20% range, random changes in brightness and contrast by up to 10%, random zooming by up to 10%, and random horizontal and vertical flipping.

### Modelling 
We build models utilizing Convolutional Neural Network (CNN) built and trained with TensorFlow framework. We developed 2 kinds of models, scratch CNN based model and transfer learning based model with MobileNetV2. Both of models are experimented with hyperparameter tuning to improve models' accuracy.

### Accuracy Results 
The accuracy is acquired by test data (10% of overall dataset) evaluation
1. Scratch model
   - Before Hyperparameter tuning : **43%**
   - After Hyperparameter tuning : **40%**
3. Transfer learning model
   - Before Hyperparameter tuning : **27%**
   - After Hyperparameter tuning : **70%**

