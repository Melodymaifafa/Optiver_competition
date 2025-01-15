
# Optiver - Trading at the Close

## Overview

This project is based on the [Kaggle competition: Optiver - Trading at the Close](https://www.kaggle.com/competitions/optiver-trading-at-the-close/overview), which uses actual stock quotes and trading data to predict stock price movements in the last 10 minutes of each trading day. 

### Problem Statement
The competition involves a regression prediction task, with the **Mean Absolute Error (MAE)** as the evaluation metric to measure the accuracy of predictions.

---

## Data Processing and Feature Engineering

During the data processing and model development phases, a series of features were extracted to capture the dynamics of stock prices and trading activities. These include:

### 1. **Order Book Dynamic Features**
- `imbalance_buy_sell_flag * imbalance_size`: Reflects the market's imbalance in buying and selling power.
- `bid_size + ask_size`: Indicates market liquidity and activity.

### 2. **Combined Price Features**
- Calculated differences and products between various prices to capture interrelationships among market prices.

### 3. **Weighted Price Features**
- Weighted average prices based on stock weights to reflect overall market trends.

### 4. **Historical Price Features**
- Captured trends and cyclical patterns by calculating past numerical values based on historical prices.
- Computed differences between historical and current prices to highlight short-term price changes.

---

## Model Development

### Model Choice
Used **LightGBM**, a gradient boosting framework known for its efficiency and strong performance in regression tasks. LightGBM was well-suited to handle the characteristics of the dataset.

### Testing Strategy
To enhance robustness and avoid overfitting:
- Transaction dates were divided into five segments to create test sets.
- Comprehensive testing was conducted to ensure model reliability across varying conditions.

---

## Summary
This project highlights the importance of feature engineering and robust testing in stock price prediction tasks. By leveraging market dynamics, historical trends, and a reliable model like LightGBM, this complex regression challenge has been tackled effectively. Check out the detailed implementation in this repository for further insights.
