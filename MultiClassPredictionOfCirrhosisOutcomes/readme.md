# Multi-Class Prediction of Cirrhosis Outcomes
* Kaggle Playground Series - Season 3, Episode 26
* https://www.kaggle.com/competitions/playground-series-s3e26/overview
* Objective: Predict probabilities of the Cirrhosis (肝硬化) three outcomes, Status_C, Status_CL, and Status_D (You will find the definition of the above status in dataset description session) 
* Evaluated with multi-class logarithmic loss

# Dataset description
* Use 17 clincial features to predict survival of patient with liver
1. ID (Integer): Unique identifier, no missing values
2. N_Days (Integer): Number of days between registration and the earlier of death, transplanation, or study analysis
3. Drug (Categorical): Type of drug D-penicillamine or placebo
4. Age (Integer): Age (days)
5. Ascites (Categorical): Presence of ascites N (No) or Y (Yes)
6. Hepatomegaly (Categorical): Presence of hepatomegaly N (No) or Y (Yes)
7. Spiders (Categorical): Presence of spiders N (No) or Y (Yes)
8. Edema (Categorical): Presence of edema 
   * N: No edema and no diuretic therapy for edema
   * S: Edema present without diuretics, or edema resolved by diuretics
   * Y: Edema despite diuretic therapy
9. Bilirubin (Continuous): Serum Bilirubin (mg/dl)
10. Cholesterol (Integer): Serum cholesterol (mg/dl)
11. Albumin (Continuous): Albumin (gm/dl)
12. Copper (Integer): Urine copper (ug/day)
13. Alk_Phos (Continuous): Alkaline phosphatase (U/liter)
14. SGOT (Continuous): SGOT (U/ml)
15. Tryglicerides (Integer): Tryglicerides
16. Platelets (Integer): Platelets per cubic (ml/1000)
17. Prothrombin (Continuous): Prothrombin time (s)
18. Stage (Categorical): Histologic stage of disease (1, 2, 3, or 4)
19. Status (Categorical): Status of patients (Target)
    * 0 (D, Death):  The patient did not survived
    * 1 (C, Censored): This means patient still being alive at the time of studying.
    * 2 (CL, Censored to Liver): The patient is censored, but the reason for censorship is specifically due to liver transplantation.

