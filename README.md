# KNIME_Telecom_Complaints_Prediction
This is Telecom_Complaints_Prediction Project Build on KNIME

📡 KNIME Telecom Complaint Prediction
📌 Project Overview

This project implements an end-to-end machine learning pipeline in KNIME Analytics Platform to predict whether a telecom customer is likely to raise a complaint. The solution focuses on leakage-safe preprocessing, class imbalance handling, and robust model evaluation using Logistic Regression.

🎯 Objective

To build a binary classification model that predicts customer complaints (Yes / No) using historical telecom customer behavior, service usage, and plan-related features.

🗂 Dataset Information

Dataset: telecom_data_clean.csv

Type: Customer-level tabular data

Target Variable:

Original: complaint_flag (Yes / No)

Engineered: complaint_flag_num (1 / 0)

The dataset is pre-cleaned, and all data leakage–prone columns (IDs, timestamps, complaint details) are removed before model training 

Knime_ML_Project

.

🧠 Machine Learning Workflow (KNIME)
1️⃣ Data Loading & Leakage-Safe Feature Selection

CSV Reader

Column Filter (removes identifiers, timestamps, leakage columns)

Rule Engine (target conversion Yes/No → 1/0)

Value Counter (class distribution validation)

2️⃣ Data Preprocessing

Missing Value Handling (Mean / Most Frequent)

Domain Calculator (ensures stable categorical domains)

One-Hot Encoding (One to Many)

Feature Scaling using Z-score Normalization

Validation using Statistics & Value Counter

3️⃣ Train-Test Split & Class Imbalance Handling

Stratified Train-Test Split (80/20, seed = 42)

SMOTE applied only on training data

Balanced training set (50:50 class distribution)

4️⃣ Model Training

Algorithm: Logistic Regression

Regularization: L2 (Ridge / Uniform Gauss)

Epochs: 1000 (to handle convergence issues)

Trained on SMOTE-balanced dataset

5️⃣ Prediction & Evaluation

Logistic Regression Predictor

Scorer node for evaluation:

Confusion Matrix

Accuracy, Precision, Recall, F1-score

Cohen’s Kappa

ROC Curve with AUC visualization

📊 Model Performance (Test Data)

Accuracy: 86.7%

Precision (Complaint class): 95.7%

Recall (Complaint class): 88%

F1 Score: 91.7%

AUC: High separability observed in ROC curve

📁 Outputs & Deliverables

The following outputs are exported as CSV files:

knime_predictions.csv

knime_confusion_matrix.csv

knime_model_metrics.csv

These files can be reused for reporting or dashboarding.

🛠 Tools & Technologies

KNIME Analytics Platform

Logistic Regression (Classification)

SMOTE (Class Imbalance Handling)

One-Hot Encoding

Z-score Normalization

✅ Key Learnings

Importance of data leakage prevention

Handling imbalanced datasets correctly

Why SMOTE must be applied only on training data

Role of regularization in Logistic Regression

Building production-ready ML workflows in KNIME

🚀 Future Improvements

Feature importance analysis using coefficients

Hyperparameter optimization loop

Model comparison with Random Forest / XGBoost

Deployment using KNIME WebPortal or API

👤 Author

Vijay Utnoori
(Machine Learning | Data Analytics | KNIME)
