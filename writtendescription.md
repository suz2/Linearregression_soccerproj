# Inspection into the determinants of goal scoring in a soccer game season
Zimu Su

## Abstract

This project aims at exploring the deterministic factor of soccer team performance to score the goals in a league season using linear regression model. The data of goals scoring and performance from the aspects of shots, possession and defensive action are collected from the male soccer teams in big 5 European leagues and Major League Soccer (MLS) in United States by web scraping fbref.com. The interpretation of the results could provide suggestions to team coach or manager to improve team’s scoring ability and get well prepared for a league season.

## Design
There is a leading trend of data-driven analysis in elite soccer team to help coach make tactics to win the game. As more specific data of team performance can be collected based on advanced sensor-based technique, it is very interesting to inspect the significant factor for goal scoring. In this project, the team’s scoring ability is cumulatively measured within the range of all the matches in a league season rather than in a specific match, because there are not so many goals scoring in a match level (mostly <4). The features of determinants are selected from aspects of shots, ball possession and defensive actions for a team in a season level. To enhance team rank in a league season, the team manager or coach could benefit from the analysis by identifying the influential aspect of team performance for scoring ability.
## Data

The datasets include 590 team statistics from Big 5 European league and Major League Soccer (MLS) in United States within 2017 - 2021 season. The goal scoring of one team per game in one season is employed as target. The features can be categorized into the aspects of shots (shots on target percentage, shots per game), possessions (possession rate, average passes percentage, dribbles successful rate) and defensive actions (block, interceptions, tackles, dribble tackles percentage). Pair plot and variance inflation factor are inspected to exclude the collinearity.

## Algorithms

*Web scraping*
Build a pipeline to collect the datasets from fbref.com using python module beautiful soup.

*Feature engineering*
* Standardilize the feature variables
* Use pair plot and variance inflation factor to exclude or transform the variables with multicollinearity.

*Models* Linear regression is performed with cross validation and lasso regularization (for mitigation of overfitting). The residual normality is checked by residual plot and Q-Q plot. Durbin watson statistic is checked to exclude the possibility of residual autocorrelation because it might be possible that the team behave very likely in each league season. Excluding those features with very low coefficients, the p-value for f test of the coefficients is less than 0.05. The model results are finally evaluated using R2 (0.798) and mean absolute error (0.165 goal per game). 

## Tools

Beautifulsoup, Scikit Learn, Pandas, Numpy, Seaborn

## Communication

The project is under supervision of Rita Biagioli and Lisa VanderVoort. The presentation is made on 02/23/22.



