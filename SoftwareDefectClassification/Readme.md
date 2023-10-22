# Binary Classification with a software defects dataset

* This is one of the competition in Kaggle Playground.
* This readme is similar to writeup.

## Introduction

* Objective of this problem
  * Predict whether a C program has any defects or not with the given various attributes about the code
* Evaluation metrics
  * Area Under the ROC Curve

## Procedures

1. Reading data files
   * Using **pd.read_csv()** to import the training dataset (train_df), and testing dataset (test_df)
   * Check the dimension of the datasets with **shape**
   * Obtain the basic statistical details (mean, std, etc) of dataset with **describe()**
   * Obtain the column names and not-null values with **info()**
   * Checking whether missing values (NaN) and duplicated values are exist in dataset with **isna().sum()**
2. Data Exploration
   * Using **pie chart** to check the distribution of target (has defects / does not have defects)
   * Using **heat map** to show the results of correlation analysis of features.
3. Modeling with ensemble
   * Training with 6 models with 25 fold validation.
   * Ensemble
     * Combine the results from 6 models by **average** to get a final result
     * Should not use average in classification tasks. (Picking the majority class is preferred)





## Reference

* Competition Website
  * [Binary Classification with a Software Defects Dataset | Kaggle](https://www.kaggle.com/competitions/playground-series-s3e23/data)
* Description of the original Website
  * [Software Defect Prediction (kaggle.com)](https://www.kaggle.com/datasets/semustafacevik/software-defect-prediction)

* Cite
  * Walter Reade, Ashley Chow. (2023). Binary Classification with a Software Defects Dataset. Kaggle. https://kaggle.com/competitions/playground-series-s3e23