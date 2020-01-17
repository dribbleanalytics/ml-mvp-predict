# Dribble Analytics MVP predictions

This repository contains code, data, and results for our MVP predictions for the 2018-19 and 2019-20 seasons.

Each folder will contain an updated dataset, IPython notebook, and folder of predictions (graphs).

[Link to most recent MVP predictions post.](https://dribbleanalytics.blog/2020/01/2020-mvp-mid-season
)

## 2018-19 predictions

For our 2018-19 predictions, we created four regression models to predict a player's vote share. They used a variety of counting stats, and advanced stats, and team success stats (seed and wins). They correctly predicted Giannis to win MVP.

All the code, data, and graphs are available in the "2018-19-season" folder.

## 2019-20 predictions

We used a much different method for our 2019-20 predictions. We used simpler models, as our data set is very small. Furthermore, instead of creating regression models, we created two linear classifiers (logistic regression and linear discriminant analysis).

All the code, data, and graphs are available in the "2019-20-season" folder.

We use the average prediction probability of the two models to create our MVP predictions.

The models take into account several more factors than last year. We added features to account for narrative (by including pre-season title odds), popularity (All-Star votes), and better metrics for performance (538's RAPTOR).

We hope that using simpler models with better data will result in even better predictions.

Our most recent predictions were performed using data from 1/16. They were:

|Rank|NBA.com MVP ladder|Model prediction|
--:|:--|:--|
|1|Giannis|Giannis|
|2|LeBron|LeBron|
|3|Doncic|Davis|
|4|Harden|Harden|
|5|Butler|Doncic|
|6|Davis|Butler|
|7|Jokic|Jokic|
|8|Mitchell|Kawhi|
|9|CP3|Mitchell|
|10|Kawhi|CP3|