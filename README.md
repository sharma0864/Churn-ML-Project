# Customer Churn Prediction

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## Project Overview
This project predicts customer churn for a telecommunications company using machine learning models.  
The goal is to identify customers likely to leave the company and provide actionable insights for retention strategies.

---

## Dataset
- **Source:** Telco Customer Churn dataset  
- **Description:** Contains information about customer demographics, account info, and usage patterns.  
- **Preprocessing:**  
  - Missing values handled  
  - Categorical variables encoded  
  - Numerical features scaled  

---

## Methodology
1. **Exploratory Data Analysis (EDA)** – Understanding the dataset and identifying key features.  
2. **Feature Engineering** – Created new features like `TotalSpent`, `ServiceCount`, and `ChargesPerTenure`.  
3. **Model Training** – Trained multiple models:
   - Logistic Regression
   - Random Forest
   - XGBoost
   - Voting Classifier (ensemble of above models)
4. **Evaluation** – Metrics used: Accuracy, Precision, Recall, F1-Score, and AUC.  

---

## Results

### ROC Curve
![ROC Curve](README_Assets/Roc-Curve-Comparison.png)

### Feature Importance
![Feature Importance](README_Assets/Feature-importance-XGBoost.png)

**Best Model:** XGBoost  
- High AUC and accuracy  
- Feature importance shows which factors affect churn the most  

---

## Folder Structure

