# Multi-Class Prediction of Cirrhosis Outcomes
* Kaggle Playground Series - Season 3, Episode 26
* https://www.kaggle.com/competitions/playground-series-s3e26/overview
* Objective: Predict probabilities of the Cirrhosis (肝硬化) three outcomes, Status_C, Status_CL, and Status_D (You will find the definition of the above status in dataset description session) 
* Evaluated with multi-class logarithmic loss

# Dataset description and insights
* Use 17 clincial features to predict survival of patient with liver
1. ID (Integer): Unique identifier
2. N_Days (Integer): 
   * Number of days between registration and the earlier of death, transplanation, or study analysis time in July 1986
3. Drug (Categorical): 
   * Type of drug D-penicillamine or placebo
   * Type of medication may impact the effectiveness of treatment, thus affecting status
4. Age (Integer): Age (days)
   * Age could be related to disease progression
   * Older patients may have different status trajectory.
5. Sex (Categorical): Sex, M (Male) or F (Female) 
   * Biological Sex may influence disease patterns and response to the treatment, thus affecting status.
6. Ascites (Categorical): Presence of ascites, N (No) or Y (Yes)
   * The accumulation of fluid in the abdomen, offen a sign of advanced liver disease, which could indicate a poorer status.
7. Hepatomegaly (Categorical): Presence of hepatomegaly N (No) or Y (Yes)
   * Enlargement of the liver. If present, it might suggest more serious liver disease and potentially a poorer status
8. Spiders (Categorical): Presence of spiders, N (No) or Y (Yes)
   * Spider angiomas are small, spider-like capiliaries visible under the skin, associated with liver disease 
9.  Edema (Categorical): Presence of edema 
   * N: No edema and no diuretic therapy for edema
   * S: Edema present without diuretics, or edema resolved by diuretics
   * Y: Edema despite diuretic therapy
   * Swelling caused by excess fluid trapped in the body's tissues, often worsening the prognosis and indicating poorer status.
10. Bilirubin (Continuous): Serum Bilirubin (mg/dl)
    * High levels can indicate liver dysfunction and may correlate with more advanced disease and poorer status.
11. Cholesterol (Integer): Serum cholesterol (mg/dl)
    * Although it does not directly related to liver function, abnormal levels can be associated with certain liver conditions and overall health status.
12. Albumin (Continuous): Albumin (gm/dl)
    * Low levels can be a sign of liver disease and can indicate a poorer status due to the liver's reduced ability to synthesize proteins.
13. Copper (Integer): Urine copper (ug/day)
    * Elevated in certain liver diseases, and could affect status if levels are abnormally high.
14. Alk_Phos (Continuous): Alkaline phosphatase (U/liter)
    * An enzyme that, when elevated, can indicate liver damage and could correlate with a worsening status.
15. SGOT (Continuous): SGOT (U/ml)
    * An enzyme that can indicate liver damage and could correlate with a worsening status.
16. Tryglicerides (Integer): Tryglicerides
    * Though mainly a cardiovascular risk indicator, they can be affected by liver function / the status of the patient
17. Platelets (Integer): Platelets per cubic (ml/1000)
    * Lower platelets count can be a result of advanced liver disease and can indicate a poorer status.
18. Prothrombin (Continuous): Prothrombin time (s)
    * A measure of how long it takes blood to clot. Liver disease can cause increased times, indicating poorer status.
19. Stage (Categorical): Histologic stage of disease (1, 2, 3, or 4)
    * The stage of liver disease, which directly correlates with the patient's status - the higher the stage, the more serious the condition
20. Status (Categorical): Status of patients (Target)
    * 0 (D, Death):  The patient did not survived
    * 1 (C, Censored): This means patient still being alive at the time of studying.
    * 2 (CL, Censored to Liver): The patient is censored, but the reason for censorship is specifically due to liver transplantation.

# Result
1. Version1/20231216_CirrhosisOutcomeBaselinePrediction_V1.csv (0.41506)
   * Train baseline model with LGBMClassifier, Gradient Boosting, and Catboost.
   * Use ensemble to obtain more accurate result.

# Ranking 
* private: 63/1661

