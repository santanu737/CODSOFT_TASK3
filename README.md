# CODSOFT_TASK3
Customer Churn Prediction

# Customer Churn Prediction - CodSoft ML Internship Task 3

My submission for Task 3 of the CodSoft Machine Learning internship.

## What this does

Predicts whether a bank customer is going to leave (churn) or stay, based on stuff like their credit score, age, balance, how many products they use, whether they're an active member, etc.

## Dataset

Bank Customer Churn dataset from Kaggle:
https://www.kaggle.com/datasets/shantanudhakadd/bank-customer-churn-prediction

10,000 bank customers with info like CreditScore, Geography, Gender, Age, Tenure, Balance, NumOfProducts, HasCrCard, IsActiveMember, EstimatedSalary, and the target column Exited (1 = churned, 0 = stayed).

Download the csv from the link above, rename it to `Churn_Modelling.csv` if needed, and put it in this folder before running.

## What I did

- Dropped RowNumber, CustomerId and Surname since they're just identifiers and don't actually help predict anything
- Encoded Geography and Gender (they're text, need to be numbers for the model)
- Scaled all the features
- Tried Logistic Regression, Random Forest, and Gradient Boosting
- Compared them on precision/recall/f1/ROC-AUC since churn isn't as balanced as a 50/50 split (roughly 20% churn rate here)
- Checked feature importance from Random Forest to see what actually drives churn the most (Age and NumOfProducts stood out in my testing)

## Files

- `churn_prediction.py` - main script
- `generate_sample_data.py` - makes fake data to test the code without needing the real dataset first
- `requirements.txt`
## Results

Random Forest and Gradient Boosting both did noticeably better than plain Logistic Regression on this one. Plots get saved as eda_overview.png, model_evaluation.png and feature_importance.png when you run it.

---
Santanu Mondal
B.Tech CSE (AI & ML), Adamas University

Done as part of the CodSoft Machine Learning internship, Sept 2026.
