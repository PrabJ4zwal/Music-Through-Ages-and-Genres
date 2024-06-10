# Music Through Ages and Genres

# Preword 

I would like to note that this project contains explicit words and words of profanity that are uncovered in the exploratory data analysis section. These words are never intended to offend, only used for analysis. 

## Context and Problem Statement
The purpose of this project is to explore how the characteristics of music change over time and by genre, with gratitude to SAURABH SHAHANE for providing an [excellent dataset of music from 1950 - 2019](https://www.kaggle.com/datasets/saurabhshahane/music-dataset-1950-to-2019/code). Being a musician myself, I went into this project with some strong preliminary knowledge and so the process of uncovering knowledge from data has been enlightening.
    Whilst this piece can for the most part be considered primarily an exploratory analysis piece (heavy on data exploration, visualisation and commentary), I also produce 3 machine learning models to demonstrate the power of machine learning for research in music fields; thede models (1) Classify songs into genres using lyrics. (2) Classify songs by decade using lyrics (3) Classify songs into genres using their characteristic scores (e.g sadness/energy/instrumentalness). To evaluate these models I primarily lean on the F1-score which provides the harmonic mean between precision and recall, a useful metric since it was found that classes in the data were imbalanced. I also produce confusion matrix reports to compare model performances before and after gridsearching for hyperparameter tuning. 

## Methodology

I produce 4 notebooks of code which you can find in the 'code' folder - 
1. '1. EDA' which explores the music dataset in depth with visualisations, commentary and engineering of new features 'decade' and 'processed_lyrics' for further exploration and modelling in subsequent notebooks. 
2. '2. Classifying_genres_from_lyrics' which uses logistic regression modelling for multiclass classification tasks, gridsearching over the best hyperparameters, and, commentary on model evaluation.
3. '3. Classifying_decade_from_lyrics' repeats the process in the previous notebook. 
4. '4. Classifying genres from characteristics' using Random Forest Classifier for the multi-class classification task. 


## Data Dictionary

artist_name: Name of the artist.

track_name: Name of the track.

release_date: Year the track was released.

genre: Genre of the track.

lyrics: Original lyrics of the track as presented by the original dataset.

processed_lyrics: Preprocessed lyrics for model input.

decade: Decade of the track release.

Various Numerical Features:

dating, violence, world/life, night/time, shake the audience, family/gospel, romantic, communication, obscene, music, movement/places, light/visual perceptions, family/spiritual, like/girls, sadness, feelings, danceability, loudness, acousticness, instrumentalness, valence, energy, topic: Various features representing different aspects of the song's content and audio characteristics.


## Findings and Conclusion

This project provides insights into how music characteristics vary by genre and over time. 

Through exploring and analysing the data I find the following - 
1. Over time songs are getting more electronic, less acoustic, shorter on average, louder, and more energetic.
2. Hip-hop genres of music can be lyrically characterised as having the highest number of words of profanity amongst the top 20 most frequently occuring words accross genres.
3. Hip-hop has highest scores in characteristics of Obscenity and Danceability / Jazz leads in acousticness and instrumentalness with hip-hop being the lowest of these/ Country leads in sadness / Rock leads in energy and violence. 

The models developed for classifying songs by genre and decade based on lyrics and specific features demonstrate the potential of machine learning in understanding musical trends. Despite the challenges of imbalanced data, the models achieved reasonable performance with all models beating the baseline accuracy, and,  with hyperparameter tuning providing marginal improvements.

Further improvements might require different approaches such as:

Trying different models (e.g., Random Forest, SVM, Neural Networks).
Engineering new features or using different text vectorization methods (e.g., Word2Vec, GloVe).
Increasing the dataset size or improving the quality of the data through webscraping lyrics for songs. 
Given further time to undestand ROC AUC curve, I would also incorporate this as a metric for model evaluation however my current understanding at this time is too rocky for it to be a useful metric in this project. 