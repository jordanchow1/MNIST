# MNIST Binary Classifier Using Scikit-Learn

## Overview
This repository contains a Jupyter Notebook that demonstrates how to prepare and analyze the MNIST dataset for a binary classification task. The goal is to determine whether a given handwritten digit is a "5" or not. The notebook covers:
- Loading and visualizing the MNIST dataset
- Preprocessing and converting multi-class labels into binary labels
- Training a binary classifier using Scikit-Learn
- Evaluating model performance using cross-validation

## Features
- **Data Loading:** Retrieves the MNIST dataset using Scikit-Learn's `fetch_openml`.
- **Data Visualization:** Displays sample digit images using Matplotlib to ensure correct reshaping.
- **Preprocessing:** Converts raw labels to `uint8` type and splits the dataset into training and testing sets.
- **Binary Labeling:** Converts the multi-class labels into binary labels (`True` for digit 5, `False` otherwise).
- **Model Training:** Trains a binary classifier using algorithms such as Logistic Regression, Support Vector Machines (SVM), or Stochastic Gradient Descent (SGDClassifier).
- **Evaluation:** Uses cross-validation and computes precision, recall, and F1 score to assess model performance.

## Dataset
The MNIST dataset consists of 70,000 grayscale images of handwritten digits (0-9). Each image is 28x28 pixels, flattened into a 784-dimensional vector.
- **Training Set:** 60,000 images
- **Test Set:** 10,000 images

## Data Preparation and Binary Classification
The notebook follows these key steps:

### 1. Loading the Data
- Fetches the MNIST dataset using `fetch_openml` and converts it into NumPy arrays.
- Verifies the dataset shape: `(70000, 784)`, confirming each image is properly flattened.

### 2. Data Visualization
- Reshapes and displays a sample image using Matplotlib to verify the data integrity.
- Ensures that the visualization process correctly reconstructs the images from 1D arrays.

### 3. Preprocessing
- Converts label data type to `np.uint8` for compatibility.
- Splits the dataset into:
  - **Training Set:** 60,000 images
  - **Test Set:** 10,000 images

### 4. Binary Label Conversion
- Creates new label arrays (`y_train_5` and `y_test_5`) where:
  - `True` if the digit is 5.
  - `False` otherwise.
- Confirms label transformation by verifying that the first image is correctly identified as a 5.

## Model Training
The binary classifier is trained using **Stochastic Gradient Descent (SGDClassifier)**, which is well-suited for handling large datasets efficiently.

## Model Evaluation
To assess model performance:
- **Cross-validation** is performed to ensure the model generalizes well.
- **Performance Metrics** include:
  - **Precision:** Measures how many predicted 5s were actually 5s.
  - **Recall:** Measures how many actual 5s were correctly identified.
  - **F1 Score:** Balances precision and recall for a more comprehensive evaluation.
