# predict-NBA-FantasyPoints
Development of LightGBM regressors for predicting NHL Fantasy Points

## Description

This GitHub repository houses Jupyter notebooks that allow for the development and application of LightGBM and Random Forest regressors that make aggregate predictions for NBA Fantasy Points. All data is pulled from [StatHead](https://stathead.com/), which requires a paid subscription. In any notebooks that use a login request to retrieve data, I have removed my email and password from the request.

## List of Notebooks (in order of use) and their uses
* *NBA_predict_FP_getmoredata-github.ipynb*: get fantasy scoring data from StatHead for all NBA players for the 2017-18 season to the 2021-22 season
* *NBA_predict_FP-moredata_ETL.ipynb*: extract, transform, and load data. Engineers features for use in the regressor
* *NBA_predict_FP_moredata_LGBM_models.ipynb*: develop LightGBM regressors with tuned hyperparameters for each position (G, F, C) to predict fantasy points
* *NBA_predict_FP_moredata_RF_models.ipynb*: develop Random Forest regressors with *n_estimators* = 1000 for each position (G, F, C) to predict fantasy points
* *NBA_predict_FP_getseason_data-github.ipynb*: get fantasy scoring data from StatHead for all NBA players for the current season that predictions will be made for
* *NBA_predict_FP_moredata_makepreds-github.ipynb*: get recent fantasy scoring data, merge with year-to-date fantasy scoring data, perform ETL, make aggregate predictions with LGBM and RF models, optimize lineups


## Dependencies

* Python libraries: sklearn >= v0.24.2, pandas, numpy, joblib, pulp, lightgbm
* [StatHead](https://stathead.com/) subscription

## Output

Optimized fantasy lineups for a slate of games (where 9 players are selected for a lineup by position) or a single game (where 5 players are selected and positions don't matter).

## Authors

Gregory Szwabowski (gszwabowski@gmail.com)
