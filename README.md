# Stock-Market-Analysis-Prediction-Yahoo-Finance-Data-
This project analyzes historical stock data to explore trends, generate trading signals, and predict the next day’s closing price using a linear regression model. It demonstrates practical use of Pandas, Matplotlib, and Scikit-Learn for real-world financial data analysis.

Dataset

Source: Yahoo Finance (yfinance Python library)

Ticker Example: Apple Inc. (AAPL)

Date Range: 2022-01-01 to 2025-01-01

Columns Used:

Open, High, Low, Close, Volume

Computed:

Short_MA (20-day), Long_MA (50-day), Crossover, Next_Close

Methods

Data Cleaning & Feature Engineering

Removed NaN values for moving averages.

Calculated rolling moving averages (20-day & 50-day) to identify trends.

Trend Analysis

Plotted closing price and moving averages to visualize market trends.

Detected Buy/Sell signals using moving average crossovers:

Buy: Short-term MA crosses above long-term MA

Sell: Short-term MA crosses below long-term MA

Predictive Modeling

Built a Linear Regression model to predict the next day’s closing price using:

Features: Close, Short_MA, Long_MA

Target: Next_Close (shifted by one day)

Split data into 80% training and 20% testing sets.

Evaluated using Mean Squared Error (MSE) and R² score:

MSE ≈ 10.65

R² ≈ 0.918

Visualization

Scatter plots for Buy/Sell signals on price chart.

Line plots comparing predicted vs actual next-day closing prices.

Helps identify patterns, volatility, and prediction accuracy visually.

Insights

The linear regression model predicted next-day prices with high accuracy (R² ~ 0.918).

Buy/Sell signals mostly aligned with short-term trends, making the moving average crossover strategy effective for visualization and portfolio-style analysis.

Short-term moving averages capture volatility and provide actionable insights for trend-following strategies.

Tools & Libraries

Python 3.12

Pandas, NumPy

Matplotlib, Seaborn

Scikit-Learn (Linear Regression)

yfinance (data fetching)


Next Steps / Extensions

Include other technical indicators (RSI, MACD) for more refined signals.

Compare multiple stocks in a portfolio to visualize relative performance.

Try ARIMA or LSTM models for multi-day or more accurate forecasts.

Add a backtesting module to calculate hypothetical returns based on Buy/Sell signals.
