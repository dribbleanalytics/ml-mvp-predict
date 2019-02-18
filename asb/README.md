# METHODOLOGY: Using machine learning to predict the 2019 MVP: All-Star break predictions 

[Link to blog post.](https://dribbleanalytics.blogspot.com/2019/02/ml-mvp-predict-asb.html
)

## Dates of predictions

The data for the mid-season MVP prediction was gathered during the All-Star break.

## The new MVP ladder

|New MVP ladder|Old MVP ladder|
:--|:--|
|Giannis|Giannis|
|Harden|Harden|
|PG13|Curry|
|Curry|Kawhi|
|Embiid|Jokic|
|Jokic|PG13|
|KD|Embiid|
|LeBron|LeBron|
|Kawhi|KD|
|Kyrie|Davis|

## Stat changes (new - old stats)

|Player|MVP ladder rank|Team Wins|Overall Seed|PTS|TRB|AST|FG%|WS|VORP|
:--|--:|--:|--:|--:|--:|--:|--:|--:|--:|
|Giannis|0|+3.3|-1|+0.5|+0.1|+0.1|+0.2%|+1.4|+0.6|
|Harden|0|+0.6|-1|+2.4|+0.5|-1.1|+0.7%|+1.6|+0.7|
|PG13|+3|+2.5|0|+2.0|-0.1|+0.2|+0.8%|+1.8|+0.7|
|Curry|-1|+3.7|-1|-0.8|-0.1|-0.4|-0.1%|+0.8|+0.3|
|Embiid|+2|+0.1|2|+0.4|+0.2|+0.1|-0.4%|+0.3|+0.0|
|Jokic|-1|-0.5|1|+0.7|+0.4|+0.2|-0.1%|+0.2|-0.1|
|KD|+2|+3.7|-1|-0.6|-0.3|-0.2|+1.0%|+0.1|-0.1|
|LeBron|0|-2.6|3|-0.5|+0.3|+0.5|-0.5%|-1.4|-0.8|
|Kawhi|-5|-0.4|1|-0.5|-0.3|+0.1|-1.1%|-0.9|-0.3|


## Newest results

|Rank|NBA.com MVP ladder|SVM|RF|KNN|DNN|Average prediction|
--:|:--|:--|:--|:--|:--|:--|
|1|Giannis|Giannis|Giannis|Giannis|Giannis|**Giannis**|
|2|Harden|Harden|Harden|Harden|Harden|**Harden**|
|3|PG13|KD|PG13|Jokic|PG13|**PG13**|
|4|Curry|Jokic|KD|PG13|KD|**KD**|
|5|Embiid|PG13|Curry|Curry|Jokic|**Jokic**|
|6|Jokic|Curry|Kawhi|KD|Curry|**Curry**|
|7|KD|Kawhi|Jokic|Embiid|Embiid|**Kawhi**|
|8|LeBron|Embiid|Embiid|Kawhi|Kawhi|**Embiid**|
|9|Kawhi|Kyrie|Kyrie|Kyrie|Kyrie|**Kyrie**|
|10|Kyrie|LeBron|LeBron|LeBron|LeBron|**LeBron**|
