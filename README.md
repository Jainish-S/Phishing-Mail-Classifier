# Phishing/Normal Mail Classification

I have got test accuracy of 99.4 using XGBoostClassifier.

## Files

1. eml_to_csv.ipynb
2. preprocessing.ipynb
3. classifier.ipynb

## EML to CSV

I have parsed all the eml files using BytesParser from the built-in email library in python and then stored the following contents to dataset.csv file.

- label (phishing or normal)
- from (sender)
- content_type
- f_path (for debugging)
- subject
- body (attachment)

## Pre-Processing

I have created helper functions to extract urls, emails from the data. Used nltk library to remove stopwords and then did stemming and lemmetization on the text data. Thereafter I did feature extraction and made many possible features and made a correlation map.

## Classifier

I have used XGBoost classifier which works the best for this type of application. I have used TF-IDF to convert text to numerical data and have applied GridSearchCV to improve classification accuracy. I have ploted the evaluation metrics using plotly and seaborn.