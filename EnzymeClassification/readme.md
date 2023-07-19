# Explore Multi-Label Classification with an Enzyme Substrate Dataset

This project is a part of the season 3 of 2023 edition Kaggle Playground Series. 

[Explore Multi-Label Classification with an Enzyme Substrate Dataset | Kaggle](https://www.kaggle.com/competitions/playground-series-s3e18/overview/description)



## Description

In this competition, our task is to predict EC1, EC2 based on 31 features. The dataset has 6 outputs (EC1-EC6). However, we only have to predict the first two outputs as the competition is required.



## Procedures

1. Data Processing
   * Read the data
   * Checking for null / nan values and duplicates
   * Drop unnecessary features
   * Correlation analysis.
2. Feature Selection
   * Mutual Information.
   * Select the features with the correlation results.
3. Data Preprocessing
   * Split the training features and targets.
   * Data Normalization with Standard Scaler.
   * Split the training dataset and testing dataset.
4. Model Training (Baseline)
   * Decision Tree
   * Logistic Regression
   * Random Forest
   * K-Nearest Neighbor
   * Naive Bayes
   * Gradient Boosting
   * XGboost
   * Adaboost
   * LightGBM
   * Catboost
5. Model Evaluation
   * Area under the ROC Curve
6. Ensemble with soft voting.
7. Generate the submission file and submit to Kaggle.
