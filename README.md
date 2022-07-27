# TV_shows_ML_Analysis

## Overview of Project
This project is a Natural Language Processing classification of the TV Shows reviews as an input data for machine learning algorithm to predict movie ranking score


## Reasons for selecting the topic: 
* Possibility to use NLP
* Everybody likes TV shows
* Good database with two different reviews with match ranking was available

## Description of the source of data: 

Kaggle website - a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges. To process that we will use NRCLex library that measures the emotional effect from a body of text. This gives frequencies of words with particular emotions in the database. We will use this as a input for neural network model to predict meta_score of the tv show.

## Questions to to answer with the data: 
* Is NLP emotion classification able to predict TV shows ranking score?
* Which emotions are better predictors of meta score?
* Which algorithm is better to predict meta score with?


## Description of the data exploration phase of the project (preliminary data preprocessing, feature engineering and feature selection, including their decision-making process)
* Kaggle data was downloaded and imported into jupyter notebook.
* Rows with no reviews or critic meta_score were deleted.
* Dropping tv shows that have just one season. 
* Dropping the reviews that are shorter than 300 characters. 
* NRCLex library was used to create emotion words frequencies for each of the review. We exported reviews to a list and then used loop to apply NRCLex function to each element and append to a list of dictionaries. Then this list of dictionaries was transformed into pandas dataframe.
* From new dataframe two columns that did not have any variation were dropped (anticipation and anticip). After, column with sum of the emotion words frequencies was added.
* Emotion frequencies data frame was merged with original data frame.
* Merged data frame was split into predicted value = y = critic meta score; and input values for the model = X = frequencies of emotions words and file with optional input features.
* All files were saved as csv files and as such uploaded to SqlLite database.

## Description of the analysis phase of the project

* Compare emotion frequencies between different tv shows meta score. This should give us an overview of the data we obtained and if it has a potential for good prediction. 
* Creating regression model to predict tv show critics score based on emotion words frequencies with artificial neural networks and linear regression. This should give us answer how each of the emotion frequency affects the meta critic score. 
* Then, neural artifical network model was created to see if more complex relationships between emotion frequencies exist and we could use them to predict the meta critic score. 
* Also, random forest model was created, which should be faster to train than ANN but should give similar accuracy.


## Description of the tool(s) that will be used to create final dashboard, Description of interactive element(s)

* Our final dashboard is made with Tableu.
* Interactive element: PCA plot that shows the name of the tv show when cursor is placed on it. 

checkout: [Link to slide show with the project description](https://docs.google.com/presentation/d/1-XUbWYdJ5RLEgE5cJGqF8EMfjUlFZJgu3gpEb6eA8Jo/edit#slide=id.g13b592af808_0_18)

 ## Data Visualisation: 
 An initial visualisation of the TV Show Analysis:
 [Click here for Dashboard Visualization](https://public.tableau.com/app/profile/michaelangelo.kodjoe/viz/TVShowsAnalysis/TVShowAnalysis)

