# Movie-Recommender-System-Capstone-Project

# What is a recommender system?
A recommender system is a type of information filtering system that provides personalized suggestions to users based on their preferences and behaviors. These systems are widely used to help users navigate through large amounts of data and find items that are most relevant to them. Recommender systems can be used in various sectors including:

# 1. E-commerce
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

# Why Use Cosine Similarity?
Cosine similarity is a metric used to measure the similarity between two vectors by calculating the cosine of the angle between them. 
In the context of a movie recommender system, each movie can be represented as a vector of features, such as genres, actors, directors, or other characteristics.

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

# Why Collaborative Filtering?
Compared to other methods like content-based filtering, which relies solely on movie features such as genre, director, and cast, collaborative filtering offers more diverse and unexpected recommendations, making the user experience better.
Collaborative filtering can also handle large datasets effectively, making it suitable for platforms with extensive user and movie bases. 
It also adapts to changes in user preferences over time, ensuring recommendations remain relevant.

# Problem Statement
With an ever-growing library of movies available on various platforms, users often struggle to find content that matches their tastes. This project addresses the challenge by creating a personalized movie recommendation system. The goal is to enhance user experience by suggesting movies that they are likely to find appealing based on their past viewing history and the preferences of similar users.

# Methodology

# Step 1: Fetch Movie Data
Using the TMDB API, we fetch data for a set number of popular movies, including details such as movie IDs, titles, genres, ratings, and popularity.

# Step 2: Create a Genre Map
We create a mapping of genre IDs to genre names using the TMDB API, enabling easier interpretation and categorization of movies by genre.

# Step 3: Fetch Multiple Movies
We retrieve multiple pages of popular movies from TMDB and store relevant details in a structured format for further processing.

# Step 4: Create User-Movie Matrix
A user-movie matrix is generated using simulated user ratings. This matrix represents user ratings for different movies, with users as rows and movies as columns.

# Step 5: Calculate Similarity
We calculate the cosine similarity between users based on their ratings in the user-movie matrix. This similarity matrix helps in identifying users with similar movie preferences.

# Step 6: Implement Collaborative Filtering
Using the similarity matrix, we identify the most similar users for a given user and predict ratings for movies that the user hasn't seen. Movies with the highest predicted ratings are recommended to the user.
