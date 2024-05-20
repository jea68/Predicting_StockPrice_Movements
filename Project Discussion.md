
## Why We Chose LSTMs and LightGBM Models

### LSTM (Long Short-Term Memory) Models:

- Suitability for Time Series Data: LSTMs are a type of recurrent neural network (RNN) that excel in handling time series data and sequential dependencies. They can capture patterns over time, making them suitable for predicting stock price movements where historical price trends and sequences are crucial.

- Handling Long-Term Dependencies: Unlike traditional RNNs, LSTMs are designed to mitigate the vanishing gradient problem, enabling them to capture long-term dependencies in the data. This is particularly important for financial data, where past events can significantly influence future prices.

### LightGBM (Light Gradient Boosting Machine):

- Efficiency and Speed: LightGBM is known for its high efficiency and speed, thanks to its histogram-based approach and leaf-wise growth strategy. It is capable of handling large datasets with high-dimensional features quickly and effectively. The dataset used for this project is very large.

- Accuracy and Performance: LightGBM often achieves state-of-the-art performance on structured/tabular data. Its ability to capture complex interactions between features and its robustness against overfitting (when properly tuned) make it a strong choice for predictive modeling in finance.

- Ease of Use and Scalability: LightGBM is user-friendly and can be easily scaled to handle large datasets. Its hyperparameters are relatively easy to tune, and it integrates well with other Python data science tools.

## Why LightGBM Performed Better

- Nature of Financial Data:

Financial data, particularly in this project, includes a mix of numerical features such as imbalance sizes, reference prices, and various bid/ask prices and sizes. LightGBM is particularly adept at handling such structured data and can effectively model the relationships between these features.

- Model Interpretability and Feature Importance:

LightGBM provides built-in feature importance metrics, which help in understanding the contribution of each feature to the model's predictions. This interpretability is crucial in financial applications where understanding the drivers of model predictions can inform trading strategies and risk management.

- Training Time and Computational Resources:

LSTMs require more computational resources and longer training times compared to LightGBM. Training deep learning models like LSTMs involves complex computations that are time-consuming, especially with large datasets. LightGBM, on the other hand, is much faster to train, making it more practical for iterative development and hyperparameter tuning.

- Overfitting and Generalization:

While LSTMs are powerful, they are also prone to overfitting, especially with small datasets or when the data does not have strong sequential dependencies. LightGBM tends to generalize better on structured data with appropriate regularization and hyperparameter tuning, leading to better performance on unseen test data.

## Conclusion
In this project, we initially explored both LSTM and LightGBM models due to their respective strengths in handling time series and structured data. After rigorous evaluation, LightGBM outperformed LSTM in terms of Mean Absolute Error (MAE) on the test set. The efficiency, scalability, and superior performance of LightGBM on the structured dataset, combined with its ability to handle large amounts of data quickly, made it the better choice for predicting stock price movements in this context.