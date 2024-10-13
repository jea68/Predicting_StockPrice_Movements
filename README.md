# Project: Predicting Nasdaq Closing Price Movements

## Overview

This project aims to predict the closing price movements for hundreds of Nasdaq-listed stocks using order book and closing auction data. The focus is on the final ten minutes of trading, characterized by rapid price fluctuations and volatility. 

Using the dataset described below, LSTM and LightGBM models were developed to predict stock price movements relative to a synthetic index, aiding in price adjustment and trading opportunities.

The notebook titled [**Predicting Price Movements.ipynb**](https://github.com/jea68/Predicting_StockPrice_Movements/blob/main/Predicting%20Price%20Movements.ipynb) contains the notebook for this project, and the notebook **Baseline Solution** is a simple solution base case model.


## Project Summary

### Models Used
1. **LSTM**: Suitable for capturing long-term dependencies in time series data.
2. **LightGBM**: Efficient gradient boosting framework for large datasets.

### Achievements
- Merged order book and auction data for comprehensive analysis.
- LightGBM outperformed LSTM in predictive accuracy, achieving a lower MAE.

## Conclusion

The project successfully developed a model for predicting Nasdaq closing price movements, with LightGBM demonstrating superior performance. The skills and insights gained apply to real-world financial forecasting and high-frequency trading.

(see **Project Discussion.md** for a detailed review)

## Further Information

For more details, visit the [Kaggle competition page](https://www.kaggle.com/competitions/optiver-trading-at-the-close).
