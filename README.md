# Biomedical Data Science Capstone Project
# Predicting Breast Cancer Diagnosis 
# Dataset: UCI Breast Cancer Wisconsin (Diagnostic) 
# Video: 
# Victoria Li 
10/20/2025

NOTE: The pdf file "CapstoneProject_2" contains the same information as the ipynb file "CapstoneProject" except without the code.

## Project Overview

This project implements 4 machine learning algorithms (Logistic Regression, Random Forest, Neural Networks, and Voting Classifier) to predict breast cancer diagnosis using tumor features given by the Breast Cancer Wisconsin Dataset from UCI Machine Learning Repository. 

## Dataset
**Source:** [UCI Machine Learning Repository - Breast Cancer Wisconsin (Diagnostic)](https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic)

**Description:**
- 569 instances (357 benign, 212 malignant)
- 30 numeric features computed from digitized images of fine needle aspirate (FNA)
- Features describe characteristics of cell nuclei present in the images
- No missing values

**Included Features:**
- Radius, texture, perimeter, area, smoothness
- Compactness, concavity, concave points, symmetry, fractal dimension
- Each feature has three measurements: mean, standard error, and "worst" (largest value)

## Project Structure
- Main Jupyter notebook
- 3-5 page written report without code
- README file (this file) 

## Methodology

### 1. Exploratory Data Analysis
Contains the distribution analysis of target variables, statistical summary of tumor features, correlation analysis among features and resulting diagnoses, visualization of key features 

### 2. Data Preprocessing
Implements an 80-20 train-test split and features are normalized and scaled using StandardScaler

### 3. Machine Learning Models
1. Logistic Regression: a binary classification model that captures linear relationships between features and diagnosis
2. Random Forest Classifier: an ensemble of 100 decision trees that handles non-linear relationships and provides ranking for feature importance to diagnoses
3. Neural Network: a multi-layer model that captures more complex non-linear relationships and prevents overfitting via early stopping 
4. Voting Classifier: an ensemble that combines the strengths and predictions from all three previous models and uses "soft" voting mechanism 

### 4. Model Evaluation
The models are evaluated based on their accuracy, precision, recall, f1-score. Confusion matrices, ROC curves and AUC scores, and feature importance analysis are generated as well.

## Key Findings
All four models demonstrated high performance (>92% accuracy). Characteristics of the cell nucleus are highly predictive of malignancy. Specifically, worst-case features, such as radius, perimeter, and area, show the strongest correlation. The Voting Classifier ensemble method diagnosis accuracy proved to be equal to or higher than that of individual models.

## Clinical Implications
This project demonstrates that machine learning models can help human experts in more efficient and accurate breast cancer diagnoses, which can enable earlier intervention and potentially improve patient outcomes. However, further validation by different datasets and future analysis is needed for clinical deployment. 
