This dataset contains historic data for the daily ten minute closing auction on the NASDAQ stock exchange. Your challenge is to predict the future price movements of stocks relative to the price future price movement of a synthetic index composed of NASDAQ-listed stocks.

This is a forecasting competition using the time series API. The private leaderboard will be determined using real market data gathered after the submission period closes.

Files
[train/test].csv The auction data. The test data will be delivered by the API.

{[stock_id]} - A unique identifier for the stock. Not all stock IDs exist in every time bucket.
date_id - A unique identifier for the date. Date IDs are sequential & consistent across all stocks.
imbalance_size - The amount unmatched at the current reference price (in USD).
imbalance_buy_sell_flag - An indicator reflecting the direction of auction imbalance.
buy-side imbalance; 1
sell-side imbalance; -1
no imbalance; 0
reference_price - The price at which paired shares are maximized, the imbalance is minimized and the distance from the bid-ask midpoint is minimized, in that order. Can also be thought of as being equal to the near price bounded between the best bid and ask price.
matched_size - The amount that can be matched at the current reference price (in USD).
far_price - The crossing price that will maximize the number of shares matched based on auction interest only. This calculation excludes continuous market orders.
near_price - The crossing price that will maximize the number of shares matched based auction and continuous market orders.
[bid/ask]_price - Price of the most competitive buy/sell level in the non-auction book.
[bid/ask]_size - The dollar notional amount on the most competitive buy/sell level in the non-auction book.
wap - The weighted average price in the non-auction book.


BidPrice∗AskSize+AskPrice∗BidSizeBidSize+AskSize
seconds_in_bucket - The number of seconds elapsed since the beginning of the day's closing auction, always starting from 0.
target - The 60 second future move in the wap of the stock, less the 60 second future move of the synthetic index. Only provided for the train set.
The synthetic index is a custom weighted index of Nasdaq-listed stocks constructed by Optiver for this competition.
The unit of the target is basis points, which is a common unit of measurement in financial markets. A 1 basis point price move is equivalent to a 0.01% price move.
Where t is the time at the current observation, we can define the target:
Target=(StockWAPt+60StockWAPt−IndexWAPt+60IndexWAPt)∗10000
All size related columns are in USD terms.

All price related columns are converted to a price move relative to the stock wap (weighted average price) at the beginning of the auction period.

https://www.kaggle.com/competitions/optiver-trading-at-the-close/data
