# Errors with Interactive Brokers

### Data Limitations

Interactive Brokers places the following limitations on real-time and historical data accessible to 3rd party applications

* **Pacing Violations** – TWS limits the number of requests for data. If too many requests for data occur in a short period of time, you may see error messages indicating “Pacing Violation”. If this happens you may need to wait a few minutes before trying to load data again. 
* **Real-Time Quotes** – TWS does impose limits on the number of active tickers \(typically around 100\). Additional booster packs can be purchased from IB to work around this issue: [Booster Packs](https://www.interactivebrokers.com/en/index.php?f=14193). 
* **Delayed Data Not Supported** – TWS does not provide access to delayed historical data and quotes. 

### The most common Errors & Issues

Here is the list of the most common errors and issues with IB connection:

* **Error "No market data permissions for NYSE STK"**

## Error "No market data permissions for NYSE STK"

In order to receive market data for charts and quote lines within Quantower, it is necessary you are subscribed to the exchange that the Symbol is listed on. If market data is not subscribed, you will see error messages similar to the following:

![](../../.gitbook/assets/image%20%28317%29.png)

In this case you will need to **subscribe to market data** from the particular exchanges mentioned in these messages. After this is done, **restart Trader Workstation platform**. Quantower will establish a new connection and you should then receive market data.

Please check our guide on [**How to subscribe to IB's Market Data**](./#how-to-subscribe-to-ib-market-data).







