# 🧠 Child Mental Health Prediction using Machine Learning

<p align="center">
  <img src="https://img.shields.io/badge/Machine%20Learning-XGBoost%20%7C%20RandomForest%20%7C%20SVM-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Project-Research%20Based-orange?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Status-Completed-success?style=for-the-badge" />
  <img src="https://img.shields.io/badge/License-MIT-lightgrey?style=for-the-badge" />
</p>

---

# 📌 Project Overview

This project focuses on predicting **mental health conditions in children** using machine learning techniques.  
It includes full pipeline development from **data preprocessing → feature selection → model training → hyperparameter tuning → explainable AI**.

---

# 🎯 Objectives

- Predict child mental health risk (binary classification)
- Identify key influencing factors
- Compare multiple ML models
- Optimize performance using hyperparameter tuning
- Provide interpretable AI explanations

---

# 📂 Dataset Information

### Dataset Size:
- 1,787 samples  
- 9 features  

### Features:

| Feature | Description | Type |
|--------|-------------|------|
| Age | Child age (10–17) | Numerical |
| Gender | Male/Female | Categorical |
| Absence_Days | School absence days | Numerical |
| Substance_Misuse | Substance usage | Binary |
| Parent_MH_Issue | Parental mental health history | Binary |
| Looked_After_Child | Foster/care system | Binary |
| School_Exclusion | Exclusion history | Binary |
| Disability | Disability status | Binary |
| Mental_Health_Problem | Target variable | Binary |

---

# ⚙️ Methodology

## 1️⃣ Data Preprocessing
- Missing value handling  
- Label encoding  
- Feature scaling (StandardScaler)  
- Train-test split (80/20 stratified)  

---

## 2️⃣ Feature Selection

### Methods Used:
- Correlation analysis  
- Feature importance (tree models)  
- SelectKBest  

### Selected Features:
- Substance_Misuse  
- Parent_MH_Issue  
- Looked_After_Child  
- Age  

---

## 3️⃣ Models Used

- Logistic Regression  
- Decision Tree  
- Random Forest  
- SVM  
- Gradient Boosting  
- XGBoost  

---

# 📊 Model Performance Comparison

| Model | Train Accuracy | Test Accuracy | AUC |
|------|----------------|---------------|-----|
| Logistic Regression | 0.8572 | 0.8743 | 0.8239 |
| Decision Tree | 0.9671 | 0.8156 | 0.6228 |
| Random Forest | 0.9671 | 0.8324 | 0.7435 |
| SVM | 0.8740 | 0.8603 | 0.7401 |
| Gradient Boost | 0.8985 | 0.8436 | 0.8088 |
| XGBoost | 0.9510 | 0.8324 | 0.7750 |

---

# 🔥 Full Features vs Reduced Features

| Feature Set | Accuracy | AUC |
|-------------|----------|-----|
| Full Features | 0.8743 | 0.8239 |
| Reduced Features | 0.8547 | 0.8160 |

✔ Reduced feature set maintains strong performance  
✔ Better efficiency with fewer variables  

---

# ⚙️ Hyperparameter Tuning

## 🔹 Random Forest
- max_depth: 20  
- n_estimators: 200  
- max_features: log2  

## 🔹 Gradient Boost
- learning_rate: 0.01  
- n_estimators: 200  
- max_depth: 5  

## 🔹 XGBoost (Best Model)
- learning_rate: 0.05  
- max_depth: 9  
- n_estimators: 200  
- subsample: 1.0  

---

# 🏆 Final Best Model

### ✔ XGBoost (Tuned)

- Accuracy: **84.92%**
- AUC Score: **0.8139**
- Best generalization performance
- Balanced precision & recall

---

# 🔍 Feature Importance

| Rank | Feature | Importance |
|------|--------|------------|
| 1 | Substance_Misuse | 0.4905 |
| 2 | Parent_MH_Issue | 0.3826 |
| 3 | Looked_After_Child | 0.0975 |
| 4 | Age | 0.0294 |

---

# 📊 Visualizations

- Correlation Heatmap  
- Model Accuracy Comparison  
- Confusion Matrix  
- ROC Curve  
- Feature Importance Plot  
- SHAP Summary Plot  
- LIME Explanation  

---

# 🚀 How to Run Project

## 1. Clone Repository
```bash
git clone https://github.com/yourusername/project.git
cd project
