# Fin-tech-ETF-

First, choose the major ETFs in the index, fix income and commodity market. The linear regression over the open price of the last half year is used to decide the current trend. The trading signals are triggered by the following rules

1. Set a threshold to the slope of the regression line, trade if the slope exceeds the threshold

2. Uptrend ( slope > 0 and slope > threshold):  

Today's open cross the regression line upward and the equity is not invested  - long
The equity has already been invested(long) and today's open greater than 95% upper Bollinger band - liquidate 
3. Downtrend (slope < 0 and slope < - threshold)

Today's open cross below the regression line and the equity is not invested  - short
The equity has already been invested(short) and today's open lower than 95% lower Bollinger band - liquidate
4. If the equity has already been invested

long but the slope turns down, liquidate
short but the slope turns upward, liquidate
 5. Trailing stop

The stoploss percentage is the absolute value of slope over the lookback period, the price is the historical mean over the last three days
