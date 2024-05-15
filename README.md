# Overview

https://www.kaggle.com/competitions/optiver-trading-at-the-close

Developed a model capable of predicting the closing price movements for hundreds of Nasdaq listed stocks using data from the order book and the closing auction of the stock.  (Target = The 60 second future move in the wap of the stock, less the 60 second future move of the synthetic index. Only provided for the train set.)
The model predicts the future price movements of stocks relative to the price future price movement of a synthetic index composed of NASDAQ-listed stocks.
Information from the auction can be used to adjust prices, assess supply and demand dynamics, and identify trading opportunities.

# Details about the Order Book and Auction
Each trading day on the Nasdaq Stock Exchange concludes with the Nasdaq Closing Cross auction. This process establishes the official closing prices for securities listed on the exchange. These closing prices serve as key indicators for investors, analysts and other market participants in evaluating the performance of individual securities and the market as a whole.

In the last ten minutes of the Nasdaq exchange trading session, market makers merge traditional order book data with auction book data. This ability to consolidate information from both sources is critical for providing the best prices to all market participants.

## Order Books and Auction Books
1. Order Book:
- Continuous Trading: In an order book system, trading occurs continuously throughout the trading session. Buyers and sellers can place orders at any time, and trades are executed as soon as matching orders are found. Order book operates on Price-time priority
- Price Discovery: Prices are determined dynamically based on the continuous interaction between buy and sell orders. The order book displays the current best bid and ask prices, along with the depth of liquidity at various price levels.
- Market Liquidity: Liquidity is typically spread out across various price levels, reflecting the ongoing trading activity.

2. Auction Book:
- Discrete Trading: In an auction book system, trading occurs at specific intervals or scheduled times. Orders are collected and matched during these auction periods, and trades are executed at a single price or within a price range determined by the auction mechanism.
- Price Discovery: Prices are determined through the auction process, where buy and sell orders are matched based on predetermined rules or algorithms. The auction mechanism may consider various factors such as order size, price, and time priority.
- Market Liquidity: Liquidity is concentrated within each auction period, as orders are matched and executed in bulk. The depth of liquidity may vary depending on the frequency and duration of auction sessions.

In summary, while both order books and auction books facilitate trading in financial markets, they differ in terms of trading dynamics, price discovery mechanisms, and liquidity distribution. Order books provide continuous trading and dynamic price discovery, while auction books offer discrete trading and price determination through scheduled auction sessions. Market makers often leverage both types of trading mechanisms to optimize their trading strategies and provide liquidity to the market.


# Evaluation 

My Model is evaluated on the Mean Absolute Error (MAE) between the predicted return and the observed target. The formula is given by:

MAE=1n∑i=1n|yi−xi|
Where:

n is the total number of data points.
y_i is the predicted value for data point i.
x_i is the observed value for data point i.

https://www.kaggle.com/competitions/optiver-trading-at-the-close


# More details

https://www.kaggle.com/code/tomforbes/optiver-trading-at-the-close-introduction