# METHODOLOGY: Using machine learning to predict the 2019 MVP

Much of this methodolgy is similar to my previous post, "Finding the least and most deserving MVPs of the last decade." The primary differences are the dataset used and the model parameters. The GitHub for the original MVP project can be found [here](https://github.com/dribbleanalytics/least-most-deserving-mvps).

Each folder will contain an updated dataset, IPython notebook, and folder of predictions (graphs). As of now, there's only one folder, which contains mid-season predictions.

[Link to mid-season predictions blog post.](https://dribbleanalytics.blogspot.com/2019/01/ml-mvp-predict-midseason.html)

[Link to All-Star break predictions blog post.](https://dribbleanalytics.blogspot.com/2019/02/ml-mvp-predict-asb.html)

## Dates of predictions

The data for the mid-season MVP prediction was gathered on 1/14 before any games were played.

## Data collection

First, I created a database of all the players who were top 10 in MVP voting since the 1979-1980 season up until last year. This was chosen as the cutoff because the 3 point line was introduced that year.

**This dataset is different from the one in the previous MVP post because it includes every year since 1979-1980, while the previous post only went until 2007-2008 so it could predict the last decade.**

The following stats were recorded for all these players:

| Counting stats | Advanced stats| MVP votes | Team stats |
| ------------- | ------------- | ------------- | -------- |
| G | WS | MVP votes won | Wins |
| MPG | WS/48 | Maximum MVP votes | Overall seed |
| PTS/G | VORP | Share of MVP votes* |  |
| TRB/G | BPM | |
| AST/G | | |
| STL/G | | |
| BLK/G | | |
| FG% | | |
| 3P% | | |
| FT% | | |

*Vote share = percentage of maximum MVP votes. So, all the players' vote share does not add up to 1 for all players. Only a player who receives every first place vote will have a vote share of 1 (Curry 2016).

For lockout years - 1998-1999 and 2011-2012 - I scaled up the win shares, VORP, and team wins according to the number of games in the lockout year; 1998-1999 was scaled up from 50 to 82, and 2011-2012 was scaled up from 66 to 82.

For this year's predictions, I scaled these stats according to the number of games the team has played so far.

All data was taken from [Basketball Reference](http://basketball-reference.com/).

## Model creation

Using scikit-learn, I created four models: a support vector regression (SVM), a random forest regression (RF), a k-nearest neighbors regression (k-NN), and a multi-layer perceptron regression (or deep neural network, DNN). Each model used scikit-learn's train test split function with a test size of 25%.

**In the previous MVP analysis, most of the stats in the table above were used as parameters. However, for these predictions, only the following parameters were used:**

| Couting stats | Advanced stats | Team stats |
| ------------- | -------------- | ---------- |
| PTS/G | VORP | Wins |
| TRB/G | WS | Overall seed |
| AST/G | | |
| FG% | | |

Several parameters were removed from the previous model because some created collinearity (such as VORP, BPM, and MP all being included).

Each model's mean squared error and variance score (r-squared) was measured to find the most accurate regression. Each model's cross-validation score for r-squared was also measured to help determine the most accurate model. Note that a higher rsquared and explained variance indicates a more accurate regression, but a lower mean squared error indicates a more accurate regression.

Along with these basic goodness-of-fit tests, I performed a standardized residuals test, Shapiro-Wilk test, Jarque-Bera test, and Durbin-Watson test. In addition to these test, I created Q-Q plots and learning curves.

## Predicting the MVP

All the models predict a player's vote share.  The player with the highest predicted vote share is the current predicted MVP winner.
