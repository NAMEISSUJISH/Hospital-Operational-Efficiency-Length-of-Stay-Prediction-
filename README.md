# 🏥 Hospital Length of Stay Prediction Using Machine Learning

## 📌 Overview

This project analyzes hospital patient data to identify factors influencing **Length of Stay (LOS)** and develops machine learning models to predict hospitalization duration.

The study was conducted in two phases:

- **Phase I:** Predict LOS using all available patient, laboratory, readmission, and facility information.
- **Phase II:** Predict LOS using only patient health conditions and complications.

The goal is to help healthcare providers improve resource allocation, patient management, and hospital operational efficiency.

---

## 🎯 Project Objectives

### Phase I — Full Feature Analysis
- Predict patient Length of Stay using all available features.
- Compare multiple machine learning models.
- Identify key factors influencing LOS.
- Evaluate model performance using statistical and classification metrics.

### Phase II — Health Conditions Analysis
- Analyze LOS using only patient health conditions.
- Identify conditions associated with longer hospital stays.
- Compare findings against Phase I.
- Understand the impact of clinical conditions on LOS.

---

## 📊 Dataset Information

| Attribute | Value |
|------------|---------|
| Records | 100,000 |
| Features | 28 |
| Target Variable | Length of Stay (LOS) |
| Domain | Healthcare Analytics |

### Data Categories
- Patient Readmission Information
- Medical Conditions
- Laboratory Measurements
- Hospital Facility Information
- Demographic Data

---

## ⚙️ Data Preprocessing

### Data Quality Checks
- Missing Value Analysis
- Data Type Verification
- Target Variable Validation

### Feature Engineering
- Converted date fields into LOS verification
- Encoded categorical variables
- Processed readmission count (`rcount`)
- Applied feature scaling using StandardScaler

### Correlation Analysis
Pearson Correlation was used to understand relationships between features and LOS while retaining all clinically relevant variables.

---

## 🤖 Machine Learning Models

### 1️⃣ Linear Regression
Baseline model used for comparison.

### 2️⃣ Random Forest Regressor
Captures non-linear relationships using ensemble learning.

### 3️⃣ XGBoost Regressor
Gradient boosting model used for high-performance prediction and feature importance analysis.

---

## 📈 Evaluation Metrics

### Regression Metrics
- R² Score
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)

### Classification Metrics
- Confusion Matrix
- Accuracy
- ROC Curve
- AUC Score

---

## 🚀 Results

### Phase I — All Features

| Model | Test R² | Test MAE | Test RMSE |
|---------|---------|---------|---------|
| Linear Regression | 0.77 | 0.87 | 1.14 |
| Random Forest | 0.93 | 0.39 | 0.64 |
| XGBoost | **0.96** | **0.36** | **0.48** |

### 🏆 Best Model
**XGBoost**

Key Findings:
- Explains 96% of LOS variation.
- Lowest prediction error.
- Strong generalization capability.
- Readmission count (`rcount`) is the strongest predictor.

---

### Phase II — Health Conditions Only

| Model | Test R² | Test MAE | Test RMSE |
|---------|---------|---------|---------|
| Linear Regression | 0.18 | 1.76 | 2.12 |
| Random Forest | 0.21 | 1.71 | 2.08 |
| XGBoost | **0.21** | **1.71** | **2.08** |

### 🏆 Best Model
**XGBoost**

Key Findings:
- Health conditions alone explain only 21% of LOS variation.
- Additional factors significantly influence LOS.
- Major psychological disorders and blood-related conditions show the highest impact.

---

## 📌 Feature Importance

### Phase I
Top Contributors:
1. Readmission Count (`rcount`)
2. Facility Type (`facid`)
3. Blood Urea Nitrogen
4. Psychological Disorders
5. Blood Disorders

### Phase II
Top Contributors:
1. Major Psychological Disorder
2. Blood Disorders (`hemo`)
3. Iron Deficiency
4. Psychotherapy Related Conditions
5. Substance Dependence

---

## 📉 Classification Analysis

To provide additional evaluation:

- LOS converted into:
  - **Short Stay**
  - **Long Stay**

### Evaluation Methods
- Confusion Matrix
- ROC Curve
- AUC Score

### Outcome
XGBoost achieved the highest classification performance, confirming its effectiveness in distinguishing short and long hospital stays.

---

## 💡 Business Impact

This project demonstrates how machine learning can:

- Improve hospital resource planning
- Support discharge decision-making
- Identify high-risk patients
- Optimize healthcare operations
- Reduce unnecessary hospitalization costs

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-Learn
- XGBoost
- Jupyter Notebook

---

## 👨‍💻 Author

**Sujish Kumar Indrajith**

MS Applied Computer Science  
Grand Valley State University

---

## 📚 References

- Hospital Length of Stay Dataset
- Scikit-Learn Documentation
- XGBoost Documentation
- Healthcare Analytics Research Papers
- Machine Learning for Healthcare Studies

---
⭐ If you found this project useful, consider giving it a star!
