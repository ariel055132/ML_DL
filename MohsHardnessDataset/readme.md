# Regression with a Mohs Hardness Dataset
* Kaggle Playground Series - Season 3, Episode 25
* https://www.kaggle.com/competitions/playground-series-s3e25/overview
* Objective: Predict the Mohs Hardness of a mineral with given properties.
* Submissions are scored on Median Absolute Error (MedAE)

# What is Mohs Hardness?
* It is a qualitative ordinal scale that characterizes stratch resistance of minerals through ability of harder material to scratch softer material. The scale ranges from 1 to 10, with 1 being the softest and 10 being the hardest. (From Wiki.)
* Diamond is the hardest material, which scores 10. 

# Result
1. 20231116_XXX.csv (Result: 0.61 --> not good)
2. 20231118_XXX.csv (Result: )

# Insights
* Some variables have a high degree of linear correlation. It may lower the performance of a model (features are similarly the same in a model perspective).
* Linear Correlation refers to a linear relationship between two variables, where the change in one variable is directly proportional to the change in another variable. In order words, if one variable increases/decreases, the other variable also increases/decreases in a proportional manner. It is usually represented by a straight line on a scatter plot.
* All the variables are numerical variables. Using neural networks is a great choice.