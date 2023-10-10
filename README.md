
# Cryptocurrency Price Prediction, Machine Learning and Python.
# Project Overview

In this project, the goal is to predict the future price of Bitcoin using a combination of historical cryptocurrency data (specifically Bitcoin prices) and information from Wikipedia detailing edits made to the Bitcoin page. 

The approach involves merging and consolidating these datasets to train machine learning models, initially starting with a random forest model. The objective is to determine whether cryptocurrency prices will increase or decrease the following day. 
Later, the model transitioned to using XGBoost and refined predictors to enhance prediction accuracy.

To assess the performance of these models, a backtesting system needs to be developed. This system will enable the evaluation of the models' predictions using historical data, providing valuable insights into their effectiveness. Additionally, selecting a robust error metric is crucial for accurately measuring the models' performance and making informed decisions about their effectiveness in predicting Bitcoin prices.




## Code

You can find the code for this project [here](https://github.com/dataquestio/project-walkthroughs/tree/master/bitcoin_price)

File overview:

* `predictive.ipynb` - a Jupyter notebook that contains the code to predict cryptocurrency prices
* `datasets.ipynb` - a Jupyter notebook that creates our wikipedia edit dataset.

# Crypto Price Prediction

## toolkit used

In this project,the following are used to build the model:

* JupyerLab
* Python 
* Python packages
    * pandas
    * yfinance
    * scikit-learn
    * xgboost
    * mwclient
    * transformers

## Dataset used

The wikipedia data is generated and it is computed in the repo. Stored in `wikidatas.csv`.  
In the project Bitcoin price data is downloaded using the package `yfinance`.

## Operation of the model

Running the code `datasets.ipynb` generates a new Wikipedia edits dataset. 

Running  the code in `predictive.ipynb`.  By default, this will load data from an existing `btc.csv` file.  

`btc.csv` file contains the stock market data

Each line in this format typically represents a single day's trading activity for a specific stock.

Date: The specific date of the trading day.
Open: The opening price of the stock at the beginning of the trading day.
High: The highest price at which the stock traded during the trading day.
Low: The lowest price at which the stock traded during the trading day.
Close: The closing price of the stock at the end of the trading day.
Volume: The total number of shares traded during the day.
Dividends: Any dividends paid out to shareholders on that day.
Stock Splits: If there were any stock splits on that day, indicating how many shares were split into a different number of shares.


for example,  2023-10-10,150.00,155.20,148.50,153.75,1000000,0.50,2


Date: October 10, 2023
Open: $150.00
High: $155.20
Low: $148.50
Close: $153.75
Volume: 1,000,000 shares
Dividends: $0.50 per share
Stock Splits: 2-for-1 split (meaning each share was split into 2 shares)

Data is loaded by default from the existing btc.csv file

Removing btc.csv will download the latest data from Yahoo Finance.
