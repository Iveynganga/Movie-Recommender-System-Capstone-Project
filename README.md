# Movie-Recommender-System-Capstone-Project

# What is a recommender system?
A recommender system is a type of information filtering system that provides personalized suggestions to users based on their preferences and behaviors. These systems are widely used to help users navigate through large amounts of data and find items that are most relevant to them. Recommender systems can be used in various sectors including:

  ## 1. E-commerce
These systems suggest products to customers based on their browsing history and past purchases. A good example is Amazon.

# 2. Streaming Services
The systems recommend movies, TV shows, or music based on user preferences (e.g., Netflix, Spotify).

# 3. Social Media
The systems curate content feeds and suggest friends or groups (e.g., Facebook, Instagram)

# 4. Online Advertising
The systems display targeted ads based on user behavior and interests (e.g., Google Ads)

# 5. News Websites
The system recommends articles that match user interests (e.g., personalized news feeds)

# 6. Academic Research
Suggests relevant research papers and collaborators (e.g., Google Scholar) 

# Project Overview
This project aims to develop a personalized movie recommender system. The system leverages collaborative filtering techniques to provide movie suggestions tailored to individual user preferences and historical interactions. By analyzing user ratings and movie data, the recommender system can predict and suggest movies that users are likely to enjoy.
Collaborative filtering is a technique used in movie recommender systems to suggest films to users based on the preferences and behaviors of similar users. 

# Problem Statement
With an ever-growing library of movies available on various platforms, users often struggle to find content that matches their tastes. This project addresses the challenge by creating a personalized movie recommendation system. The goal is to enhance user experience by suggesting movies that they are likely to find appealing based on their past viewing history and the preferences of similar users.

# What is Cosine Similarity?
Cosine similarity is a metric used to measure the similarity between two vectors by calculating the cosine of the angle between them. 
In this movie recommender system project, each movie can be represented as a vector of features, such as genres, actors, directors, or other characteristics.

# Why Use Cosine Similarity?
# 1. Vectorization of Features: 
Movies can be represented as vectors, where each feature (e.g., genres, cast, production companies, popularity) is a component. Cosine similarity allows us to measure how "close" two movie vectors are in this high-dimensional space.

# 2. Magnitude Independence: 
Cosine similarity focuses on the direction of the vectors rather than their magnitude. This is crucial in cases where two movies might have very different absolute values (e.g., budget) but similar patterns across features. It helps when certain features vary greatly in scale, like revenue vs. vote average, without skewing the similarity score.

# 3. Works Well for High-Dimensional Data: 
In a recommender system, the feature space can become very large (especially after encoding categorical variables), and cosine similarity is computationally efficient for comparing such high-dimensional vectors.

# 4. Popular for Collaborative Filtering: 
In collaborative filtering, user-item interaction data (like movie ratings) can be represented as vectors. Cosine similarity is often used to compute similarities between users (user-based collaborative filtering) or items (movie-based collaborative filtering), which is useful for recommending movies based on user preferences or similar movies.

# 5. Effective for Sparse Data: 
Movie datasets are often sparse, meaning that many features (like cast or genre) don't apply to every movie. Cosine similarity handles this sparseness well by focusing on non-zero dimensions.

# Methodology

# Step 1: Loading of Data and Understanding the Dataset

The first step is loading the data and understanding the dataset which involves reviewing the dataset's columns, types, and summary statistics to gain insights into the data.

# Step 2: Identify Key Attributes
These are the most important features or columns that provide valuable information for analysis and model building.

# Step 3: Data Preprocessing
Data preprocessing involves cleaning, transforming, and organizing raw data into a format that can be effectively used for analysis and model building. Some of the steps include checking for missing values, encoding, feature engineering among others.

# Step 4: EDA - Exploring the Dataset
EDA involves visually and statistically exploring a dataset to uncover patterns, trends, and relationships.

# Step 5: One-Hot Encoding
This is a technique used to convert categorical variables into a numerical format that machine learning models can understand. This way, machine learning models can interpret categorical data without assuming any ordinal relationship between categories.

# Step 6: Feature Scaling
Scaling numeric features is necessary to ensure they are on the same scale.

# Step 7: Cosine Similarity
Cosine similarity is a metric used to measure how similar two vectors are, regardless of their magnitude. It calculates the cosine of the angle between two vectors, and the value ranges from -1 to 1

# Step 8: Recommendation
The recommendation part of the model involves calculating the similarity between movies based on certain features (such as genres, cast, crew, production companies, budget, and revenue) using cosine similarity. This process enables the system to suggest movies that are closely related in terms of content or characteristics, based on the selected features and the weights applied to each.
