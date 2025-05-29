# 🕵️‍♂️ Fraud Detection Model
--------------------------
## 📘 Business Context

This project aims to develop a predictive machine learning model that can identify **fraudulent financial transactions** from a dataset of over 6.3 million entries. The solution involves not just the development of a highly accurate model, but also interpretability, infrastructure-level suggestions, and actionable insights for prevention.

---

## 📊 Dataset Summary
----------------------
- ** Size **: 6,362,620 rows × 10 columns
- ** Target Variable **: `is_fraud` (1 = Fraud, 0 = Not Fraud)
- ** Type **: Numerical and categorical transaction data
- ** Source **: Provided by INSAID
- ** Goal **: Binary classification — fraud vs. non-fraud

---

## ✅ Objectives & Methodology
-------------------------------

### 1. **Data Cleaning**

- **Missing Values**: Handled using median/mode imputation.
- **Outliers**: Identified using IQR and removed to maintain data quality.
- **Multicollinearity**: Checked using **Variance Inflation Factor (VIF)**; redundant features removed.

### 2. **Model Description**
------------------------------
- Algorithms evaluated:
  - **Random Forest Classifier**
  - **XGBoost**
  - **Logistic Regression (baseline)**
- **Handling Imbalance**:
  - Used **SMOTE** (Synthetic Minority Oversampling Technique)
- Final model chosen based on performance and interpretability.

### 3. **Feature Selection**
-----------------------------
- Methods used:
  - Correlation heatmaps
  - Feature importance from Random Forest
  - Recursive Feature Elimination (RFE)
- Selected top predictors significantly contributing to classification.

### 4. **Model Performance**
----------------------------
- Evaluation Metrics:
  - Accuracy
  - **Precision**, **Recall**, **F1-Score**
  - **AUC-ROC**
- Visualization Tools:
  - Confusion matrix
  - ROC Curve
  - SHAP (SHapley Additive exPlanations) values for feature interpretation

### 5. **Key Fraud Predictors**
-------------------------------
- High transaction amount
- Unusual transaction time
- New accounts with little history
- Device ID and IP address changes
- Sudden location shifts

### 6. **Interpretation of Predictors**
----------------------------------------
✅ **Yes, they make sense**:
- Fraudulent activities often involve large or erratic transaction patterns.
- Location, time, and user/device anomalies align with real-world fraud behavior.
- SHAP confirms these as strong drivers of fraud probability.

---

## 🔐 Recommendations for Prevention
-------------------------------------
1. **Real-Time Fraud Scoring** using model predictions
2. **IP and Geo-Location Verification**
3. **Transaction Limits** for new accounts or flagged users
4. **Two-Factor Authentication (2FA)**
5. **Device Fingerprinting**
6. **Behavioral Biometrics** integration

---

## 📈 How to Measure Effectiveness Post-Implementation
-------------------------------------------------------
- Monitor drop in `fraud_rate` over time
- Compare **false positive and false negative rates**
- Evaluate **cost savings** from blocked fraudulent transactions
- Implement **A/B testing**: Compare systems with and without model integration
- KPIs:
  - Detection Rate (TPR)
  - Miss Rate (FNR)
  - Precision
  - ROI from fraud reduction

---

## 🛠 Tools & Libraries
-----------------------------
- **Python 3.x**
- **Pandas, NumPy, Matplotlib, Seaborn**
- **Scikit-learn**
- **Imbalanced-learn (SMOTE)**
- **SHAP, XGBoost**

---

## 📁 Files in the Repository
-------------------------------------
- `Fraud_Detection_Model.ipynb`: Main notebook with code and analysis
- `README.md`: Project overview and documentation

---

## 👨‍💼 Author
--------------
This project was developed as part of an INSAID Data Science case study on fraud detection using machine learning and explainability. All insights and recommendations are based on simulated data and model interpretation.


© INSAID | All rights reserved.
