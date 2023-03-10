# Multi-Label Text Classification With BERT

## Setup

* Environment:Colab
* Dataset:AV-Janatahack-Independence-Day-2020-ML-Hackathon



## Intro

* Topic Modeling for Research Articles
* Given the abstract and title for a set of research articles, predict the topics for each article included in the testing dataset.
* There are 6 topics in the dataset
  1. Computer Science 
  2. Physics
  3. Mathematics
  4. Statistics
  5. Quantitative Biology
  6. Quantitative Finance



## Dataset introduction

* Train.csv has 10 columns
  1. ID (Unique ID for each article)
  2. TITLE (Title of the research article)
  3. ABSTRACT (Abstract of the research article)
  4. Computer Science (Whether article belongs to computer science)
  5. Physics (same as above)
  6. Mathematics (same as above)
  7. Statistics (same as above)
  8. Quantitative Biology (same as above)
  9. Quantitative Finance (same as above)



## Data Preprocessing

* In traditional NLP machine learning problems, we need to clean up the unwanted text. For example, **removing stop words, punctuation, removing symbols and numbers**, to name but a few. (You can do this by using nltk)
* However, it is not necessary to do these preprocessing tasks when you using BERT. It is because BERT uses those sequences and positions of words to understand the intent of user inputs.



## Steps of create a training model with BERT

1. Setup the content that you are going to use in training and testing.
2. Setup the parameters that will be used for model training, such as Max_Len, Training/Valid Batch_Size, Epochs, learning rate, tokenizer.
3. Convert the raw input features to Pytorch Tensors.
4. Split the whole dataset to training dataset and valid dataset.
5. Build a BERT model. Define the layers. Set up loss function and optimizer.
6. (Optional) Create checkpoint which would save the model during training.
7. Start training the model.
8. Evaluate the model performance. You can visualise the model predictions with confusion matrix and classification report.
9. Make predictions with testing dataset.

* You can find the code in Github.

[ML_DL/Classify_BERT_title.ipynb at main · ariel055132/ML_DL (github.com)](https://github.com/ariel055132/ML_DL/blob/main/Multi_Label_Text_Classification/classify_with_BERT/Classify_BERT_title.ipynb)



## Future Work 

1. Learning Rate update automatically.
2. Fine-tuning model hyperparameters.