# Project: Predicting Nasdaq Closing Price Movements

## Overview

This project aims to predict the closing price movements for hundreds of Nasdaq-listed stocks using order book and closing auction data. The focus is on the final ten minutes of trading, characterized by rapid price fluctuations and volatility. 

Using the dataset described below LSTM and LightGBM models were developed to predictsstock price movements relative to a synthetic index, aiding in price adjustment and trading opportunities.


## Dataset Description

The dataset includes historic data for the ten-minute closing auction on the Nasdaq Stock Exchange. Key columns include:

- `stock_id`: Unique identifier for the stock.
- `date_id`: Unique identifier for the date.
- `imbalance_size`: Amount unmatched at the reference price.
- `imbalance_buy_sell_flag`: Direction of auction imbalance.
- `reference_price`, `matched_size`, `far_price`, `near_price`: Various price metrics.
- `bid_price`, `ask_price`, `bid_size`, `ask_size`: Competitive buy/sell levels in the non-auction book.
- `wap`: Weighted average price in the non-auction book.
- `seconds_in_bucket`: Seconds elapsed since the auction's start.
- `target`: 60-second future move in the WAP of the stock relative to the synthetic index.

## Model Evaluation

Models were evaluated using the Mean Absolute Error (MAE):

\[ MAE = \frac{1}{n} \sum_{i=1}^{n} |y_i - x_i| \]

Where \( y_i \) is the predicted value and \( x_i \) is the observed value.

## Project Summary

### Skills Demonstrated
- **Data Science**:
  - Data cleaning, preprocessing, and feature engineering.
  - Exploratory Data Analysis (EDA).
  - Time series analysis.

- **Machine Learning**:
  - Feature selection and model tuning.
  - Training and evaluating LSTM and LightGBM models.

### Models Used
1. **LSTM**: Suitable for capturing long-term dependencies in time series data.
2. **LightGBM**: Efficient gradient boosting framework for large datasets.

### Achievements
- Merged order book and auction data for comprehensive analysis.
- LightGBM outperformed LSTM in predictive accuracy, achieving a lower MAE.

## Conclusion

The project successfully developed a model for predicting Nasdaq closing price movements, with LightGBM demonstrating superior performance. The skills and insights gained are applicable to real-world financial forecasting and high-frequency trading.

## Further Information

For more details, visit the [Kaggle competition page](https://www.kaggle.com/competitions/optiver-trading-at-the-close).