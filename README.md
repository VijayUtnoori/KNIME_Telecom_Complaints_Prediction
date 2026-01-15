# KNIME_Telecom_Complaints_Prediction
This is Telecom_Complaints_Prediction Project Build on KNIME

# KNIME Telecom Complaint Prediction

This repository contains a **KNIME Analytics Platform machine learning workflow** for predicting whether a telecom customer is likely to raise a complaint.  
The project demonstrates a complete **end-to-end ML pipeline** built using best practices in KNIME.

---

## 📌 Project Overview

The main objectives of this project are to:

- Load and clean telecom customer data
- Perform leakage-safe preprocessing and feature preparation
- Handle class imbalance using SMOTE
- Train a Logistic Regression classification model
- Evaluate model performance using standard metrics
- Export predictions and evaluation results

This project is designed to showcase how a **structured and production-style ML workflow** can be built visually in KNIME.

---

## 🧠 Workflow Structure

The KNIME workflow is organized into the following logical blocks:

- **Input & Cleaning**
  - CSV Reader
  - Column filtering to remove leakage-prone fields
  - Target conversion (Yes/No → 1/0)

- **Preprocessing**
  - Missing value handling
  - Domain calculation
  - One-hot encoding
  - Z-score normalization

- **Split & Balance**
  - Stratified train-test split (80/20)
  - SMOTE applied only on training data

- **Model Training**
  - Logistic Regression with L2 regularization
  - Stable convergence using higher iterations

- **Evaluation & Export**
  - Confusion matrix and performance metrics
  - ROC curve and AUC
  - CSV export of predictions and results

---

## 📊 Model Performance (Test Data)

- Accuracy: **86.7%**
- Precision (Complaint class): **95.7%**
- Recall (Complaint class): **88%**
- F1 Score: **91.7%**
- ROC-AUC: Strong class separability observed

---

## 📁 Outputs

The workflow generates the following output files:

- `knime_predictions.csv`
- `knime_confusion_matrix.csv`
- `knime_model_metrics.csv`

These outputs can be reused for reporting or dashboarding.

---

## 🛠 Tools Used

- KNIME Analytics Platform
- Logistic Regression
- SMOTE
- One-Hot Encoding
- Z-score Normalization

---

## 👤 Author

**Vijay Utnoori**  
Machine Learning | Data Analytics | KNIME
