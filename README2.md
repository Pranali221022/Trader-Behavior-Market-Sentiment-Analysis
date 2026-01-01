##Trader Behavior vs Market Sentiment Analysis

##Overview
This project analyzes historical trader behavior data to uncover patterns in profitability, trading frequency, trade size, and transaction costs. The goal is to derive actionable insights that can support smarter and more efficient
trading strategies.

The analysis is exploratory in nature and focuses on understanding how trader performance behaves under varying levels of trading activity and cost exposure, while outlining a framework for integrating market sentiment.

##Datasets Used

1.Historical Trader Data 
Transaction-level trading data containing:
- Execution price
- Trade size (tokens and USD)
- Buy/Sell direction
- Timestamps (IST)
- Realized profit and loss (Closed PnL)
- Transaction fees
- Trade identifiers

2.Bitcoin Fear & Greed Index
Daily market sentiment data containing:
- Sentiment classification (Fear, Neutral, Greed)
- Sentiment index value
- Date and timestamp

##Methodology

###Data Preprocessing
- Parsed timestamps using correct day-first datetime format.
- Handled missing PnL values by treating them as zero.
- Derived trade_date from intraday timestamps to enable daily aggregation.

###Feature Engineering
- Created daily performance metrics including:
  - Total daily PnL
  - Average trade size (tokens and USD)
  - Trade count per day
  - Total daily transaction fees

###Aggregation
- Converted transaction-level data into daily-level metrics to support meaningful trend and behavior analysis.

##Exploratory Data Analysis (EDA)

The following analyses were conducted:

1.Daily PnL Distribution
- Identified a highly skewed profit distribution.
- Found that a small number of extreme days drive overall profitability.

2.Trade Count vs Profitability
- Observed no strong linear relationship between trade frequency and PnL.
- Identified increased downside risk during periods of excessive trading.

3.Fees vs Profitability
- Found that high transaction costs often coincide with flat or negative returns.
- Highlighted the importance of cost-efficient trading behavior.

##Key Insights

- Trader profitability is highly volatile and driven by infrequent extreme events.
- Higher trading frequency does not guarantee better performance.
- Overtrading increases exposure to transaction costs and downside risk.
- Moderate and selective trading activity tends to outperform aggressive
  high-frequency behavior.
- Transaction fees materially impact net profitability and should be actively
  managed.

##Market Sentiment Framework

The Fear & Greed Index is included to demonstrate a sentiment-based analytical framework. Due to non-overlapping time ranges between trader data and sentiment data, direct date-wise merging was not performed.

However, the methodology illustrates how trader behavior can be evaluated under different market sentiment regimes when aligned datasets are available.

##Limitations

- Trader data and sentiment data do not overlap temporally.
- Sentiment analysis is demonstrated conceptually rather than empirically.
- Results are exploratory and not intended for predictive modeling.

##Tools & Libraries
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn


##Author
Pranali Morajkar