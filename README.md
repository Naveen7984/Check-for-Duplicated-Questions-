Duplicate Question Detection Project:
This project aims to detect duplicate questions in a dataset using natural language processing (NLP) and machine learning techniques. The dataset consists of pairs of questions, and the goal is to predict whether the two questions in each pair are duplicates of each other.

Features:
Data Preprocessing: Standardizing text by lowercasing, replacing special characters, expanding contractions, and removing HTML tags and punctuations.
Feature Engineering: Generating basic features, token features using NLTK stopwords, length-based features, and fuzzy matching features to represent the similarity between question pairs.
Dimensionality Reduction: Using t-SNE to reduce the dimensionality of the feature space for better visualization.
Model Building: Training and evaluating Random Forest and XGBoost classifiers for duplicate question detection.
Vectorization: Converting text data into numerical vectors using CountVectorizer.

Deployment:
A web application has been built using Streamlit to interact with the trained model. Users can input question pairs and get predictions on whether they are duplicates.

Files:
model.pkl: Trained Random Forest model
cv.pkl: CountVectorizer object
stopwords.pkl: List of stopwords used in preprocessing

This project demonstrates an end-to-end pipeline for detecting duplicate questions, from data preprocessing and feature engineering to model training and deployment using Streamlit.
