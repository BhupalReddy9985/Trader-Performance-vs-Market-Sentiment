# Trader-Performance-vs-Market-Sentiment

# Objective

The goal of this project is to analyze how Bitcoin market sentiment (Fear vs Greed) relates to trader behavior and performance on the Hyperliquid platform. The analysis aims to uncover behavioral patterns and actionable insights that could inform smarter trading strategies under different market regimes.

# Datasets

# 1.Bitcoin Fear & Greed Index

Fields: timestamp, value, classification (Fear / Greed)

Used to represent daily market sentiment

# 2.Historical Trader Data (Hyperliquid)

Fields include: account, coin, execution price, trade size, side, timestamp, closed PnL, fees, etc.

Used to analyze trader performance and behavior

Both datasets were aligned at a daily level using date-based aggregation.

# Methodology

# 1.Data Cleaning & Preparation

Loaded both datasets and checked for missing values and duplicates

Converted timestamps to datetime format

Created a common date column and merged datasets on a daily basis

# 2.Feature Engineering

Daily PnL per trader

Win rate (percentage of profitable trades)

Average trade size (USD)

Leverage proxy (trade size relative to execution price)

Trade frequency (trades per day)

Long/Short ratio based on trade side

# 3.Analysis

Compared trader performance metrics across Fear vs Greed days

Analyzed behavioral changes such as leverage usage, trade size, and frequency

Segmented traders into groups:
      High vs Low leverage
      Frequent vs Infrequent traders
      Consistent vs Inconsistent traders (based on PnL volatility)

# 4.Visualization

Used boxplots and bar charts to compare distributions and behavioral differences

Generated summary tables to support findings

# Key Insights

# 1.Performance differs by market sentiment

Greed periods are associated with higher volatility in daily PnL.

Fear periods show more stable but generally lower returns.

# 2.Trader behavior changes with sentiment

Traders increase trade frequency and position size during Greed days.

During Fear days, traders reduce activity and exposure.

# 3.Risk is concentrated among specific trader segments

High-leverage and frequent traders experience larger drawdowns during Fear regimes.

Consistent traders show relatively stable performance across both sentiment states.

# Strategy Recommendations

# 1.Risk control during Fear periods

Cap leverage and reduce position sizes, especially for high-frequency traders, to limit drawdowns.

# 2.Selective aggressiveness during Greed periods

Allow increased trade frequency or leverage only for traders with historically consistent performance.

These rules of thumb can help adapt trading behavior dynamically based on prevailing market sentiment.
