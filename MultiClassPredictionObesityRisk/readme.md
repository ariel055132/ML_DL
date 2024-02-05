# Multi-Class Prediction of Obesity Risk
* Kaggle Playground Series Season 4, Episode 2
* https://www.kaggle.com/competitions/playground-series-s4e2/overview
* Goal: Use various factors to predict obesity risk in individuals
* Submissions are evaluated using the **accuracy** score.
* Dataset: The obesity or CVD risk dataset (https://www.kaggle.com/datasets/aravindpcoder/obesity-or-cvd-risk-classifyregressorcluster)

# Dataset description
* Gender
* Age
* Height
* Weight
* family_history_with_overweight
* FAVC (Frequent consumption of high caloric food)
* FCVC (Frequency of consumption of vegetables)
* NCP (Number of main meals)
* CAEC (Consumption of food between meals)
* SMOKE
* CH20 (Consumption of water daily)
* SCC (Calories consumption monitoring)
* FAF (Physical activity frequency)
* TUE (Time using technology devices)
* CALC (Consumption of alcohol)
* MTRANS (Transportation used)

# Submission
1. 20240201_Baseline_LGB.csv
   * Just train a plain model only
   * 0.89378
2. 20240204_FineTuned_LGBM.csv
   * Train a fine-tuned LightGBM model with optuna 
   * 0.89450
3. 20240205_FineTuned_XGBoost.csv
   * Train a fine-tuned XGBoost model with optuna 
   * 0.91437