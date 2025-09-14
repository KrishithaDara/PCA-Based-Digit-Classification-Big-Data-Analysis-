# PCA-Based-Digit-Classification-Big-Data-Analysis-
MNIST Digit Classification using PCA and Gaussian Naive Bayes
A Python implementation of handwritten digit classification using Principal Component Analysis (PCA) for dimensionality reduction and Gaussian Naive Bayes for classification on the MNIST dataset.
1.Overview

This project demonstrates how dimensionality reduction can be effectively used for digit classification. The implementation uses PCA to reduce the 784-dimensional MNIST images to a lower-dimensional space and then applies Gaussian Naive Bayes classification based on multivariate normal distributions.

2.Features

Dimensionality Reduction: Uses PCA to reduce MNIST images from 784 to a configurable number of principal components

Gaussian Classification: Implements classification using multivariate normal distributions for each digit class
Hyperparameter Optimization: Automatically finds the optimal number of principal components
Visualization: Includes scatter plots of the first two principal components and accuracy curves
High Performance: Achieves ~96% accuracy with optimal component selection

3.Requirements
bashpip install numpy matplotlib scikit-learn scipy
Dataset
The project uses the MNIST dataset from OpenML, which contains:

70,000 grayscale images of handwritten digits (0-9)
Each image is 28×28 pixels (784 features)
Training set: 56,000 images (80%)
Test set: 14,000 images (20%)

4.Implementation Details
Algorithm Steps

Data Preprocessing: Normalize pixel values to [0, 1] range
Train-Test Split: Split data into 80% training and 20% testing
PCA Transformation: Apply PCA to reduce dimensionality
Parameter Estimation: Calculate mean and covariance matrix for each digit class
Classification: Use maximum likelihood estimation with multivariate normal distributions
Evaluation: Calculate accuracy and visualize results

Usage
Open and run the Jupyter notebook:
bashjupyter notebook mnist_pca_classification.ipynb
<img width="809" height="231" alt="image" src="https://github.com/user-attachments/assets/a98ab986-52a4-445b-b9c7-d5c5eb6ee508" />

5.Results
Best Components: 42
Best Accuracy: 95.96%
Shows accuracy curve from 2-50 components
Includes PCA visualization of digit clusters
Evaluation: Calculate accuracy and visualize results

