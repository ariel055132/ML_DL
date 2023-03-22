# Text Classification With TF-IDF

## Setup & introduction

* same as repo Multi-Label Text Classification With BERT



## Data-Checking

1. Checking Label Distribution of 6 topics.

```
Computer Science:  41 (Total: 8594)
Physics:  29 (Total: 6013)
Mathematics:  27 (Total: 5618)
Statistics:  25 (5206)
Quantitative Biology:  3 (587)
Quantiative Finance:  1 (249)
```

2. Checking the text length of title & abstract with distance plot. It shows normal distribution.



## Text Preprocessing

1. Remove accented characters from text with **unidecode**.
2. Convert the char in sentence to lowercase.
3. Remove the stop words with **nltk**.
4. Remove the stemmer in each character.
5. Remove the special characters.



## TF-IDF (Term Frequency-Inverse Document Frequency)

* An algorithm to transform text into a meaningful representation of number which is used to fit machine learning algorithms for prediction
* It is more meaningful than traditional encoding approaches such as one-hot encoding as it can **show the importance of a word to a document** in a collection or corpus.
* Use the tf-idf method in scikit-learn and transform the text into the tf-idf vectors. And then train the model with the new vectors

```python
tfv = TfidfVectorizer(min_df=3,  max_features=None, 
            strip_accents='unicode', analyzer='word',token_pattern=r'\w{1,}',
            ngram_range=(1, 3), use_idf=1,smooth_idf=1,sublinear_tf=1,
            stop_words = 'english')

# Fitting TF-IDF to both training and test sets (semi-supervised learning)
tfv.fit(list(train['cons'].values) + list(test['cons'].values))

#Train
xtrain_tfv = tfv.transform(tr['cons']) 
xvalid_tfv = tfv.transform(ev['cons'])

#Test
xtest_tfv= tfv.transform(test['cons'])
```

