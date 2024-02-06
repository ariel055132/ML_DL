# Multi-Class Prediction of Obesity Risk
* Kaggle Playground Series Season 4, Episode 2
* https://www.kaggle.com/competitions/playground-series-s4e2/overview
* Goal: Use various factors to predict obesity risk in individuals
* Submissions are evaluated using the **accuracy** score.
* Dataset: The obesity or CVD risk dataset (https://www.kaggle.com/datasets/aravindpcoder/obesity-or-cvd-risk-classifyregressorcluster)

# Dataset description
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
6. FAVC (Frequent consumption of high caloric food)
   * yes (18982, 91.4%)
   * no  (1776, 8.6%)
   * Most people (91.4%) frequently consume high caloric food
7. FCVC (Frequency of consumption of vegetables)
8. NCP (Number of main meals)
9. CAEC (Consumption of food between meals)
   * Sometimes (17529, 84.4%)
   * Frequently (2472, 11.9%)
   * Always (478, 2.3%)
   * no (279, 1.3%)  
   * Most people (84.4%) consume food between meals
10. SMOKE
   * no (20513, 98.8%)
   * yes (245, 1.2%)
11. CH20 (Consumption of water daily)
12. SCC (Calories consumption monitoring)
13. FAF (Physical activity frequency)
14. TUE (Time using technology devices)
15. CALC (Consumption of alcohol)
16. MTRANS (Transportation used)
17. NObeyesdad (Prediction Target)
   * Obesity_Type_III   (4046, 19.5%)   (324)
   * Obesity_Type_II    (3248, 15.6%)   (297)
   * Normal_Weight     （3082, 14.8%)    (287)
   * Obesity_Type_I       (2910, 14.0%) (351)
   * Insufficient_Weight （2523, 12.2%)  (272)
   * Overweight_Level_II  (2522, 12.1%)  (290)
   * Overweight_Level_I   （2427, 11.7%) (290)
   * In training dataset, we have the highest number of people with Obesity_Type_III, having share of 19.5%

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