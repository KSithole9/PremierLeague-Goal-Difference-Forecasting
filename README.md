# PremierLeague-Goal-Difference-Forecasting
The datasets used in this project were obtained from the English Premier League collection available at https://www.kaggle.com/datasets/saife245/english-premier-league.

Abstract: This paper explores the use of machine learning models to predict outcomes in the English Premier League (EPL) results over the course of multiple seasons. Using a model trained on goal differentials from a previous season, the model will predict results for the next season. The model is able to determine whether a team is likely to win or lose by using the predicted goal difference data. Our model assumes that all teams in both seasons consist of the same players. This project achieves the best results when using linear regression compared to other models such as RandomForestRegressor, DecisionTreeRegressor, and SVR. This method provides a basis for further improvements and offers insightful information about the difficulties involved in predicting the results of football games.

Introduction: The English Premier League (EPL), known for its unpredictable nature and intense competition, is considered the highest level of football. Because team lineups are always changing, forecasting the results of matches is extremely difficult. By utilizing machine learning techniques and emphasizing goal difference as a crucial metric for prediction, this study seeks to address this challenge. This method shows the possible effectiveness of such approaches by using historical data from one season to train a model and then using that model to predict results in the next season.

Data Analysis: Each English Premier League season comprises twenty teams, each team participates in 19 home games and 19 away games. At the end of each season, the three teams with the worst performance are dropped out, making way for new teams in the next season from the EFL Championship, the second tier of English football. This system of promotion and relegation in each season helps to maintain a competitive balance for the top two tiers of English football. It is also common for teams to have different players in each season. Because we were not provided player data in our datasets, we will assume the players on each team throughout both seasons remain the same for this project.


![image](https://github.com/KSithole9/PremierLeague-Goal-Difference-Forecasting/assets/152675019/9bd90b93-5bd2-4ba2-b54d-f5e9bfe03935)

These graphs show the similarity in team performance during both seasons used in this project. Even with the possibility for teams to consist of different players in the following season, there is a clear correlation in team performance regardless of this.

Data Preprocessing: The first step in data preprocessing is to load and filter datasets for the 2020–2021 and 2021–2022 EPL seasons. For analysis purposes, columns like home team, away team, full-time home goals (FTHG), and full-time away goals (FTAG) are kept. To maintain dataset consistency, teams that are not in both seasons are removed from the datasets.


![image](https://github.com/KSithole9/PremierLeague-Goal-Difference-Forecasting/assets/152675019/24d52881-4979-46b3-825f-a7126771c613)

![image](https://github.com/KSithole9/PremierLeague-Goal-Difference-Forecasting/assets/152675019/48e46956-458a-483a-9827-58c9392d267e)
Feature Engineering: Each team is assigned a unique ID to create a standardized representation for teams throughout both seasons. These are listed in each row as HomeID and AwayID to represent which teams are playing each other. A column for GoalDif is added as our predictor which represents the goal difference between the home and away teams. Goal differential is a reliable indicator of team performance and is computed as (HomeGoals - AwayGoals). By choosing to use goal difference over ratios, data analysis problems caused by infinite, or zero ratios are reduced.

![image](https://github.com/KSithole9/PremierLeague-Goal-Difference-Forecasting/assets/152675019/95a50fe3-653b-4612-b91b-862ce754240e)

![image](https://github.com/KSithole9/PremierLeague-Goal-Difference-Forecasting/assets/152675019/1b3742db-f639-4add-b235-d4e574388b42)


![image](https://github.com/KSithole9/PremierLeague-Goal-Difference-Forecasting/assets/152675019/508e7df4-9c93-4f10-9835-557986bff783)


Model Selection: Several regression models were taken into consideration, such as Decision Tree Regressor, Random Forest Regressor, Support Vector Regressor (SVR), and Linear Regression. Based on accuracy metrics, Linear Regression stands out as the preferred model, outperforming other models with a mean squared error of 3.79. As mentioned before, we are training our model on the first season and testing on the following season.

![image](https://github.com/KSithole9/PremierLeague-Goal-Difference-Forecasting/assets/152675019/9cf993e3-ab1a-4a99-ad7d-72542a348b4f)

![image](https://github.com/KSithole9/PremierLeague-Goal-Difference-Forecasting/assets/152675019/695d8f18-b810-4880-9e2e-c3f5f9669ebe)
Results: Applying the linear regression model on the 2021–2022 season shows encouraging accuracy, with a mean squared error of 3.79. SVR (3.84), Random Forest Regressor (4.54), and Decision Tree Regressor (6.42) are examples of comparative models that are not as accurate. The results of the predicted values are interesting. While they are still far from the actual values, they provide predictions that can be used to calculate the likelihood of the home team winning or losing. If the predicted value is positive, it is likely the home team will win. If the predicted value is negative, it is likely the away team will win. This model provides a great foundation for predicting the next season's match outcome.

![image](https://github.com/KSithole9/PremierLeague-Goal-Difference-Forecasting/assets/152675019/a215666c-69df-4b59-95c3-9c508c1df85d)
Conclusion: In conclusion, this study demonstrates that it is possible to predict English Premier League results with a machine learning model that has been trained on the home team, away team, and goal difference information from the previous season. The application of linear regression has proven to be effective. Even without player-specific data, the model provides insightful information about how matches will turn out. This project establishes the foundation for future investigation and improvement, with the possibility of adding more features to improve prediction performance.



