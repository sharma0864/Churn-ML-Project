# Customer Churn Prediction

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## Project Overview
This project predicts customer churn for a telecommunications company using machine learning models. The goal is to identify customers likely to leave the company and provide actionable insights for retention strategies.

## Dataset
- **Source:** Telco Customer Churn dataset  
- **Description:** Contains information about customer demographics, account info, and usage patterns.  
- **Preprocessing:**  
  - Handled missing values  
  - Encoded categorical variables  
  - Scaled numerical features  

## Methodology
1. **Exploratory Data Analysis (EDA)**, Understanding the dataset and identifying key features.  
2. **Feature Engineering**, Created new features like `TotalSpent`, `ServiceCount`, and `ChargesPerTenure`.  
3. **Model Training**, Trained multiple models:
   - Logistic Regression
   - Random Forest
   - XGBoost
   - Voting Classifier (ensemble of the above models)
4. **Evaluation**, Metrics used: Accuracy, Precision, Recall, F1-Score, and AUC.  

## Results

### Model Performance Summary
| Model | Accuracy | AUC | Recall | F1-Score |
| :--- | :--- | :--- | :--- | :--- |
| **XGBoost** | **0.744136** | **0.839979** | **0.791444** | **0.621849** |
| Random Forest | 0.764748 | 0.818987 | 0.641711 | 0.591862 |
| Logistic Reg. | 0.745558 | 0.823453 | 0.713904 | 0.598655 |
| Voting Classifier | 0.762615 | 0.835282 | 0.729947 | 0.620455 |

**Best Model:** **XGBoost** - Rationale: XGBoost has the highest Recall, identifying 79% of all churners and the highest AUC. For this project, catching as many potential churners as possible is the top priority. This makes XGBoost the best choice, even though Random Forest has the highest overall Accuracy.

### ROC Curve
![ROC Curve](README_Assets/Roc-Curve-Comparison.png)

### Feature Importance: Key Drivers of Churn

The feature importance analysis from the XGBoost model highlights the most important factors affecting a customer's likelihood to churn.

![Feature Importance](README_Assets/Feature-importance-XGBoost.png)

**Top 3 Most Important Features:**
1. **Contract_Two year:** This is the strongest predictor. Customers with a two-year contract are much less likely to churn.
2. **InternetService_Fiber optic:** This service type is the second most important factor, showing that Fiber Optic users are a critical group to watch.
3. **Contract_One year & tenure:** The length of commitment and how long a customer has been with the company are also very important.

## Conclusion and Actionable Insights

The model shows that **contractual commitment** is the most significant factor in customer retention.

1. **Focus on Long-Term Contracts:** The main priority for retention should be to encourage customers to sign **two-year contracts** with incentives.
2. **Address Fiber Optic Segment:** Conduct further analysis on **Fiber Optic** customers to see if their high importance score is due to loyalty or frustration leading to churn.
3. **Targeted Campaigns:** Create early-stage retention programs for customers with **low tenure** or those nearing the end of a **one-year contract**.

## Folder Structure
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

## Author / Contact

   **Tushar**  
-  Email: tusharjan31@gmail.com  
-  GitHub: [sharma0864](https://github.com/sharma0864)  
  
