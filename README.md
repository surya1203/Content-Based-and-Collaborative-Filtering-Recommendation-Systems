# Content-Based-and-Collaborative-Filtering-Recommendation-Systems

This was our final project for CS 593: Data Mining II: Advanced Algorithms for Mining Big Data, under Porf. Khashayar Dehnad. This project contains two types of  recommendation systems, both working on independent of each other: 1. Content Based Recommendation System and 2. Collaborative Filtering Recommendation System. Content based recommendation systems recommend items such as movies, songs, products etc. (movies in our case) to users based on the similarity of content, whereas collaborative filtering recommendation systems suggests content based on the similarity between the users.

## Content Based Recommendation System:
Dataset : [Netflix Movies and TV Shows](https://www.kaggle.com/datasets/shivamb/netflix-shows)

The dataset contains TV shows and Movies from Netflix, and is constantly updated. Currently, after the mid-2021 update, it has over 8000 rows and 200M subscribers. It contains The dataset contains attributes like: show_id, title, director, cast, country, date_added, release_year, rating, duration listed_in description, type, year_added, month_added; which are very good metadata! Attributes: show_id, title, director, cast, country, date_added, release_year, rating, duration listed_in description, type, year_added, month_added; which are very good metadata! RAKE, short for Rapid Automatic Keyword Extraction algorithm, has been used to extract a lot of the attribute values, which is a keyword extraction algorithm which tries to determine key phrases in a body of text. We used to it to comb through the dataset to extract prediction variables like cast, director and common key words. This needs to be done since those columns do not have the data in our required format. Thus, we extract them and ‘bag’ them in separate easily accessible lists. Cosine similarity is the metric used to measure how similar the documents are irrespective of their size.


## Collaborative Filtering Reommendation System:
Dataset : [The Movies Dataset](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset?select=ratings_small.csv)

The dataset we are using for collaborative filtering is called The Movies Dataset. We are specifically using ‘ratings_small.csv’ out of the available files as we only need userId, movieId and ratings for a collaborative filtering prediction. It is a subset of 100,000 ratings from 700 users on 9,000 movies. It has 4 columns: userId, movieId, rating & timestamp; and more than 100,000 rows, which is a good sample size for a prediction. Surprise, used for this recommendation system, is a Python scikit for building and analyzing recommender systems that deal with explicit rating data. The name SurPRISE (roughly :) ) stands for Simple Python Recommendation System Engine. It provides ready-to-use prediction algorithms for recommendation systems, and can use both built-in datasets, as well as custom datasets. We used RMSE as accuracy measure.









