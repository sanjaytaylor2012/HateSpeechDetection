# HateSpeechDetection


## Table of Contents
- [Inspiration](#inspiration)
- [How I built it](#how-i-built-it)
- [Challenges](#challenges)
- [Dataset](#dataset)

---

## Inspiration
In the current day, social media such as Instagram, Twitter, and Youtube has the potential to be a great space where people share ideas and spread joy. However, it can also be a place of toxicity and hate. With bilions of users, it is impossible to catch every instance of hate speech. However, machine learning algorithms can be used to detect hate speech using Natural Language Processing in order to flag a message as hate speech and remove it from the platform.

## Concept
The concept for my algorithm is to take in text data from a dataset with information such as user demographics, their message, and whether or not their message was considered to be hate speech. The data was taken from the comment section of the site Youtube. Then the model would train itself based on this data and be able to detect if new comments are hate speech or not.


## How I built it

I built this using a Jupyter Notebook and libraries such as the Natural Learning Toolkit (NLTK) library, pandas, regular expressions (re), Sci-kit Learn, and the string library. First, I added punctation percentages as well as text length as features to the model along with the demographics that came with the dataset. This includes the messages themselves, number of comments the user left, number of subscribers they have, number of videos they have uploaded, whether they have profanity in their username, and their age. I then performed feature analysis for the model using numpy histograms for a visual representation of how each feature that I created or used would affect the model. 

<p align="center">
  <img width="460" height="300" src="https://github.com/sanjaytaylor2012/HateSpeechDetection/blob/main/Screenshot%202022-11-16%20142614.png">
</p>
Blue corresponds to hate speech comments

Orange corresponds to non-hate speech comments

X-axis is characters per message

This histogram shows that longer messages are more likely to be hate speech and shorter messages are less likely to be hate speech. This is one of the feature that helps the model differenciate between hate speech and non hate speech.

<p align="center">
  <img width="460" height="300" src="https://github.com/sanjaytaylor2012/HateSpeechDetection/blob/main/Screenshot%202022-11-16%20142658.png">
</p>
Blue corresponds to hate speech comments

Orange corresponds to non-hate speech comments

X-axis is number of comments left by a user

This histogram shows that the users that write hateful comments tend to also write MORE comments. This is one of the feature that helps the model differenciate between hate speech and non hate speech.

Then I tested a Count vectorizer and a TFIDF vectorizer with using Grid Search to determine the most effective and effiecient vectorizer when applied to a Random Forest Classifier. Then, I optimized both a Random Forest Classifier as well as Gradient Boosting through testing with 5-fold cross validation, TFIDF vectorizer and various parameter settings until I found the most optimal settings for each algorithm. Finally, I pitted the two algorithms against each other and determined that the Gradient Boosting Classifier was the better algorithm in terms of speed, accuracy, and precision.  

## Challenges
The biggest challange I faced was understanding the how pandas DataFrames fit into the models. Getting the classifiers to fit each of the dataframes as well as formatting them correctly required a deep understanding of of dataframes.

## Team
Antonio Villarreal - https://www.linkedin.com/in/antoniovillarreal2024/  
Sanjay Taylor - https://www.linkedin.com/in/sanjaytaylor/  
Vincent Lin - https://www.linkedin.com/in/vincent-lin-uf/  
Michael Logsdon - https://www.linkedin.com/in/michaellogsdon1/  
Walid Barazenji - https://www.linkedin.com/in/walid-barazenji/  



## Dataset
Dataset on Kaggle: https://www.kaggle.com/datasets/saurabhshahane/cyberbullying-dataset?select=youtube_parsed_dataset.csv
