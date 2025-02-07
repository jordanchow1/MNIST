# MNIST Binary Classifier Using Scikit-Learn

## Overview
This repository contains a Jupyter Notebook that demonstrates how to prepare and analyze the MNIST dataset for a binary classification task.
The primary focus is to identify whether a given handwritten digit is a "5" or not. The notebook goes through loading the data, visualizing sample images, preprocessing, converting the multi-class labels into binary labels, and training a binary classifier.

## Features
- **Data Loading:** Retrieves the MNIST dataset using Scikit-Learn's `fetch_openml`.
- **Data Visualization:** Uses Matplotlib to display sample digit images, ensuring that the image data is correctly reshaped.
- **Preprocessing:** Converts raw labels to `uint8` type and splits the dataset into training and testing sets.
- **Binary Labeling:** Transforms the original multi-class labels into binary labels for the digit "5" (i.e., `True` if the digit is 5, `False` otherwise).
- **Model Training:** The data is fully prepared for training a binary classifier using algorithms such as logistic regression, SVM, or SGDClassifier.

## Dataset
The MNIST dataset is composed of 70,000 grayscale images of handwritten digits (0-9). Each image is 28x28 pixels, flattened into a 784-dimensional vector. In this project:

Training Set: The first 60,000 images.
Test Set: The remaining 10,000 images.

## Data Preparation and Binary Classification
The notebook performs the following key steps:

### Loading the Data: Fetches the MNIST dataset and converts it into NumPy arrays.
Visualization: Reshapes and displays a sample image using Matplotlib to verify the data.
Preprocessing:
Converts the label data type to np.uint8 to ensure compatibility.
Splits the dataset into training (60,000 examples) and testing (10,000 examples).
Binary Label Conversion: Creates new label arrays (y_train_5 and y_test_5) where each label is a boolean:
True if the original label is 5.
False otherwise.
Results
The exploratory data analysis in the notebook yielded the following outcomes:

### Data Shape Confirmation:

The full dataset has a shape of (70000, 784), confirming that each image is flattened correctly.
Training and testing splits are correctly sized with 60,000 and 10,000 samples respectively.
Label Transformation:

The conversion of labels from string representations to unsigned 8-bit integers (np.uint8) ensures that numerical operations and comparisons work as expected.
Binary labels (y_train_5 and y_test_5) are successfully created by checking if each label is equal to 5. For example, verifying the first label confirms that the first image represents a 5.
Visualization:

A sample digit is reshaped from a 784-dimensional vector back to a 28x28 image and visualized using Matplotlib.
The successful display of the image confirms that the reshaping and plotting processes are functioning as intended.
