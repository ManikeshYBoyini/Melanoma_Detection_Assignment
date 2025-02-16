# Melanoma Detection

> This project aims to build a Convolutional Neural Network (CNN) model capable of accurately detecting melanoma, a potentially deadly form of skin cancer. Melanoma accounts for 75% of skin cancer deaths, making early detection crucial. A reliable system that can analyze skin images and alert dermatologists about the presence of melanoma has the potential to significantly reduce manual diagnostic efforts.

## Table of Contents
- [Problem Statement](#problem-statement)
- [Project Pipeline](#project-pipeline)
- [Technologies Used](#technologies-used)
- [Acknowledgements](#acknowledgements)

## Problem Statement

### Business Understanding

The dataset consists of 2,357 images of both malignant and benign skin lesions, sourced from the International Skin Imaging Collaboration (ISIC). These images have been categorized based on the ISIC classification system, with some subsets slightly imbalanced due to a higher prevalence of melanomas and moles.

The dataset includes images of the following skin conditions:

- Actinic keratosis
- Basal cell carcinoma
- Dermatofibroma
- Melanoma
- Nevus
- Pigmented benign keratosis
- Seborrheic keratosis
- Squamous cell carcinoma
- Vascular lesion

### Business Goal

The goal of this project is to develop a multiclass classification model using a custom CNN in TensorFlow to accurately classify the different types of skin lesions. The model should help dermatologists with early melanoma detection, potentially saving lives through quicker intervention.

### Business Risk

- Incorrect classification of skin cancer types could lead to inappropriate treatment and missed opportunities for early intervention.

## Project Pipeline

### 1. Data Reading and Understanding
- Define paths for both training and testing images in the dataset.
  
### 2. Dataset Creation
- Create training and validation datasets with a batch size of 32.
- Resize images to 180x180 pixels for uniformity.

### 3. Dataset Visualization
- Implement code to visualize one example from each of the nine disease classes.

### 4. Model Building & Training (Initial Model)
- Build a CNN model that can classify images into the nine disease categories.
- Normalize pixel values between 0 and 1 to aid model convergence.
- Choose an appropriate optimizer and loss function for training.
- Train the model for ~20 epochs and evaluate performance.
- Assess overfitting or underfitting and note findings.

### 5. Data Augmentation
- Apply a suitable data augmentation strategy to combat overfitting/underfitting and enhance model generalization.

### 6. Model Building & Training (With Augmented Data)
- Build the CNN model as before, but with augmented data.
- Normalize pixel values, choose an optimizer, and loss function.
- Train for ~20 epochs and analyze model performance.
- Compare results with the previous model to determine if overfitting/underfitting issues have been resolved.

### 7. Class Distribution Analysis
- Evaluate the current class distribution within the training dataset.
- Identify which class has the fewest samples.
- Identify which classes are dominant in terms of sample size.

### 8. Handling Class Imbalances
- Use the Augmentor library to rectify class imbalances in the training dataset.

### 9. Model Building & Training (With Rectified Class Imbalance)
- Rebuild the CNN model, again normalizing pixel values and choosing the right optimizer and loss function.
- Train the model for ~30 epochs.
- Analyze the impact of addressing class imbalances on model performance and check for resolved issues.

## Technologies Used

- **TensorFlow**: For building and training the CNN model.
- **Keras**: For deep learning model construction.
- **Python**: For data processing and model implementation.
- **Augmentor**: For handling class imbalances through data augmentation.

## Acknowledgements

- **ISIC (International Skin Imaging Collaboration)**: For providing the dataset.
- **TensorFlow/Keras Documentation**: For guidance in model building and training.
