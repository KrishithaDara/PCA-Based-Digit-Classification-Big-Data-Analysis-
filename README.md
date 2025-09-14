# PCA-Based Digit Classification - Big Data Analysis

MNIST Digit Classification using PCA and Gaussian Naive Bayes

A Python implementation of handwritten digit classification using Principal Component Analysis (PCA) for dimensionality reduction and Gaussian Naive Bayes for classification on the MNIST dataset.

## Overview

This project demonstrates how dimensionality reduction can be effectively used for digit classification. The implementation uses PCA to reduce the 784-dimensional MNIST images to a lower-dimensional space and then applies Gaussian Naive Bayes classification based on multivariate normal distributions.

## Features

- **Dimensionality Reduction**: Uses PCA to reduce MNIST images from 784 to a configurable number of principal components
- **Gaussian Classification**: Implements classification using multivariate normal distributions for each digit class
- **Hyperparameter Optimization**: Automatically finds the optimal number of principal components
- **Visualization**: Includes scatter plots of the first two principal components and accuracy curves
- **High Performance**: Achieves ~96% accuracy with optimal component selection

## Requirements

```bash
pip install numpy matplotlib scikit-learn scipy
```

## Dataset

The project uses the MNIST dataset from OpenML, which contains:
- 70,000 grayscale images of handwritten digits (0-9)
- Each image is 28×28 pixels (784 features)
- Training set: 56,000 images (80%)
- Test set: 14,000 images (20%)

## Implementation Details

### Algorithm Steps

1. **Data Preprocessing**: Normalize pixel values to [0, 1] range
2. **Train-Test Split**: Split data into 80% training and 20% testing
3. **PCA Transformation**: Apply PCA to reduce dimensionality
4. **Parameter Estimation**: Calculate mean and covariance matrix for each digit class
5. **Classification**: Use maximum likelihood estimation with multivariate normal distributions
6. **Evaluation**: Calculate accuracy and visualize results

## Usage

Open and run the Jupyter notebook:
```bash
jupyter notebook big_data_final.ipynb
```

## Results

| Metric | Value |
|--------|-------|
| **Best Components** | 42 |
| **Best Accuracy** | **95.96%** |
| **Dimensionality Reduction** | 784 → 42 (94.6% reduction) |

### Key Findings
- Shows accuracy curve from 2-50 components
- Includes PCA visualization of digit clusters
- Optimal performance achieved with significant dimensionality reduction

## Visualizations

The project includes:
-  PCA scatter plot of first two components colored by digit
-  Accuracy vs. number of components curve
