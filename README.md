# PremierLeague-Goal-Difference-Forecasting
The datasets used in this project were obtained from the English Premier League collection available at https://www.kaggle.com/datasets/saife245/english-premier-league.

Abstract: This paper explores the use of machine learning models to predict outcomes in the English Premier League (EPL) results over the course of multiple seasons. Using a model trained on goal differentials from a previous season, the model will predict results for the next season. The model is able to determine whether a team is likely to win or lose by using the predicted goal difference data. Our model assumes that all teams in both seasons consist of the same players. This project achieves the best results when using linear regression compared to other models such as RandomForestRegressor, DecisionTreeRegressor, and SVR. This method provides a basis for further improvements and offers insightful information about the difficulties involved in predicting the results of football games.

Introduction: The English Premier League (EPL), known for its unpredictable nature and intense competition, is considered the highest level of football. Because team lineups are always changing, forecasting the results of matches is extremely difficult. By utilizing machine learning techniques and emphasizing goal difference as a crucial metric for prediction, this study seeks to address this challenge. This method shows the possible effectiveness of such approaches by using historical data from one season to train a model and then using that model to predict results in the next season.

Data Analysis: Each English Premier League season comprises twenty teams, each team participates in 19 home games and 19 away games. At the end of each season, the three teams with the worst performance are dropped out, making way for new teams in the next season from the EFL Championship, the second tier of English football. This system of promotion and relegation in each season helps to maintain a competitive balance for the top two tiers of English football. It is also common for teams to have different players in each season. Because we were not provided player data in our datasets, we will assume the players on each team throughout both seasons remain the same for this project.


![image](https://github.com/KSithole9/PremierLeague-Goal-Difference-Forecasting/assets/152675019/9bd90b93-5bd2-4ba2-b54d-f5e9bfe03935)


