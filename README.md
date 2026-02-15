# Credit Card Fraud Detection

A Machine Learning project focused on detecting fraudulent credit card transactions using imbalanced learning techniques and Logistic Regression.

---

## Project Overview

Credit card fraud detection is a critical real-world problem where fraudulent transactions represent a very small percentage of total transactions.

This project builds a robust fraud detection model using:

- Logistic Regression
- SMOTE (Synthetic Minority Oversampling Technique)
- Stratified Cross-Validation
- ROC-AUC and Precision-Recall evaluation

The primary challenge addressed in this project is **class imbalance**.

---

## Dataset Information

- DatsSet : https://www.kaggle.com/datasets/jacklizhi/creditcard
- Total Transactions: 284,807
- Fraudulent Transactions: 492 (~0.17%)
- Non-Fraud Transactions: ~99.83%

### Features
- V1 – V28 (PCA-transformed features)
- Time
- Amount
- Target: `Class`
  - 0 → Legitimate Transaction
  - 1 → Fraudulent Transaction

> Note: Features were PCA-transformed to protect sensitive financial information.

---

## Problem Statement

Because fraud cases are extremely rare, traditional accuracy metrics are misleading.

This project focuses on:

- Handling class imbalance
- Maximizing fraud detection (Recall)
- Maintaining reasonable Precision
- Optimizing ROC-AUC score

---

## Techniques Used

### 1️.Data Preprocessing
- Feature scaling
- Stratified train-test split

### 2️.Handling Class Imbalance
- Under-Sampling
- SMOTE (Oversampling)

### 3️.Exploratory Data Analysis
- Correlation analysis
- Outlier detection (IQR method)
- PCA & t-SNE visualization

### 4️.Model Training
Models evaluated:
- Logistic Regression
- K-Nearest Neighbors
- Support Vector Machine
- Decision Tree

---

## Final Model

**Best Model:** Logistic Regression   
SMOTE significantly improved generalization performance compared to simple under-sampling.

---

## Evaluation Metrics

Because this is an imbalanced dataset, the following metrics were used:

- ROC-AUC Score
- Precision-Recall Curve
- Confusion Matrix
- Cross-Validation Score

Accuracy was not used as the primary metric.

---

## Key Learnings

- Imbalanced datasets require special handling.
- Accuracy is misleading in fraud detection.
- SMOTE improves model stability and generalization.
- Cross-validation prevents data leakage.
