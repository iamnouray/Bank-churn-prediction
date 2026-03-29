# Customer Churn Prediction

## Project Overview
This project builds a machine learning model to predict whether a bank customer will leave (churn) or stay. The goal is to help banks identify at-risk customers early and take action to improve retention.

---

## Dataset Description
- Source: Kaggle — Bank Customer Churn Dataset  
- Rows: 10,000 customers  
- Features: 11 (after removing ID-related columns)  
- Target: `Exited` (1 = churn, 0 = stay)  
- Churn rate: ~20.4% (imbalanced dataset)  
- No missing values  

---

## Workflow Steps
1. Exploratory Data Analysis (EDA)  
2. Data preprocessing:
   - Dropped irrelevant columns  
   - One-hot encoding for categorical features  
   - Train/test split (80/20)  
   - Feature scaling using StandardScaler  
3. Model training  
4. Model evaluation  
5. Feature importance analysis  

---

## Models Used
- Logistic Regression (baseline)  
- Decision Tree (non-linear model)  
- Random Forest (ensemble model, best performance)  

---

## Evaluation Metrics and Results

| Model | Accuracy | Precision | Recall | F1-score | ROC-AUC |
|------|---------|----------|--------|----------|---------|
| Logistic Regression | 81% | 59% | 19% | 28% | 0.7748 |
| Decision Tree | 86% | 79% | 40% | 53% | 0.8423 |
| Random Forest | 86% | 78% | 46% | 58% | 0.8522 |

- **Best model:** Random Forest (ROC-AUC = 0.8522)

---

## Key Insights
- Age is the strongest predictor of churn  
- Customers aged 40–60 are more likely to leave  
- Customers in Germany show the highest churn rate  
- Inactive customers churn more frequently  
- Customers with high balance and only one product are high risk  

---

## Business Impact / Real-World Use
This model can be used by banks to:

- Identify customers at risk of leaving  
- Target high-risk customers with retention strategies  
- Improve customer retention and reduce losses  
