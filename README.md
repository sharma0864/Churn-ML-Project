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

### Model Performance Summary
| Model | Accuracy | AUC | Recall | F1-Score |
| :--- | :--- | :--- | :--- | :--- |
| **XGBoost** | **0.744136** | **0.839979** | **0.791444**|**0.621849** |
| Random Forest | 0.764748	| 0.818987 | 0.641711 |	0.591862 |
| Logistic Reg. | 0.745558	| 0.823453 | 0.713904 |	0.598655 |
| Voting Classifier |	0.762615 | 0.835282 | 0.729947 | 0.620455 |

**Best Model:** **XGBoost** - Rationale: XGBoost offers the highest Recall (identifying 79% of all churners) and the highest AUC. For this project, catching the maximum number of potential churners is the top priority, making XGBoost the most strategic choice, despite Random Forest having the highest overall Accuracy.

### ROC Curve
![ROC Curve](README_Assets/Roc-Curve-Comparison.png)

---

### Feature Importance: Key Drivers of Churn

The XGBoost model's feature importance analysis highlights the most critical factors influencing a customer's likelihood to churn.

![Feature Importance](README_Assets/Feature-importance-XGBoost.png)

**Top 3 Most Important Features:**
1.  **Contract_Two year:** The single strongest predictor. Customers committed to a two-year contract are significantly less likely to churn.
2.  **InternetService_Fiber optic:** This service type is the second most influential factor, indicating that Fiber Optic users are a key segment to monitor.
3.  **Contract_One year & tenure:** The length of commitment and how long a customer has been with the company are also highly critical.

---

## Conclusion and Actionable Insights

The model confirms that **contractual commitment** is the overwhelmingly dominant factor in customer retention.

1.  **Focus on Long-Term Contracts:** The highest priority for retention strategy should be encouraging and incentivizing customers to sign **two-year contracts**.
2.  **Address Fiber Optic Segment:** Further analysis should be performed on **Fiber Optic** customers to understand if their high importance score is due to high loyalty or high frustration (leading to churn).
3.  **Targeted Campaigns:** Develop early-stage retention programs for customers with **low tenure** or those approaching the end of a **one-year contract**.

---

##   Folder Structure
```
.
├── 1_notebooks/           # Jupyter notebooks for EDA, modeling, and analysis
├── README_Assets/         # Images and charts for the README
├── data/                  # Contains the raw and processed datasets
├── .gitignore             # Files/folders to be ignored by Git
├── LICENSE                # The project's license
├── README.md              # The project overview and results (this file)
└── requirements.txt       # Python dependencies for the project
```

## 👨‍💻 Author / Contact

   **Tushar**  
-  Email Id: tusharjan31@gmail.com  
-  GitHub: [sharma0864](https://github.com/sharma0864)  
  
