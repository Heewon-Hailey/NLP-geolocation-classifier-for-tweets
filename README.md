# Geolocation prediction for tweets

## About the project

It is to predict the geolocation (country) where the tweet comes from. It involves two tasks; Task1. preprocessing a collection tweets and Task2. implementing a text classifier.

<br>

## Datasets
A collection of 943 tweets which contains a list of tweets and corresponding country labels is used. The country labels are the standard 2 letter country code [1].

After preprocessing the raw tweets, valid tweets are split into training, development and test datasets with a 70%/15%/15% ratio. They preserve the ratio of the classes for all partitions.

<br>

## Implementation

**Task1. text data processing**<br>
It creates a bag-of-words (BOW) representation for the tweets. Each BOW word goes through the following steps: (1) tokenize (tweet -> word tokens); (2) lowercase; (3) remove any word that does not contain any English alphabets; (4) remove stopwords. After preprocessing, it excludes an empty tweet and return the preprocessed data.


**Task2. text classifiers**<br>
It implements two models; Naive Bayes and Logistic Regression. To compare the two models, it computes accuracy and macro-averaged F-score for each classifier. Additionally, it conducts a further analysis by observing the most important features and their weights for each class for the two classifiers.

**Additional tasks for hashtags**<br>
It tokenizes the collected hashtags by the MaxMatch algorithm to improve the efficiency during word lookups. It contains words including only lemmas. Also, a reversed version of the MaxMatch algorithm is implemented. To compare the two versions of algorithms, a unigram language model computes scores. The unigram model (1) uses the NLTK's Brown corpus (brown_words) for collecting word frequencies; (2) lowercases all words in the corpus; (3) uses add-one smoothing when computing the unigram probabilities; and (4) works in the log space to prevent numerical underflow.

<br>

## Version
Python 3.7.11<br>
Numpy 1.19.5<br>
NLTK 3.6.7<br>

<br>

## Reference

[1] https://www.iban.com/country-codes

<br>

---
:uk: :us: :kr: :jp: :cn: :question:
 
Have fun 😉

