# FINTECH PROJECT 3

## Bitcoin’s Price Correlation with the Stock Market & BTC Price Prediction 

### First Notebook

#### **Analyzing the evolution of Bitcoin’s price correlation with the stock market over time.**

* **Has there been a change in how Bitcoin’s price moves with the market? If so, why?**
  * Before 2020, crypto assets such as Bitcoin and Ethereum showed little correlation with major stock indices. They were thought to help diversify risk and act as a hedge against swings in other asset classes and inflation.
  * Lately, Bitcoin’s correlation with stocks has turned higher than that between stocks and other assets such as gold, investment grade bonds, and major currencies which suggests that suggest that Bitcoin has been acting as a risk asset.
  * Since 2020, sentiment in crypto and equity markets indicate a growing interconnectedness between the two asset classes that could destabilize financial markets.
  * An explanation for this could be the fact that central banks flooded markets with liquidity in 2020 when the pandemic happened and increased money supply much quicker than in the past.
  * Another reason why we can say that there has been a change in how Bitcoin’s price moves with the market is because Bitcoin has always been considered inflation-proof and could therefore be a hedge against rising inflation. However, its extreme volatility and growing correlation with the stocks threatens this theory.

* **Use Sentiment Analysis to see the sentiments expressed about Bitcoin in news headlines, social media, and other texts.**

### Second Notebook

Part 1
* BTC performance analysis with the market to see if correlation has changed over time 
  * SPY (Overall)- Chose SPY as a benchmark to see how the overall market performed
  * BTC (Crypto Currency)- Chose BTC as the benchmark crypto
  * ETH (Crypto Currency)- Chose ETC to see if it follows BTC or if it’s an anomaly
  * XRP (Crypto Currency)- Chose XRP to see if it follows BTC or if it’s an anomaly
* Price movement analysis- Time period: 1/1/18- 12/31/21
* Quantitative analysis
* Calculate returns and combine them in a data frame then plot the performance analysis charts 
* **How did the relationship between BTC and SPY change over time?**
  * From 2018 to 2019, we can see that BTC, ETH and XRP move more closely together while SPY follows its own path. But in 2020, we see BTC breakaway from its pattern with the other cryptocurrencies and become more strongly correlated with SPY. From 2020 to 2021, we also see how BTC’s volatility increases drastically. The change in relationship between BTC and SPY can be attributed to the change of sentiment in crypto as well as increased market liquidity caused by the pandemic. 
* Risk analysis of returns
  * Calculate the std deviation
  * Calculate and plot beta
  * Calculate the correlation
  * Calculate the volatility
* Calculate sharpe ratio
* Data visualization
  1. Cumulative returns performance analysis
  2. Correlation mix and heat map
  3. Fitting a regression line on the correlation between SPY & BTC 
  4. Rolling std plot
  5. Rolling beta plot
  6. Density plot (Volatility)
  7. Sharpe ratio bar

* **Analyze data**
  * **Standard Deviation**- Standard deviation is a measure of how far data points deviate from the mean. Volatile stocks have a higher standard deviation which indicates the stock has a higher risk. Looking at the standard deviation plot, BTC has a higher standard deviation than SPY, ETH and XRP which means it is more volatile. It’s also important to note that BTC’s standard deviation increases drastically in early 2021, which is when it becomes more strongly correlated with SPY.
  * **Volatility**- Using the density plot, we can measure the volatility of the stock. The less volatile the stock, the smaller the standard deviation value. A smaller standard deviation means that the stock is less likely to have large (positive or negative) changes in value. Looking at the density plot, we see that BTC has the widest distribution making it more volatile because there is a greater percentage in price movement. This means there is a greater chance of observing a wider range of prices which we can also see from the fluctuation in both BTC’s prices and returns.
  * **Correlation**- Correlation is the positive or negative relationship between two variables. From the correlation mix, we can see that BTC and SPY are not perfectly correlated so correlation does not imply causation. However, they are very highly correlated which suggests a strong relationship. SPY also seems to have a strong correlation with ETH while it has a low correlation with XRP. BTC has a high correlation with ETH, but it has a moderate correlation with XRP. ETH and XRP have a moderately high correlation with each other which suggests that when it comes to following SPY movement, XRP would be the anomaly.  
  * **Beta**- Beta is a measure of the volatility—or systematic rick—of a security or portfolio compared to the overall market. Systematic risk is the risk that cannot be diversified away. BTC has a high beta which indicates that BTC’s price tends to be a lot more volatile than the market. Looking at the combined beta plot to compare BTC, ETH and XRP to SPY, we can see that BTC has the highest beta, and it is clearly more volatile than both ETH and SPY. If we want a diversified portfolio, we would need to add stocks that have less correlation and less volatility with the overall market. 
  * **Sharpe Ratio**- The Sharpe ratio shows the risk-return relationship and how much return to expect per unit of risk. SPY gives the highest return for every unit of risk assumed by the investor while ETH and XRP give a negative return for every unit of risk assumed. BTC has a positive return per unit of risk which makes it a good addition to a portfolio. However, for diversification purposes, it could be worth adding XRP even though it gives a negative return because of its lower correlation with SPY and ETH.

Part 2
* Create a portfolio simulation based on performance analysis
* Investor profile
  * Risk tolerance- medium
  * Age- 45
  * Time horizon- 20 years
  * Asset type- cryptocurrency
  * Investment amount- $300,000
* **Because the investor is optimistic about the market, create a long-position algorithm**
  * Because we want the trading algorithm to identify the trading signals that indicate opportunities to buy BTC stock, we need to identify the times when the short-window SMA is greater than the long-window SMA. When this happens, the price trend for BTC stock is moving upward in the short term and we want to own BTC stock during this time.

* **Analysis of the long-position algorithm**
  * With the overlay plot, we can identify the trading signals from the algorithm. Specifically, the green, upward-pointing arrows indicate the entry points, and the red, downward-pointing arrows indicate the exit points. 
  * This algorithm can recognize the crossover points of the long- and short-window SMAs. A trade was entered when the “SMA50” value crossed above the “SMA100” value, and the trade was exited when the “SMA50” value crossed below the “SMA100” value.
  * This trading strategy is called a long position because it focuses on first buying the stock, then holding it, and then selling it only when the short-term price trend turns lower. The investor makes a profit using the “buy low, sell high” strategy.
* **Back test the long-position algorithm** 
  * Now that we've built the algorithm, we can back test its profitability. Backtesting is a method that allows us to assess how well a strategy works retrospectively, using historical data to validate how accurately the strategy would have predicted the actual results.
* Set amount- $300,000
* Define back testing period- 1/1/18-12/31/21

* **Interpret Backtest Results from the Overlay Plot**
  * The Overlay Plot highlights the fact that the total value of the portfolio changed with each entry and exit of a 50-share position in BTC.
  * With an initial investment amount of $300,000, the final value of the trading algorithm resulted in a final portfolio value of $3,185,616.11 during the backtesting period. The portfolio fluctuated and reached a maximum value of $5,666,619.64 which is reflective of the high volatility of BTC and its prices.
  * Visualizing the potential upside and downside of an algorithm over time is just as important as measuring the profitability of any portfolio. In this case, overall trade performance was quite volatile so the high returns can be misleading for an investor. Therefore, an investment in BTC needs to be taken with caution due to the high assumption of risk. 
  * Based on the investor’s profile, the medium risk tolerance means they could add BTC to their portfolio but due to its volatility, it would be wise to invest an amount that they can afford to lose as well as adding other asset types for diversification purposes that can act as a hedge when the overall market is down. 
* **Calculate performance metrics**
  * **Annualized return**- represents the expected ROI over a time-period of one year. In this case, the dollar value of the portfolio should increase by about 66.99% each year.
  * **Cumulative returns**- represents the percentage gain or percentage loss for an investment across the entire investment. In this case, the dollar value of the portfolio increased by approximately 961.87% over the backtesting period. This may seem like an unusual number, but BTC had astronomical and slightly abnormal growth during this time-period.
  * **Annual volatility**- represents the standard deviation of the asset’s daily return values measured on an annualized basis. The annual volatility of the portfolio has a spread of about 71.58% surrounding the annualized return. This means that the portfolio might return as much as 138.57% (66.99% + 71.58%) or lose as much as 4.59% (66.99% - 71.58%) per year. The wide range between the maximum and minimum returns for BTC prove exactly how volatile it is.
  * **Sharpe Ratio**- measures an asset's outperformance as compared to the asset’s volatility where volatility is characterized by the standard deviation of its daily return values. In this case the Sharpe ratio is 0.936. 
  * **Sortino Ratio**- measures the downside volatility of the asset. Also, it’s best to compare it with the Sortino ratios of other portfolios. The Sortino ratio of our portfolio suggests a rate of about 1.399 for the risk-adjusted annual profitability compared to the annual downside risk. Since a Sortino ratio greater than 1.0 is acceptable, BTC would be a good addition to the portfolio considering its high volatility. 

* **Conclusion**
  * Overall, the portfolio performed very well during the backtesting period, but the high returns do not come without high risk. The investor has a medium risk tolerance and a medium time horizon so they can afford to take some risk that comes with investing in BTC, but it would not be prudent to place all their eggs in the BTC basket. My recommendation would be that an investment in BTC needs to be combined with other asset classes for diversification and hedging purposes.

### Third Notebook

* Build an algorithmic trading bot to create trading signals for BTC
* **Define trading strategy**
  * When actual returns are greater than or equal to 0, buy BTC long but if actual returns are less than 0, sell BTC short.
* Create trading signals for actual returns and strategy returns 
* **Use linear regression to predict the returns and analyze these returns**
  * Out of the three RMSE scores, the out-of-sample RMSE is the lowest with a value of 0.00826. Therefore, it is better to use out-of-sample data that the model hasn't seen before because it gives us a higher accuracy in our predictions and thus a better performance than in-sample data that the model was trained on. This makes sense if we factor in how BTC's price is constantly fluctuating making it both volatile and unpredictable.

* **Conclusion**
  * **Based on baseline performance and predicted returns, determine if you should buy or sell.**
    * Based on the baseline performance and predicted returns, I would advise the investor to buy BTC because the model shows that the predicted returns vs actual returns are not too different. This is reassuring to an investor who may question if BTC’s actual performance is indicative of future performance. 
  * **Adjust the algorithm’s input features to find the parameters that result in the best trading outcomes**
    * Adjusted the SMA input features, tried different window sizes but the out-of-sample RMSE remained the lowest of the three.
  * Overall, the investor is moderately risk tolerant, but BTC is very volatile so while the investor can afford to assume some risk, the portfolio has to include other asset classes for diversification and hedging purposes.

Sources:
1. Financial Data
https://finance.yahoo.com/quote/SPY?p=SPY&.tsrc=fin-srch 
https://finance.yahoo.com/quote/BTC-USD?p=BTC-USD&.tsrc=fin-srch 
https://finance.yahoo.com/quote/CUH22.NYM?p=CUH22.NYM
https://finance.yahoo.com/quote/XRP-USD?p=XRP-USD&.tsrc=fin-srch 
2. Crypto Prices Move More in Sync with Stocks, Posing New Risks 
https://blogs.imf.org/2022/01/11/crypto-prices-move-more-in-sync-with-stocks-posing-new-risks/ 
3.	Crypto and Stocks Look Increasingly Correlated. That Has Raised Risk Fears.
https://www.barrons.com/articles/crypto-and-stocks-look-increasingly-correlated-thats-raised-risk-fears-51642207952 
4.	Correlation Between Bitcoin and The Stock Markets Suggests a New Correction Could Be Coming
https://seekingalpha.com/article/4459110-correlation-between-bitcoin-and-stock-markets-suggests-new-correction-coming 



  
