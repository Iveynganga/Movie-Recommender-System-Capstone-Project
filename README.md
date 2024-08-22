# Movie-Recommender-System-Capstone-Project

# Project Overview
This project aims to develop a personalized movie recommender system. The system leverages collaborative filtering techniques to provide movie suggestions tailored to individual user preferences and historical interactions. By analyzing user ratings and movie data, the recommender system can predict and suggest movies that users are likely to enjoy.
Collaborative filtering is a technique used in movie recommender systems to suggest films to users based on the preferences and behaviors of similar users. 
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
