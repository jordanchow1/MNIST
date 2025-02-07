# MNIST Binary Classifier Using Scikit-Learn

## Overview
This repository contains a Jupyter Notebook that demonstrates how to prepare and analyze the MNIST dataset for a binary classification task.
The primary focus is to identify whether a given handwritten digit is a "5" or not. The notebook guides you through loading the data, visualizing sample images, preprocessing, and converting the multi-class labels into binary labels.

## Features
- **Data Loading:** Retrieves the MNIST dataset using Scikit-Learn's `fetch_openml`.
- **Data Visualization:** Uses Matplotlib to display sample digit images, ensuring that the image data is correctly reshaped.
- **Preprocessing:** Converts raw labels to `uint8` type and splits the dataset into training and testing sets.
- **Binary Labeling:** Transforms the original multi-class labels into binary labels for the digit "5" (i.e., `True` if the digit is 5, `False` otherwise).
- **Foundations for Model Training:** The data is fully prepared for training a binary classifier using algorithms such as logistic regression, SVM, or SGDClassifier.
