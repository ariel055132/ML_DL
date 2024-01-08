# Binary Classification with a Bank Churn Dataset
* This project / competition is the first episode of Season 4 Kaggle Playground Series.
[Binary Classification with a Bank Churn Dataset](https://www.kaggle.com/competitions/playground-series-s4e1/overview)
* Objective: Predict whether a customer continues with their account or closes it (Bank churn).
* Evaluation: Area Under the ROC Curve

# Dataset description
1. id: the index of the dataset 
2. Customer ID: Unique identifier for each customer
3. Surname: The customer's surname or last name (String)
4. Credit Score: A numerical value representing the customer's credit score
5. Geography: The country where the customer resides (France / Spain / Germany, String)
6. Gender: The customer's gender (Male / Female, String)
7. Age: The customer's age (Numerical)
8. Tenure: The number of years the customer has been with the bank (Numerical)
9. Balance: The customer's account balance (Numerical)
10. NumOfProducts: The number of bank products the customer uses (Numerical)
11. HasCrCard: Whether the customer has a credit card (1 = yes, 0 = no)
12. IsActiveNumber: Whether the customer is an active member (1 = yes, 0 = no)
13. EstimatedSalary: The estimated salary of the customer
14. Exited: Prediction target, whether the customer has churned (1 = yes, 0 = no)

# Submission and results
1. 20240108_xgb_v1.csv
   * Baseline model with XGBoost.
   * Categorical features are encoded as one-hot encoding.