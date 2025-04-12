
Data has always been an essential driver of trading, and traders have long made efforts to gain an advantage from access to superior information.

Today, modern traders, especially **high frequency trading (HFT)** firms, invest in ultra-fast data connections. However, because ultra-fast access can give an unfair advantage, regulators now use **speed-bumps** - intentional delays in processing orders to level the playing field. This is meant to prevent abuse from firms who might otherwise exploit tiny time advantages for arbitrage. 

## Traditional Investing vs Modern Quant Investing. 

### Traditional investing
* Relied mostly on public data like finantial statements, earning reports, macro and industry data. 
* Used models built by humans to project earnings and prices. 
* Included technical analysis such as chart patterns, indicators based on price and volume... 

### Modern Quant investing 
* ML can analyse this data more effectively. 

In this section we will analyse market and fundamental data sources and explains how they reflect the environment in which they are created. The details of the trading environment matter not only for the proper interpretation of market data but also for the design and execution of the strategy and the implementation of realistic backtesting simulations.


## Market Data reflects the trading environment. 
Maket data isn't just numbers - it is the result of how the market actually works. It is shaped by human behaviour, technology, rules and the back-and-forth of supply and demand. If you're trading, especially with algorithms or machine learning, understanding this is critical because it affects how you interpret the data and build strategies.

Algorithmic traders use algorithms, including ML, to analyze the flow of buy and sell orders and the resulting volume and price statistics to extract trade signals that capture insights into, for example, demand-supply dynamics or the behavior of certain market participants. 

### Market microstructure
This is the study of how the market wors at the deepest level. It focuses on: 
* Price discovery: how a price is formed from trades. 
Bid-ask spread: the gap between buying and selling prices. 
* LatencyL how fast information flows
* Transaction costs

It is crutial for: 
* Building realistic simulations of your strategy. 
* Understand why a trade went wrong or right
* Designing execution algorithms (i.e., how to enter/exit the market efficiently)

***Takeaway***

*To build strong trading systems — especially with machine learning — you don’t just need data.
You need to understand where that data comes from, how it’s created, and what market behavior it reflects.*

## Working with high-frequency market data
There are two main types of market data in the U.S. equities market, both governed by Reg NMS (Regulation National Market System): 
* Consolidated Feed: 
  - Combines quotes and trades from all exchanges.
    - Quotes: information about the current bid and ask prices for a particular security. The bid is the highest price a buyer is willing to pay, and the ask is the lowest price a seller is willing to accept.
    - Trade: includes details about executed trades, such as the price at which a security was bought or sold, the quantity traded, and the time of the transaction.
  - Managed by Securities Information Processors (SIPs).
  - Useful for broad market insights.
* Propierary data: 
  - Provided by individual exchanges (like NASDAQ).
  - Includes more detailed, real-time order flow and quote data.
  - Often used for high-frequency or algorithmic trading


How to work with NASDAQ order book data
* The order book shows real-time supply and demand (bids and asks).
* Data is delivered in “ticks” (every tiny market event).
* Quote Levels:
  - Level I: Basic best bid/ask prices.
  - Level II: adds information about bid and ask prices by specific market makers as well as size and time of recent transactions for better insights into the liquidity of a given equity.
  - Level III: adds the ability to enter or change quotes, execute orders, and confirm trades and is only available to market makers and exchange member firms. Access to Level III quotes permits registered brokers to meet best execution requirements.

The trading activity is reflected in numerous messages about orders sent by market participants. These messages typically conform to the electronic Financial Information eXchange (FIX) communications protocol for real-time exchange of securities transactions and market data or a native exchange protocol.

### AlgoSeek minute bars 
AlgoSeek provides historical intraday data at the quality previously available only to institutional investors. The AlgoSeek Equity bars provide a very detailed intraday quote and trade data in a user-friendly format aimed at making it easy to design and backtest intraday ML-driven strategies. As we will see, the data includes not only OHLCV (Open, High, Low, Close) information but also information on the bid-ask spread and the number of ticks with up and down price moves, among others. 

Quote and trade data fields The minute bar data contain up to 54 fields. There are 8 fields for the open, high, low, and close elements of the bar, namely:
- The timestamp for the bar and the corresponding trade
- The price and the size for the prevailing bid-ask quote and the relevant trade

There are also 14 data points with volume information for the bar period:
- The number of shares and corresponding trades
- The trade volumes at or below the bid, between the bid quote and the midpoint, at the midpoint, between the midpoint and the ask quote, and at or above the ask, as well as for crosses
- The number of shares traded with up- or downticks, i.e., when the price rose or fell, as well as when the price did not change, differentiated by the previous direction of price movement



