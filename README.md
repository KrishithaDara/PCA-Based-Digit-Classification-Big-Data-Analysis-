# PCA-Based Digit Classification - Big Data Analysis

**MNIST Digit Classification using PCA and Gaussian Discriminant Analysis**

A Python implementation of handwritten digit classification using Principal Component Analysis (PCA) for dimensionality reduction and Gaussian Discriminant Analysis with full covariance matrices on the MNIST dataset.

## Overview

This project demonstrates dimensionality reduction for digit classification. The implementation uses PCA to reduce 784-dimensional MNIST images to a lower-dimensional space, then applies Gaussian Discriminant Analysis using multivariate normal distributions with full covariance matrices for each digit class.

## Features

* **Dimensionality Reduction**: PCA reduces MNIST images from 784 dimensions to optimal number of components
* **Gaussian Discriminant Analysis**: Classification using multivariate normal distributions with full covariance matrices (not Naive Bayes)
* **Component Optimization**: Tests 2-50 principal components to find optimal dimensionality
* **Visualization**: Scatter plots of first two principal components and accuracy curves
* **High Performance**: Achieves 95.96% accuracy with 42 components

## Requirements

```bash
pip install numpy matplotlib scikit-learn scipy
```

## Dataset

MNIST dataset from OpenML:
* 70,000 grayscale images of handwritten digits (0-9)
* Each image: 28×28 pixels (784 original features)
* Training: 80% (56,000 images)
* Testing: 20% (14,000 images)

## Implementation

### Algorithm Steps

1. **Data Preprocessing**: Normalize pixel values to [0, 1] range using `X = mnist.data / 255.0`
2. **Train-Test Split**: 80-20 split using `train_test_split(test_size=0.2)`
3. **PCA Transformation**: Apply PCA with `n_components` from 2 to 50
4. **Parameter Estimation**: Calculate mean vector and **full covariance matrix** for each of 10 digit classes
5. **Classification**: Maximum likelihood using `multivariate_normal.pdf()` with full covariance
6. **Optimization**: Find best number of components by testing accuracy across range

### Technical Details

**NOT Naive Bayes**: This implementation uses `np.cov(X_train_digit_pca.T)` which creates the full covariance matrix. Naive Bayes would assume feature independence (diagonal covariance only).

**Method**: Gaussian Discriminant Analysis (equivalent to Quadratic Discriminant Analysis in PCA space).

## Usage

```bash
jupyter notebook Big_data_final.ipynb
```

## Results

| Metric | Value |
|--------|-------|
| **Optimal Components** | 42 |
| **Best Accuracy** | **95.96%** |
| **Components Tested** | 2-50 |
| **Dimensionality Reduction** | 784 → 42 (94.6% reduction) |

### Performance Progression (from your output)
- 10 components: 88.69%
- 20 components: 94.46%
- 30 components: 95.61%
- **42 components: 95.96%** (optimal)
- 50 components: 95.82% (slight decline)

## Visualizations

* PCA scatter plot: First two components colored by digit class
* Accuracy curve: Performance vs. number of components (2-50)
