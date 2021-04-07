# Eluvio-DS-Challenge
An "open challenge" focusing on NLP with predictive analytics.


## Necessary package installations:
- pandas
- nltk
- sklearn
- collections

## Problem:
- Predict the probability that an event happened in a given year using NLP and machine learning.

## Solution:
- Preprocessing
  - Lemmatization
  - tolower()
  - type conversion
- Vectorization
  - TF-IDF vectorizer
  - y_train doesn't need vectorization (only 8 values in the entire set (2008-2016)
- Logistic Regression
  - Train model using newton-cg (chosen because of runtime, accuracy. Other option were sag/saga b/c of size of dataset)
  - Using source text, predict the probability that the input happened in a given year

## Conclusions:
- From the analysis above, we can make the following insights:
  - 1. Check the probability trends to see when news goes "out of date"
  - 2. Predict societal uptrends and downtrends based on news headlines (market, fads, etc.)
  - 3. Predict the likelihood of an event occuring in a certain year

- Improvements to make:
  - If LR model cannot make a prediction, it seems to assign generic probabilities
    - Possible solutions: 
      - tune hyperparameters of model
      - take a larger subset of the data
      - change ML model (SVM, KNN, or LVQ may work better)
  - Runtime for LR model takes about 10 minutes
    - Possible solutions:
      - tune hyperparameters of model (find a faster optimizer)
      - take a smaller subset of the data


