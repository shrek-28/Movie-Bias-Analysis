# 📊 Does Fandango Inflate Movie Ratings?

## Overview
This project explores potential bias in Fandango’s movie ratings, specifically investigating whether Fandango systematically inflated user ratings compared to other platforms such as IMDB, Rotten Tomatoes, and Metacritic. The analysis is inspired by Nate Silver’s FiveThirtyEight article that raised concerns about Fandango's objectivity.

The original article can be explored at this link: https://fivethirtyeight.com/features/fandango-movies-ratings/ 

## Objectives
The primary goals of this project are to:
* Determine whether Fandango’s rating system favors higher ratings.
* Compare Fandango ratings to those of IMDB, Rotten Tomatoes, and Metacritic.
* Assess the distribution and central tendency of movie ratings across platforms.

## Dataset Information 
The source of the dataset, was obtained from FiveThirtyEight, at this link: https://github.com/fivethirtyeight/data/tree/master/fandango 
Both CSV files, ```fandango_scrape.csv``` and ```all_sites_scores.csv``` were downloaded.

#### Feature Information: 
```all_sites_scores.csv``` contains every film that has a Rotten Tomatoes rating, a RT User rating, a Metacritic score, a Metacritic User score, and IMDb score, and at least 30 fan reviews on Fandango. The data from Fandango was pulled on Aug. 24, 2015.

Column | Definition
--- | -----------
FILM | The film in question
RottenTomatoes | The Rotten Tomatoes Tomatometer score  for the film
RottenTomatoes_User | The Rotten Tomatoes user score for the film
Metacritic | The Metacritic critic score for the film
Metacritic_User | The Metacritic user score for the film
IMDB | The IMDb user score for the film
Metacritic_user_vote_count | The number of user votes the film had on Metacritic
IMDB_user_vote_count | The number of user votes the film had on IMDb

`fandango_scrape.csv` contains every film 538 pulled from Fandango.

Column | Definiton
--- | ---------
FILM | The movie
STARS | Number of stars presented on Fandango.com
RATING |  The Fandango ratingValue for the film, as pulled from the HTML of each page. This is the actual average score the movie obtained.
VOTES | number of people who had reviewed the film at the time we pulled it.

## Data Cleaning and Preprocessing Steps
1. The year was used as a separate variable, to allow separate analysis.
2. Only films in both Fandango Ratings and All Site Ratings were filtered out and utilized.
3. Normalization of scores to fit them between a 0-5 rating, as present in Fandango ratings.

## Exploratory Data Analysis Conducted:
1. Different sorts of plots, including scatterplots, KDE plots, clustermaps and histograms were utilized, to view the distributions of different variables, counts of differences, and to analyze relationships between critic ratings and user ratings.
2. Comparisons were made between Fandango ratings, and ratings from IMDB, MetaCritic and Rotten Tomatoes.
3. Scores were normalized to make sure all ratings are on the same scale

## Key Findings
1. Fandango shows a higher rating, for even the worst rated films, showing a rating between 3-4.
2. Even the worst film, Taken 3, according to the dataset, was rated a 4.5 stars, whereas the other sites showed a normalized rating of 1.89 stars only.
3. The other sites, such as RT, MetaCritic, and IMDB show other ratings such as between 1-3 only, for the worst films. 
