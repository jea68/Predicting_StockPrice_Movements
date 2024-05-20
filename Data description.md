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


reduced data is only stock_id = 0, as the data set is too large to upload