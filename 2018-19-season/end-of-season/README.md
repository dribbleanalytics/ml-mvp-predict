# METHODOLOGY: Using machine learning to predict the 2019 MVP: end of season predictions 

[Link to blog post.](https://dribbleanalytics.blog/2019/04/ml-mvp-all-nba-predict-2019)

## Dates of predictions

The data for the end of season MVP predictions was gathered after the end of the regular season.

## Final MVP ladder (week 25)

|Rank|Player|
--:|:--|
|1|Giannis Antetokounmpo|
|2|James Harden|
|3|Paul George|
|4|Stephen Curry|
|5|Joel Embiid|
|6|Nikola Jokic|
|7|Kevin Durant|
|8|Damian Lillard|
|9|Kawhi Leonard|
|10|Russell Westbrook|

## Results

|Rank|NBA.com MVP ladder|SVM|RF|KNN|DNN|**Average prediction**|
--:|:--|:--|:--|:--|:--|:--|
|1|Giannis|Harden|Giannis|Giannis|Harden|**Giannis**|
|2|Harden|Giannis|Harden|Harden|Giannis|**Harden**|
|3|PG13|Jokic|Curry|PG13|Jokic|**Jokic**|
|4|Curry|KD|Jokic|Curry|KD|**Curry**|
|5|Embiid|Curry|Embiid|Kawhi|Lillard|**PG13**|
|6|Jokic|Kawhi|PG13|Jokic|PG13|**KD**|
|7|KD|Lillard|Kawhi|KD|Curry|**Kawhi**|
|8|Lillard|PG13|Lillard|Lillard|Embiid|**Lillard**|
|9|Kawhi|Embiid|KD|Embiid|Kawhi|**Embiid**|
|10|Westbrook|Westbrook|Westbrook|Westbrook|Westbrook|**Westbrook**|
