# Binary Prediction of Smoker Status using Bio-Signals
* Kaggle Playground Series - Season3, Episode 24
* https://www.kaggle.com/competitions/playground-series-s3e24/overview
* Objective: Using binary classification to predict a patient's smoking status from given information about various other health indicators

# Dataset Description (train.csv)
1. id: Unique identifier for each data
2. age: Age of the individual
3. height(cm): Height of the individual in centimeters
4. weight(kg): Weight of the individual in kilograms
5. waist(cm): Waist Circumference length (腰圍長度)
6. eyesight(left): eyesight measurements for the left eyes
7. eyesight(right): eyesight measurements for the right eyes
8. hearing(left): hearing ability for the left ears, represented as binary
9. hearing(right): hearing ability for the right ears
10. systolic: systolic blood pressure (收縮壓，上壓)
11. relaxation: relaxation blood pressure (下壓)
12. fasting blood sugar: fasting blood sugar level
13. Cholesterol: Total cholesterol level (膽固醇)
14. triglyceride: Total triglyceride level (三酸甘油酯)
15. HDL: High-density lipoprotein cholesterol level (好膽固醇)
16. LDL: Low-density lipoprotein cholesterol level (壞膽固醇)
17. hemoglobin: Hemoglobin level in the blood (血紅素)
18. Urine protein: Level of protein in urine, categorized. (尿液中微量蛋白的濃度)
19. Serum creatinine: Serum creatinine level (肌酸酐)
20. AST: glutamic oxaloacetic transaminase type
21. ALT: glutamic oxaloacetic transaminase type
22. GTP: Level of gamma-glutamyl transferase enzyme.
23. dental caries: Presence (1) or absence (0) of dental cavities.
24. smoking: Target variable indicating if the individual is a smoker (1) or not (0).


# NoteBooks
1. smokerStatusBaseline.ipynb
2. smokerStatusBaselineEnsemble.ipynb
   * Result with RandomForestClassifier

# Ranking
* Top 15-20%