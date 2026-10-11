# Predictive Analytics for Stock Market Movements

## Project Overview
This project uses historical stock market data and Machine Learning classification models to predict whether the next trading day's closing price will increase compared with the current day's closing price.

## Objectives
- Analyse historical stock prices and trading volume.
- Perform data cleaning and exploratory data analysis (EDA).
- Create technical indicators and features.
- Train and evaluate Machine Learning models.
- Compare baseline and expanded-feature model performance.

## Dataset
- **Observations:** 9,909
- **Original columns:** Date, Open, High, Low, Close, Adj Close, Volume
- **Period:** December 1980 – April 2020

## Tools and Technologies
- Python
- Pandas and NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook
- GitHub

## Data Processing and Feature Engineering
The project includes data validation, daily returns, moving averages, Relative Strength Index (RSI), multi-period returns, moving-average ratios, rolling volatility, and volume changes.

The target variable is 1 when the next trading day's closing price is higher than the current closing price, and 0 otherwise.

## Machine Learning Models
- Logistic Regression
- Random Forest Classifier

The data was split chronologically into training and testing sets to preserve time order.

## Model Evaluation Results

| Experiment | Model | Accuracy | ROC-AUC |
|---|---|---:|---:|
| Baseline | Logistic Regression | 52.07% | 0.5125 |
| Baseline | Random Forest | 47.72% | 0.5010 |
| Expanded Features | Logistic Regression | 50.66% | 0.5041 |
| Expanded Features | Random Forest | 50.05% | 0.5166 |

The results indicate limited predictive performance. ROC-AUC values remain close to 0.5, so the models do not demonstrate a strong ability to distinguish between upward and non-upward price movements.

## Project Files
- `Stock_Market_Prediction_Final_Report.docx` — Project report
- `stock_market_features.csv` — Feature-engineered dataset
- `model_comparison.csv` — Model evaluation comparison
- `stock_predictions.csv` — Actual and predicted directions
- `improved_logistic_model.joblib` — Saved Logistic Regression pipeline
- `improved_random_forest_model.joblib` — Saved Random Forest model
- Jupyter Notebook — Analysis and model development code

## Conclusion
The project demonstrates a complete workflow for historical stock data analysis, feature engineering, model training, and evaluation. The tested models showed weak predictive performance, and further experimentation and time-series validation are needed.

## Limitations and Disclaimer
The dataset represents historical market behaviour. The models do not account for all economic events, company announcements, market sentiment, transaction costs, or slippage. This project is for educational purposes only and is not financial advice or a guarantee of future results.
