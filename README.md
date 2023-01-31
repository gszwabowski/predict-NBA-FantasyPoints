# predict-NHL-FantasyPoints
Development of LightGBM regressors for predicting NHL Fantasy Points

## Description

This GitHub repository houses Jupyter notebooks that allow for the development and application of LightGBM regressors that predict Fantasy Points for NHL players. All data is pulled from [FantasyData](https://fantasydata.com/), which requires a paid subscription. In any notebooks that use a login request to retrieve data, I have removed my email and password from the request.

## List of Notebooks (in order of use) and their uses
* *NHL_predict_FP-getdata-github.ipynb*: get fantasy scoring data from FantasyData for all NHL players for the 2016-17 season to the 2021-22 season
* *NHL_predict_FP-ETL.ipynb*: extract, transform, and load data. Engineers features for use in the regressor
* *NHL_predict_FP-LGBM.ipynb*: develop LightGBM regressors for each position (C, W, D, G) to predict fantasy points
* *NHL_predict_FP-getseason_data-github.ipynb*: get fantasy scoring data from FantasyData for all NHL players for the current season (that predictions will be made for)
* *NHL_predict_FP-makepredictions-github.ipynb*: get recent fantasy scoring data, merge with year-to-date fantasy scoring data, perform ETL, make predictions, optimize lineups


## Dependencies

* Python libraries: sklearn >= v0.24.2, pandas, numpy, joblib, pulp, lightgbm
* [FantasyData](https://fantasydata.com/) subscription

## Output

Optimized fantasy lineups for a slate of games (where 9 players are selected for a lineup by position) or a single game (where 5 players are selected and positions don't matter).

## Authors

Gregory Szwabowski (gszwabowski@gmail.com)
