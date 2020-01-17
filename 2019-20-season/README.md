# METHODOLOGY: Predicting the 2020 MVP with linear models

Each folder will contain an updated dataset, IPython notebook, and folder of predictions (graphs).

[Link to mid-season predictions blog post.](https://dribbleanalytics.blog/2020/01/2020-mvp-mid-season
)

## Dates of predictions

The data for the mid-season MVP prediction was gathered on 1/16 before any games were played. We predicted MVP probability for players on the top 10 of the NBA.com MVP ladder from 1/10.

## Data collection

First, I created a database of all the players who were top 10 in MVP voting since the 1984-1985 season up until last year. This was chosen as the cutoff because that is the first season for which Basketball-Reference has pre-season title odds.

We used all the counting and advanced stats available on Basketball-Reference (found [here](https://www.basketball-reference.com/leagues/NBA_2019_per_game.html) and [here](https://www.basketball-reference.com/leagues/NBA_2019_advanced.html)) as features in our model. In addition, we considered team wins, overall seed, pre-season title odds, All-Star votes, and offensive and defensive RAPTOR (538's player evaluation metric). Note that we use All-Star vote rank among players in the MVP race as our metric for All-Star votes because more players vote over time, making the raw numbers unstable.

For lockout years - 1998-1999 and 2011-2012 - we scaled up the necessary features (team wins, win shares, etc.) to the number of games in the lockout year; 1998-1999 was scaled up from 50 to 82, and 2011-2012 was scaled up from 66 to 82.

## Model creation

We created two models: a logistic regression and a linear discriminant analysis. Unlike last year's MVP predictions, we are creating classification models to predict MVP probability instead of regression models to predict expected vote share.

Our "model" takes the average of the prediction probabilities from the two models. We tested the model's performance by fitting the two models on all the data except for a given year, and then predicting the MVP in that year. 

## Predicting the MVP

All the models predict a player's MVP probability. The player with the highest predicted probability is the current predicted MVP winner.