# Predicting Short-Term Price Movements of Top 10 Cryptocurrencies Using Historical OHLCV Data

## Overview
This project focuses on predicting **short-term price direction** (up or down) of the **top 10 cryptocurrencies** using historical **OHLCV (Open, High, Low, Close, Volume)** data.
The goal is to evaluate whether traditional price-based and momentum features, combined with machine learning models, can capture short-term market movements.

## Dataset
- Historical OHLCV data for the top 10 cryptocurrencies
- Time-series data with engineered features
- Binary target variable indicating next-period price direction

## Feature Engineering
### Price-Based Features
* **Daily Return** – Measures day-to-day price change
* **High–Low Range** – Captures intraday volatility
* **Open–Close Range** – Indicates daily price pressure
* **7-day Volatility** – Short-term risk measure

### Moving Averages & Momentum
* **MA_7, MA_14** – Trend smoothing
* **Volume MA_7, MA_14** – Trading activity trends
* **Price vs MA Ratios** – Distance from recent trend
* **Momentum (t / t−7)** – Medium-term price strength

### Lag Features
* **Previous day return**
* **Previous day volume change**

## Target Variable
* **Target = 1** → Price increases in the next period
* **Target = 0** → Price decreases or stays the same

## Models Implemented
* Logistic Regression
* Random Forest
* Gradient Boosting
* Baseline Models

## Evaluation Metrics
* Accuracy
* Precision
* Recall
* F1-score
* Directional Accuracy
* Confusion Matrix

## Key Findings
* Ensemble models slightly outperform linear models
* Class imbalance impacts recall and precision
* Baseline strategies highlight market bias
* Feature engineering contributes more than model complexity

## Visualizations
* Model performance comparison charts
* Confusion matrices
* Metrics summary tables

## Limitations
* Moderate predictive performance
* High market noise in short-term crypto prices
* No external or sentiment data included

## Future Work
* Incorporate technical indicators (RSI, MACD)
* Add sentiment and macroeconomic data
* Explore deep learning models (LSTM, Transformers)
* Improve class balancing strategies

## Tools & Libraries
* Python
* Pandas, NumPy
* Scikit-learn
* Matplotlib, Seaborn
