# NBA Win Prediction

## Purpose:
Create a Machine Learning model that takes input NBA data and ouputs which team will win the game.

## Methods:
Sourced data primarily from **basketball-reference.com** and worked in Jupyter Notebooks for project development. The task in Logistic Regression (win-loss), but outputs a win percent since most sports games do not have guaranteed results.

## Model:
A 3-hidden-layer deep-learning model was used for this logistic regression task. \
Regularlization methods incluide: Dropout (20%|0.2) and BatchNorm1d. \
Input and Internal layers feature ReLU outputs and Output layer features sigmoid for Binary Cross Entropy Loss. \

## Results:
**The model achieved an overall 66% accuracy.** \
Testing Statistics: \
Accuracy: 0.66 \
Precision: 0.652 \
Recall: 0.659 \
F1-measure: 0.651 \
The model is favored towards home games, either due to data imbalance or home advantage (as discussed below). \
|           | precision | recall | f1-score | support |
|-----------|-----------|--------|----------|---------|
| away_team | 0.60      | 0.48   | 0.53     | 2157    |
| home_team | 0.69      | 0.78   | 0.73     | 3167    |
\
![image](https://github.com/ahernandezjr/nba-win-prediction/assets/76761720/80dbe379-20ef-49f2-8547-66f67fd670ba) \

## Discussion:
Various models land within the range of 60% to 70% accuracy. Lower percent models tend to only use player statistics. Higher percent models create ELO/MMR systems assigned to teams and track them throughout the year. Given this model takes simple data without much modification, this is viewed as a success. \
Win percent is impacted by a *Home-Advantage Phenomenon*. Given that games played at home in the NBA increase the home-team's chance of winning to ~60%, this impacts the model as viewed in the confusion matrix below.

## Future Work:
Further regularization methods could be used on the data. \
Dataset balancing between home and away games (3167 vs 2157) may help imrpove the model. \
A collaborative, simple website is intended to run the model.
