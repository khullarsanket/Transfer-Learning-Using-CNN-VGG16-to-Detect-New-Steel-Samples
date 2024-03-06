# Transfer Learning Using CNN VGG16 to Detect New Steel Samples

## Project Overview

This repository explores an innovative approach to classifying steel micrograph images from the CMU-UHCS dataset using transfer learning from the VGG16 Convolutional Neural Network (CNN). By harnessing pretrained weights from VGG16's convolutional layers, we generate feature vectors for input images, which are then used for binary classification with a Support Vector Machine (SVM).

![image](https://github.com/khullarsanket/Transfer-Learning-Using-CNN-VGG16-to-Detect-New-Steel-Samples/assets/119709438/4631a68c-84cd-4d95-9966-1a4aa4605ba4)

## Key Features

- **Feature Extraction with VGG16:** Utilizes VGG16 up to various max-pooled layers for depth-specific feature extraction.
- **SVM Classification:** Implements one-vs-one approach in SVM for binary classification across four distinct steel micrograph categories, leading to multilabel classification through majority voting.
- **Cross-validation:** Employs cross-validation error for comparative analysis between one-vs-one and multilabel classifiers.

![image](https://github.com/khullarsanket/Transfer-Learning-Using-CNN-VGG16-to-Detect-New-Steel-Samples/assets/119709438/fa7b91b5-1b7b-425d-a42e-be47c3228c32)

## Methodology

1. **Feature Vector Generation:** Extracts features from input images using different depths of VGG16, translating these into arrays of size corresponding to the depth's number of filters.
2. **SVM Implementation:** Uses the extracted feature vectors for training SVM classifiers in a one-vs-one scheme, culminating in a multilabel classification system.
3. **Validation:** Validates classifiers' performance using cross-validation error metrics.

## Getting Started

Follow the instructions for setting up the environment, using the pretrained VGG16 model for feature extraction, training the SVM classifiers, and evaluating the system's performance on new steel sample images.

## Conclusion

This project demonstrates the efficacy of combining transfer learning from CNNs with SVM for the classification of steel micrograph images, showcasing the potential for advanced materials characterization.

