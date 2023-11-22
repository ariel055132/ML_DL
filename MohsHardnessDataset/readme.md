# Regression with a Mohs Hardness Dataset
* Kaggle Playground Series - Season 3, Episode 25
* https://www.kaggle.com/competitions/playground-series-s3e25/overview
* Objective: Predict the Mohs Hardness of a mineral with given properties.
* Submissions are scored on Median Absolute Error (MedAE)

# What is Mohs Hardness?
* It is a qualitative ordinal scale that characterizes stratch resistance of minerals through ability of harder material to scratch softer material. The scale ranges from 1 to 10, with 1 being the softest and 10 being the hardest. (From Wiki.)
* Diamond is the hardest material, which scores 10. 

# Dataset Features Description
1. id: Unique identifier or index of the row
2. allelectrons_Total: Total number of electrons
3. density_Total: Density 
4. allelectrons_Average: Average number of electrons
5. val_e_Average: Average number of valence electrons
6. atomicweight_Average: Average atomic weight
7. ionenergy_Average: Average ionization energy
8. el_neg_chi_Average: Average electronegativity (on the Pauling scale)
9. R_vdw_element_Average: Average Van der Waals radius
10. R_cov_element_Average: Average covalent radius
11. zaratio_Average: Average ratio between the atomic nucleus and electron cloud
12. density_Average: Average density
13. Hardness: Hardness value. (Prediction Target)

# Result
1. 20231116_BaselinePrediction.csv (Result: 0.61 --> not good)
   * Train the regression model.
   * Finetuned the parameters with RandomizedSearchCV
   * Stacking approach is used in order to obtain a better result.
2. 20231118_BaselinePredictionV2.csv (Result: 0.50 --> Better than first one)
   * Obtain the fine-tuned parameters with Optuna.
   * Compare the performance using stacking and voting. Use voting instead of stacking
3. 20231122_NNPredictionV1.csv (Result: 0.42 --> More Better)
   * Build a six layer neural network to train
   * 32,16,8,4,2,1

# Insights
* Some variables have a high degree of **linear correlation**. It may lower the performance of a model (features are similarly the same in a model perspective). You may delete one of them when training.
* Linear Correlation refers to a linear relationship between two variables, where the change in one variable is directly proportional to the change in another variable. In order words, if one variable increases/decreases, the other variable also increases/decreases in a proportional manner. It is usually represented by a straight line on a scatter plot.
* All the variables are **numerical variables**. Using **neural networks** is a great choice.