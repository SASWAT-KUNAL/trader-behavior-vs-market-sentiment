# Trader Behavior vs Bitcoin Market Sentiment

## Objective

The goal of this project is to explore how trader behavior relates to Bitcoin market sentiment, using two datasets:

1. Bitcoin Fear/Greed Index - daily classification of market sentiment
2. Historical trading data from Hyperliquid - including execution prices, trade sides, size, PnL, and fees

By merging these datasets on date, I analyzed whether sentiment (fear or greed) has a measurable impact on how traders perform, how much they trade, and what they pay in fees.

## Data Overview

The historical trading dataset includes columns like:
- Account
- Coin
- Execution Price
- Size USD
- Side (Buy/Sell)
- Timestamp
- Closed PnL
- Fee

The sentiment dataset includes:
- Date
- Value (numeric index)
- Classification (Extreme Fear, Fear, Neutral, Greed, Extreme Greed)

## Methodology

- Loaded both datasets and converted timestamps to a consistent datetime format
- Aggregated the trading data by day to calculate:
  - Average PnL
  - Total volume traded
  - Total fees paid
- Merged aggregated trader data with the daily sentiment classification
- Created visual comparisons to analyze trends across different sentiment levels

## Key Insights

1. Trader PnL is mostly stable across sentiment levels.  
   On average, trader profitability does not show a strong difference between fear and greed days. This suggests that experienced traders may not be overly influenced by market sentiment.

2. Trading volume is significantly higher on Fear and Extreme Fear days.  
   Volume traded increases steadily from greed to fear, with the highest volume observed on days classified as Extreme Fear. This indicates traders are more active during market uncertainty, possibly due to volatility or attempts to capitalize on dips.

3. Fees paid also increase on Fear and Extreme Fear days.  
   The total fees paid by traders rise alongside trading volume. Higher fees may reflect more frequent trades or reactive strategies during high-sentiment volatility.

## Tools and Libraries Used

- Python
- Pandas
- Matplotlib
- Seaborn
- Jupyter Notebook

## How to Use

Clone this repository, open the notebook file (assignment.ipynb), and run the cells in order. All data exploration and visualizations are included inline in the notebook.

## Author

Saswat Kumar Panda  
Applied for: Junior Data Scientist - Trader Behavior Insights

