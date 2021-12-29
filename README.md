# technical_indicators_cryptos
Using technical indicators to find optimal trading strategies to deploy onto trading bot. 

<pre>   
In the Jup Notebook you will find implementations of different indicators, 
and a backtest for each strategy sperately by itself. 
Also a graph generated to visualize the price along with each strategy. 
Then another backtest of MACD (9int) and Bolinger Band (10int) 
but this time optamized to inlude a precusor to candlestick identification.  
I didn't have a lot of luck using specific candlesticks in conguntuire with the indicators,
(used TA-LIB library to identify the candlesticks, will replace it with my own implementation later)
so instead I just used, 
if previous 4 candles went up relative to each other and current candle did not as a replacement.

When a strategy is in place, a low stoploss and takeprofit can cause excessive triggers that lack quality,
so I set those at the maximum I'm willing to loose and an optimal amount I would like to make,
that trigger only as a failsafe. Relying primairly on the technical indicators and candlestick identification precusor. 

Backtested on my implementation of a backtest the profit margin was satisfactory. 
And on Freqtrade's backtest in a 1 year timeframe, the results averaged 100% return,
and for MACD9fall, depending on the whitelist pairs to trade, 
as high as 1000%, but that is an optimistic number that should not be expected to be norm.
Let's go with 100% over the year as the norm. 
Inside the results directory you will find the output from the Freqtrade backtests.

Freqtrade is an opensource trading bot for cryptos and uses the ccxt library so you can connect to any crypto exchange.
It has backtesting functionality which gives a lot of details which can be used to further optimize a strategy,
along with a dry run function which lets you run the bot live but not make real trades. 
You can connect the Freqtrade bot to a telegram account to recieve notifications and control the bot. 
https://www.freqtrade.io/en/stable/

Feel free to use my trading strategy, which you will find in following directory. 
technical_indicators_cryptos/Freqtrade/ft_userdata/user_data/strategies/

Please backtest and dryrun all strategies for a while before using live. 
For those that benefit your welcome haha and for those that loose I am sorry.
Note again that a low stoploss and low takeprofit/roi can interfere with the trading strategy,
and should only be set as a failsafe. Currenty set to 50% stoploss and 10% takeprofit. 
Drawdown is between 8% and 50% depending on the stock selection for MACD9fall.
Drawdown is too high to be considered safe for BB10fall. 

And if you could spare some change haha
ETH
0x38f96AD454b2F9d90eBF725062123a136ddfbD80


</pre>   

