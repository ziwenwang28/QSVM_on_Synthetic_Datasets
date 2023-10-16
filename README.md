# SVMs and Quantum Computing Research
I used the code to test for quantum support vector machines on synthetic datasets with various level of  dominance of principal components.

## Introduction

In the realm of machine learning, Support Vector Machines (SVMs) stand as a cornerstone, offering robust solutions for a wide array of applications. The emergence of Quantum Computing heralds a profound transformation for classical SVMs, promising the potential for quantum speedup and unparalleled accuracy, particularly when dealing with high-dimensional and structured datasets, chiefly driven by the quantum kernel evaluation.

## Research Focus

This research project delves into the evaluation of SVM efficiency, with a specific focus on the comparison between quantum and classical approaches, set against synthetic datasets. The emphasis here lies in examining the capabilities of Quantum SVMs, particularly in extreme scenarios, which involve high-dimensional data with minimal discernible patterns.

## Key Findings

The results of this research are intriguing. Quantum SVMs showcase exceptional accuracy, making them a promising tool for tackling complex problems. However, a notable downside emerged - sluggish training times. This discovery holds paramount significance in the contemporary landscape of data proliferation, where higher dimensions and unstructured data are increasingly prevalent.

## Future Prospects

The goal of this work is to contribute to the ongoing pursuit of enhancing Quantum SVMs. The objective is to ensure that their efficiency aligns with their exceptional accuracy, making them not only a powerful tool for today's data-intensive tasks but also a viable solution for the data-rich future that awaits.

This README serves as an introduction to our research, and you can find more details in the accompanying documentation and research paper. We look forward to the potential of Quantum SVMs and their role in shaping the future of machine learning.

# Prerequisites for Running the Code

Before you can run the tested code provided in this repository, it's essential to install the following libraries. We recommend using `pip` to install these dependencies.

## Installation Instructions

```shell
pip install qiskit_machine_learning
pip install qiskit_aer
pip install qiskit

# Synthetic Dataset Generation for Machine Learning

## Dataset Generation Process

This code is responsible for generating a synthetic dataset for use in machine learning experiments. Here's how the dataset is created:

1. **Setting the Random Seed**: The code initiates the random seed to ensure reproducibility using `np.random.seed(0`.

2. **Defining Dataset Parameters**: The number of samples (`num_samples`) and the number of features (`num_features`) are specified to configure the dataset. You have the flexibility to adjust the number of features, allowing you to create datasets of varying dimensions.

3. **Generating Data with Controlled Correlations**: The code generates random data with distinct correlations within the initial features. It sets the mean to zeros and configures the covariance matrix as an identity matrix using `np.eye(num_features)`. Importantly, for the first five features, the code increases the variance, accentuating their significance within the dataset.

4. **Multivariate Normal Distribution**: The dataset is generated using `np.random.multivariate_normal(mean, cov, num_samples)`. In this function, `mean` and `cov` parameters define the mean and covariance matrix for a multivariate normal distribution. This results in a dataset filled with random values while retaining controlled correlations among the initial features.

5. **Splitting into Training and Testing Sets**: The generated dataset is then divided into training and testing sets using the `train_test_split` method. The training set serves as the foundation for training machine learning models, while the testing set is used to assess the models' performance.

6. **Data preprocessing is performed, including standardization using StandardScaler, and principal component analysis (PCA) is applied.

The dataset generation process prepares the data for use in training and evaluating machine learning models, including classical Support Vector Machines (SVMs) and Quantum Support Vector Machines (QSVMs) with various feature maps and optimizers. The code explores different configurations to identify the most effective setup.
