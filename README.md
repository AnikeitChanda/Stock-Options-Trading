# Stock-Options-Trading
Made for the Computational Investment Group at the University of Buffalo

# Descriptions
`Option_Component.ipynb` utilizes the TDAmeritrade API to get option chains for a particular stock.
These option chains are passed through a model to filter them based on custom parameters in order to generate recommendations for the user to advise them on which stock options to invest in.

`Deep-ITM-Call-Options-Strategy.ipynb` utilizes the TDAmeritrade API to get CALL option chains for a particular stock.
In particular the call option chains are scanned to find deep ITM option recommendations that can be bought and excercised at a later time for future profit or to recuperate losses.

`Stock-Price-&-PL-Prediction.ipynb` is used to give the user a strategy recommendation for a particular option i.e whether to buy/sell a particular option contract. This is done by first running a Monte Carlo simulation of GBM of the stock to produce a probability distribution describing the probability of a stock reaching a certain price on a given day in the future. This distribution is then transformed to a CDF and then discretized. The user is then able to introduce a bias to skew the distribution on how bullish/bearish they think the market is. This final distribution is used to compute an expected profit/loss value using different strategies for all the option contracts(received from TDAmeritrade) on a given day in the future, in order to give the user a strategy recommendation. 
