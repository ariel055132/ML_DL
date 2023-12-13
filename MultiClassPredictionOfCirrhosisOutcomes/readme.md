# Multi-Class Prediction of Cirrhosis Outcomes
* Kaggle Playground Series - Season 3, Episode 26
* https://www.kaggle.com/competitions/playground-series-s3e26/overview
* Objective: Predict probabilities of the Cirrhosis (肝硬化) three outcomes, Status_C, Status_CL, and Status_D (You will find the definition of the above status in dataset description session) 
* Evaluated with multi-class logarithmic loss

# Dataset description
* Use 17 clincial features to predict survival of patient with liver
1. ID (Integer): Unique identifier, no missing values
2. N_Days (Integer): Number of days between registration and the earlier of death, transplanation, or study analysis
3. Drug (Categorical): 
* Status_D (0) = Death, Status_C (1) = Censored, Status_CL (2) = Censored due to liver transplanation
  * D: The patient did not survived
  * C: This means patient still being alive at the time of studying.
  * CL: The patient is censored, but the reason for censorship is specifically due to liver transplantation.

