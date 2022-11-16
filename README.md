# HateSpeechDetection


## Table of Contents
- [Inspiration](#inspiration)
- [How I built it](#how-we-built-it)
- [Challenges](#challenges)
- [Dataset](#dataset)

---

## Inspiration
In the current day, social media such as Instagram, Twitter, and Youtube has the potential to be a great space where people share ideas and spread joy. However, it can also be a place of toxicity and hate. With bilions of users, it is impossible to catch every instance of hate speech. However, machine learning algorithms can be used to detect hate speech using Natural Language Processing in order to flag a message as hate speech and remove it from the platform.

## Concept
The concept for my algorithm is to take in text data from a dataset with information such as user demographics, their message, and whether or not their message was considered to be hate speech. The data was taken from the comment section of the site Youtube. Then the model would train itself based on this data and be able to detect if new comments are hate speech or not.


<p align="center">
  <img width="460" height="300" src="https://github.com/Antonio-Villarreal/Dyscovery/blob/main/Images/Game1.png">
</p>

## How I built it

I built this using a Jupyter Notebook and libraries such as the Natural Learning Toolkit (NLTK) library, pandas, regular expressions (re), Sci-kit Learn, and the string library. First, I performed feature analysis for the model using numpy histograms for a visual representation of how each feature that I created or used would affect the model. I then added punctation percentages as well as text length as features to the model along with the demographics that came with the dataset. Then I tested a Count vectorizer and a TFIDF vectorizer with using Grid Search to determine the most effective and effiecient vectorizer whem applied to a Random Forest Classifier. Then, I optimized both a Random Forest Classifier as well as Gradient Boosting through testing with 5-fold cross validation, TFIDF vectorizer and various parameter settings until I found the most optimal settings for each algorithm. Finally, I pitted the two algorithms against each other and determined that the Gradient Boosting Classifier was the better algorithm in terms of speed, accuracy, and precision.  

## Challenges
The biggest challange I faced was understanding the how pandas DataFrames fit into the models. Getting the classifiers to fit each of the dataframes as well as formatting them correctly required a deep understanding of of dataframes.

## Team
Antonio Villarreal - https://www.linkedin.com/in/antoniovillarreal2024/  
Sanjay Taylor - https://www.linkedin.com/in/sanjaytaylor/  
Vincent Lin - https://www.linkedin.com/in/vincent-lin-uf/  
Michael Logsdon - https://www.linkedin.com/in/michaellogsdon1/  
Walid Barazenji - https://www.linkedin.com/in/walid-barazenji/  

<p align="center">
  <img width="460" height="300" src="https://github.com/Antonio-Villarreal/Dyscovery/blob/main/Images/Team.jpg">
</p>

## Dataset
Dataset on Kaggle: https://www.kaggle.com/datasets/saurabhshahane/cyberbullying-dataset?select=youtube_parsed_dataset.csv
