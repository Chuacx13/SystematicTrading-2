# Systematic Trading 2: Combining Bollinger Bands, RSI, and ATR

This strategy integrates four technical indicators—Bollinger Bands, Relative Strength Index (RSI), Exponential Moving Average (EMA) and Average True Range (ATR) —to generate buy and sell signals. These indicators help identify potential trend reversals, momentum shifts, and market volatility, providing a well-rounded approach to decision-making in trading. The aim of this project is to achieve a Sharpe Ratio above 1 for trading AAPL stock while backtesting on insample results. Subsequently, it hopes to gain similar results in an out-of-sample result.

## Initial Setup and Optimized Parameters

The strategy is initialized by downloading historical stock data of AAPL and computing the Bollinger Bands, RSI, and ATR for each stock. The parameters used for each indicator a:

- **Bollinger Bands**: A window of 30 periods and 1 standard deviations is selected, allowing the bands to adjust to typical price swings.
- **RSI Window**: A 9-period window is chosen, which is different from the usual 14-day period for identifying overbought and oversold conditions.
- **ATR Window**: A 14-period ATR is used to capture the stock’s volatility trends.
- **EMA**: A 21-period window is used for long run ema and a 9-period window is used for short run ema.

These parameters have been adjusted and optimized to yield the **highest sharpe ratio** for our strategy among other parameters tested during the tuning process.

---

## Results

In-sample backtesting
![in-sample-results](/assets/in-sample-results.png)
Out-of-sample backtesting
![out-of-sample-results](/assets/out-of-sample-results.png)

### Performance Visualization

The strategy's performance is visualized by plotting the stock price, signals, and the cumulative returns over time. The performance comparison is made with a simple buy-and-hold strategy of APPL stock.

## Improvements

- Apply statistical tests
- Apply stop loss
