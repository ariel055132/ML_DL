# Multi-Class Prediction of Obesity Risk
* Kaggle Playground Series Season 4, Episode 2
* https://www.kaggle.com/competitions/playground-series-s4e2/overview
* Goal: Use various factors to predict obesity risk in individuals
* Submissions are evaluated using the **accuracy** score.
* Dataset: The obesity or CVD risk dataset (https://www.kaggle.com/datasets/aravindpcoder/obesity-or-cvd-risk-classifyregressorcluster)

# Dataset description (Training dataset)
1. Gender
   * Female (10422, 50.2%)
   * Male (10336, 49.8%)
   * Gender distribution is fairly equal in training dataset
2. Age
3. Height
4. Weight
5. family_history_with_overweight
   * yes (17014, 82.0%)
   * no (3744, 18.0%)
   * Most people (82%) have a family history with overweight
   * Insight: It should be an important features.
6. FAVC (Frequent consumption of high caloric food)
   * yes (18982, 91.4%)
   * no  (1776, 8.6%)
   * Most people (91.4%) frequently consume high caloric food
   * Insight: It should be an important features.
7. FCVC (Frequency of consumption of vegetables)
8. NCP (Number of main meals)
9. CAEC (Consumption of food between meals)
   * Sometimes (17529, 84.4%)
   * Frequently (2472, 11.9%)
   * Always (478, 2.3%)
   * no (279, 1.3%)  
   * Most people (84.4%) consume food between meals
   * Insight: It should be an important features.
10. SMOKE
   * no (20513, 98.8%)
   * yes (245, 1.2%)
   * Almost all people (98.8%) are non-smokers
11. CH20 (Consumption of water daily)
12. SCC (Calories consumption monitoring)
    * no (20071, 96.7%)
    * yes (687, 3.3%)
    * Almost all people (96.7$) does not bother calories when they are eating.
    * Insight: It should be important features
13. FAF (Physical activity frequency)
14. TUE (Time using technology devices)
15. CALC (Consumption of alcohol)
    * Sometimes (15066, 72.6%)
    * no (5163, 24.9%)
    * Frequently (529, 2.5%)
16. MTRANS (Transportation used)
    * Public Transportation (16687, 80.4%)
    * Automobile (3534, 17.0%)
    * Walking (467)
    * Motorbike (38)
    * Bike (32)
    * Most of the people use some form of vehicle while only a few people prefers walking or using bike.
    * Insight: It should be important features
17. NObeyesdad (Prediction Target)
   * Obesity_Type_III   (4046, 19.5%)   (324)
   * Obesity_Type_II    (3248, 15.6%)   (297)
   * Normal_Weight     （3082, 14.8%)    (287)
   * Obesity_Type_I       (2910, 14.0%) (351)
   * Insufficient_Weight （2523, 12.2%)  (272)
   * Overweight_Level_II  (2522, 12.1%)  (290)
   * Overweight_Level_I   （2427, 11.7%) (290)
   * In training dataset, we have the highest number of people with Obesity_Type_III, having share of 19.5%
* Noted: Outliers are found in Age feature only. Most of the people are aged between 20-30.
* In correlation analysis, we can found that:
   * Height and Weight exhibit a moderate positive correlation of 0.42, other variables are CH20 and weight, FAF and weight
   * Age shows negative correlations with physical activity frequency (FAF, -0.19), and time using technology device (TUE, -0.30)

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
4. 20240206_FineTuned_LGBM.csv
   * 0.91473
5. 20240206_FineTuned_LGBM_Others.csv
   * Using hyperparameters from https://www.kaggle.com/code/divyam6969/beginners-easy-obesity-risk-lgsm-tuning/notebook
   * 0.91943
6. 20240208_Baseline_Catboost_submission.csv
   * Train a baseline model with Catboost.
   * One-Hot encoding the categorical variables
   * 0.90968