# m5-forecasting-accuracy

This work presents M5 accuracy competition: Results, findings, and conclusions. There are three main components:

1.   Analyzing data sets to summarize their main characteristics, as presented in **EDA.ipynb**.
2.   Selecting, manipulating, and transforming raw data into time-series features, as presented in **preprocess.ipynb**.
3.   Forecasting time series with Gradient boosting models, as presented in **model.ipynb**.

The experiment results showed that all the models could achieve very competitive results. However, while this study enabled me to accurately predict time series representing the hierarchical unit sales for the largest retail company, there are limitations to be addressed for future work.

First, while this work explored the use of "Date" and "Lag" data as features, other business features were not explored. It would be preferable to scrutinize several features based on business insights or common sense, such as Rolling-window analysis of a time series, Pricing (e.g., the weekly price of an item in each store, special events), and Trends (e.g., sales lags (n-p days), average volume per (item, (item +store))) since
the use of other features proved to be effective in reducing the forecasting error by 20% to 60% [ref](https://forecasters.org/resources/time-series-data/).

Second, this work dealt with the problem of Retail Demand Forecasting by using Gradient boosting, including Catboost, LightGBM, and XGBoost. While Gradient boosting could produce a good performance, several algorithms and techniques must be developed and considered in the future to explore better results. For example, using the regularization techniques of ridge, lasso, and elastic-net regression to deal with overfitting when the dataset is large, exploring the Prophet model, specifically designed to detect patterns in business time series with solid seasonality and several seasons of historical data, dealing with a custom ensemble-based model.

Finally, although this study explored basic and commonly used EDA techniques, there are relevant EDA techniques that were not tracked. Therefore, exploring other EDA techniques will be valuable for gaining insight into data.
