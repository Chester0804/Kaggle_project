# Kaggle_project
In this project, I backtested several models which essentially are to predict stock market to go up or go down based on news. DJIA and S&P500 are the research objects.

## Folders description
* Key results are summarized in "result.md"
* "DJIA_long_only" folder is the detailed result for DJIA by assuming that short selling is not allowed.
* "DJIA_long_short" folder is the detailed result for DJIA by assuming that short selling is allowed.
* "SP500_long_short" folder is the detailed result for SP500 by assuming that short selling is allowed.
* "SP500_improvement_v1" folder is the improvement on SP500.
* "raw_data" folder contains all raw datasets used. 

## Description for each folder
* For "DJIA_long_only" and "DJIA_long_short", I provide the detailed portfolio information for the best AUC in Kaggle with the filling method "fill at t+0 close" and also the portfolio information for the highest Sharpe ratio. Besides, I provide the Jupyter notebook and also the performance summary table for both filling methods.
* For "SP500_long_short", I provide the detailed notebook and performance summary table for both filling methods.

## Special notes for the highest Sharpe ratio strategy (DJIA)
* The modeling method is using the top 3, 10, 25 news on day i to make predictions for day i+2 by neural network.
* Short-selling is allowed.
* The strategy is to make decision on day i+1, i.e. based on news of day i, predict the up or down trend of day i+2, wait until day i+1 to make decision (long or short or hold).
* Filling method is t+0 close price.
