# 📈S&P 500 Movement Prediction with Random Forests
This project implements a machine learning pipeline using a Random Forest Classifier to predict whether the S&P 500 Index (^GSPC) will go up or down the next day. The goal is to generate signals for longing or shorting the market based on historical data, improving precision through backtesting and engineered features.

## 🧠 Project Objective
The objective is to:
- Predict whether the S&P 500 will rise or fall the next day
- Use this prediction to simulate profitable long/short trading strategies
- Enhance model accuracy with engineered features and robust backtesting

## 🔍 Features
- **Data Source:** `yfinance` pulls historical data for the S&P 500 from 1990 onward
- **Initial Model:** trains a basic Random Forest on key features like `Close`, `Open`, `High`, `Low`, and `Volume`
- **Target Variable:** binary outcome (1 = price goes up, 0 = price goes down)
- **Evaluation Metric:** precision score to represent the accuracy of the model
- **Backtesting Framework:** evaluates model performance across multiple windows
- **Feature Engineering:** adds rolling averages and trend indicators to improve model robustness

## 📈 Results
- Initial model precision: 58%
- After backtesting and engineering: **Some improvement**, depending on threshold and horizon tuning (5-10%)

## 🚀 Requirements
- Python 3.8+
- Jupyter Notebook
- Pandas, NumPy, MatPlotlib, Scikit-Learn
- yfinance
Install dependencies via:
`pip install yfinance pandas scikit-learn matplotlib`

## 📬 Future Improvements
- Include real trading cost and slippage in backtesting
- Try other classifiers (XGBoost, SVM)
- Integrate live signals with brokerage API for paper/live trading
- Use additional macroeconomic indicators for feature enrichment
