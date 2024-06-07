Duplicate Question Detection Project
Overview
This project aims to detect duplicate questions in a dataset using natural language processing (NLP) and machine learning techniques. The dataset consists of pairs of questions, and the goal is to predict whether the two questions in each pair are duplicates of each other.

Data Preprocessing
Loading and Merging Data: The dataset contains pairs of questions identified by qid1 and qid2. We start by creating a series of all question IDs and count the number of unique and repeating questions.

Preprocessing Questions: The preprocess function is used to clean and standardize the text in the questions. This includes:

Lowercasing the text
Replacing special characters and numbers with their string equivalents
Expanding contractions
Removing HTML tags and punctuations
Feature Engineering
We generate several features to represent the similarity between question pairs:

Basic Features:

Length of questions
Number of words in each question
Number of common words between the two questions
Token Features: Using NLTK stopwords, we extract the following features:

Common non-stopwords ratio (minimum and maximum)
Common stopwords ratio (minimum and maximum)
Common token ratio (minimum and maximum)
Whether the first and last words are the same in both questions
Length-Based Features:

Absolute difference in length between questions
Average token length
Longest common substring ratio
Fuzzy Features: Using fuzzy matching techniques to calculate:

Fuzzy ratio
Partial ratio
Token sort ratio
Token set ratio
Dimensionality Reduction
We use t-SNE to reduce the dimensionality of the feature space for better visualization:

2D and 3D embeddings of the features are plotted using Plotly for visualization.
Model Building
Two machine learning models are used for classification:

Random Forest Classifier
XGBoost Classifier
The dataset is split into training and testing sets, and models are trained and evaluated for accuracy.

Vectorization
We use CountVectorizer to convert the text data into numerical vectors, creating a combined feature set for both questions in each pair.

Model Evaluation
The performance of the models is evaluated using accuracy scores.

Deployment
The trained models and vectorizer are saved using pickle for future use.

Usage
To use the models, load the saved model.pkl, cv.pkl, and stopwords.pkl files and apply them to new question pairs to predict duplicates.

Files
model.pkl: Trained Random Forest model
cv.pkl: CountVectorizer object
stopwords.pkl: List of stopwords used in preprocessing
Conclusion
This project demonstrates an end-to-end pipeline for detecting duplicate questions using a combination of NLP techniques and machine learning models. The detailed preprocessing, feature engineering, and model building steps ensure robust duplicate detection, making it suitable for real-world applications such as question-answering platforms.
