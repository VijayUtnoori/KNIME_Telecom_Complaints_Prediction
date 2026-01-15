# KNIME_Telecom_Complaints_Prediction
This is Telecom_Complaints_Prediction Project Build on KNIME

📡 KNIME Telecom Complaint Prediction
Overview

This repository contains an end-to-end machine learning workflow built using KNIME Analytics Platform to predict whether a telecom customer is likely to raise a complaint. The project emphasizes leakage-safe preprocessing, class imbalance handling, and robust evaluation using Logistic Regression.

Objective

To develop a binary classification model that predicts customer complaints (Yes / No) based on historical telecom customer behavior, service usage, and subscription details.

Dataset

File: telecom_data_clean.csv

Type: Customer-level tabular dataset

Target Variable:

Original: complaint_flag (Yes / No)

Engineered: complaint_flag_num (1 / 0)

All data leakage–prone columns (IDs, timestamps, complaint-specific fields) are removed prior to modeling to ensure realistic performance.

KNIME Workflow Summary
1. Data Preparation

CSV Reader

Leakage-safe Column Filtering

Target encoding using Rule Engine

Missing value handling (Mean / Most Frequent)

2. Feature Engineering

Domain Calculator for category stability

One-Hot Encoding (One to Many)

Z-score normalization for numeric features

3. Train–Test Split & Class Balancing

Stratified 80/20 split (fixed seed)

SMOTE applied only on training data

Balanced training dataset (50:50)

4. Model Training

Algorithm: Logistic Regression

Regularization: L2 (Ridge / Uniform Gauss)

Iterations: 1000 (for stable convergence)

5. Evaluation

Confusion Matrix

Accuracy, Precision, Recall, F1-score

Cohen’s Kappa

ROC Curve with AUC

Model Performance (Test Data)

Accuracy: 86.7%

Precision (Complaint class): 95.7%

Recall (Complaint class): 88%

F1 Score: 91.7%

AUC: Strong class separability observed

Outputs

The following outputs are exported for reporting and analysis:

knime_predictions.csv

knime_confusion_matrix.csv

knime_model_metrics.csv

Tools & Technologies

KNIME Analytics Platform

Logistic Regression

SMOTE (Class Imbalance Handling)

One-Hot Encoding

Z-score Normalization

Key Takeaways

Preventing data leakage is critical for valid ML models

Class imbalance must be handled carefully (SMOTE on training only)

Regularization improves Logistic Regression stability

KNIME enables clean, production-style ML pipelines without code

Future Enhancements

Feature importance analysis

Hyperparameter optimization

Model comparison (Random Forest, XGBoost)

Deployment via KNIME WebPortal or API

Author

Vijay Utnoori
Machine Learning | Data Analytics | KNIME
