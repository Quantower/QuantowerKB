---
description: >-
  Here are descriptions of the most common errors when working with or
  connecting to Binance Futures in Quantower platform
---

# Errors with Binance connection

### Event Log panel

All error messages you can see in the main menu in the Event panel 

![How to start Eventlog Panel](../../.gitbook/assets/image%20%28103%29.png)

![This is the Event log Panel](../../.gitbook/assets/image%20%28101%29.png)

## Possible errors with Binance Futures / Binance Spot connection

### There is an error "Api-key format invalid". 

Check that your ApiKey and ApiSecret are correct.

**"Invalid API Key"** error occurs for several reasons:

* a trader **did not enable Future Trading** in the personal account on the Binance website
* API Keys were not copied correctly.

{% hint style="info" %}
If you sure that everything is correct, please recreate the new keys and the problem is resolved. It's better to recreate it through another browser \(sometimes errors occur when creating through Google Chrome\).
{% endhint %}

![](../../.gitbook/assets/binance-futures-error.png)

To solve it, please check that your API Key has permissions for Futures trading. **Go to Binance official website &gt; Under your account select API management &gt; check & activate Futures Trading**

![](../../.gitbook/assets/image%20%2888%29.png)



### **"TimeStamp"** error occurs when the time on the Binance server does not match the time on the user's computer.

![Binance Futures error in Quantower - Timestamp for the request](../../.gitbook/assets/image%20%2889%29.png)

To solve it, please, go to **Windows Settings &gt; Time & Language &gt;** and click on **Sync Now** button**.**

![](../../.gitbook/assets/image%20%2892%29.png)

### 

### Error "Order's notional must be smaller than 5.0 \(unless you choose to reduce only\).

 

![](../../.gitbook/assets/image%20%28102%29.png)

As of February 24, 2021 the value of the perpetual futures order must be at least $5. If it is less than that, the order will be rejected. If you encounter this error, increase the volume you are placing so that it is greater than or equal to $5.

Example: When opening 0.001 ETH, the value of the order is greater than $5, so it will be placed. An order for 1 ANK is worth less than $5, so it will be rejected.

### "Margin is insufficient" error occurred when trying to place the order.

 Check your wallet balance. Make sure there is enough coin to make a trade. When trading USDS-M futures on Binance Futures, the wallet account must have USDT tokens.

### "Too many new orders" error has occurred.

 Limit on the number of orders set by the exchange was reached \(usually this is a limit on a particular instrument\). Maybe a limit on the instrument itself, or a limit on orders sent in a certain period \(for example, 10 orders per second - spam\).

### "Balance is insufficient" has occurred. Not enough funds on the balance.

 Check your wallet balance and make sure you have enough coins for the transaction.

### An error has occurred: "I can't close the position. Request was executed partially - the value of the open position is less than $5. 

This situation is connected with the rule of exchange Binance Futures about the minimum order volume from $5. You may close a position worth less than $5 using the following methods:

 1. Buy up to minimum volume and place limit order to close position. 

2. Place a pending stop order to close the position with a volume equal to the position. 

3. Set Stop-Loss or Take-Profit on the server-side.

 4. Close the order through Binance Futures website.

### Error - This listenKey does not exist

You are connecting to the exchange with one api on different platforms. each platform must have its own api. Rebuild the  new api key for our platform.

