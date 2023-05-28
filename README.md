# Microsoft Movie Start-up Analysis

By Victor Mwatu
***
***

<div>
<center><img src="images/movie.jpg" height="300"/></center>
</div>

## Overview
***
Microsoft corporation intends to venture into movie production business. The statistical analysis below determined the best course of action to take in terms of which kinds of moveis are most popular.

## Business Problem
***
Microsoft corporation wants to start a movie production studio. This is a data driven analysis on the movies that are top rated by online voters to determine the best movies to produce. Customer satisfaction is the main goal of any business because it directly affects the profitability of a business. Here we shall try to find patterns that relate to customer satisfaction.


<div>
<center><img src="images/movieBiz.jpg" height="300"/></center>
</div>

## Data Understanding
***
The data is from two of the most popular movie rating and analysis websites, 'IMDB', 'The MoviesDB', and 'Rotten Tomatoes' have been chosen for their popularity and comprehensive data. The data contains movie ratings, genres, and release date which are the target data for this study but also includes other data fields as well. The success of movies will be rated by customer satisfaction represented here as movie ratings.

## Conclusions

From the data analysis done the following inferences were drawn:

1. Movie lengh should be ideally between 50 to 200 minutes. Movies with this length have the highest ratings.

2. The most produced movie genre is Drama and Comedy which seem largest market. 

3. Most movies are of English language.

Future analysis:

Future analysis is recomended to establish correlations between these variables and others. 

avg_imdb = imdb_data['averagerating'] 
lenght_imdb = imdb_data['runtime_minutes']

fig, ax = plt.subplots(figsize=(10,5))

ax.scatter(avg_imdb, lenght_imdb)

ax.set_title('Ratings vs Movie Length')
ax.set_ylabel('Movie Length')
ax.set_xlabel('Ratings')

imdb_data['genres'].value_counts().head(10).plot.barh(color='blue');


rt_release_month.plot.bar(color='red')