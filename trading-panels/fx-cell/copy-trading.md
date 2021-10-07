---
description: >-
  The "Copy trades" panel allows you to automate trading between multiple
  accounts. Creating trading bots without programming to synchronise trading
  between accounts
---

# Copy Trading

One of the frequent questions from our community is: how to copy trades between multiple accounts? Such functionality can be very useful for proprietary trading companies and managers with multiple accounts who use Quantower as their trading tool. So we decided to meet this challenge and made a new dashboard - Copy Trading.

{% embed url="https://youtu.be/qIE2BxBvuJo" %}

* How to open the "copy trades" panel and where it is located. 
* How the "copy trades" panel works and how it differs from the "Multiorder" 
  * panel Top - Manager for managing the list of bots to copy trades 
  * Bottom - Log of all actions 
* Parent and child connections 
* How to create a trade copy bot 
* QTY copy mode - two modes for selecting trading volume on child accounts
  * Percentage - % trade from the balance in proportion to the parent account
  * Multiplier - multiplier, K from the trade of the parent account

### How to open the "copy trades" panel and where it is located.

The panel refers to the trading panels and can be found in the "trading panels" group in the main menu of the platform by clicking on the button in the top left corner.

![](../../.gitbook/assets/image%20%28334%29.png)

### How the "copy trades" panel works and how it differs from the "Multiorder"

This panel allows you to fully automate trades between multi-accounts of the same connection according to a pre-created script. Unlike the **Multi-Order** panel, in this panel once you have created an algorithm for the bot, transactions will then be fully automatically copied without the trader's involvement into the specified account whenever a trade is made.

The trade copying bot will only work if each account is actively connected. If one of the child accounts is not connected in the **Connection Manager**, no trade copying will be made for that account.

{% hint style="danger" %}
You can only create a synchronisation of all trades between accounts of the same connection, exchange or broker. 

The Trade Copy panel supports the following connections: FTX, Binance, Binance Futures, Bitfinex, Rithmic, Bybit, BitMEX, Interactive Brokers
{% endhint %}

You can visually observe the complete synchronisation of trades by opening two charts at the same time. You can see the display of those trades on the chart that the bot creates automatically. Every movement of positions, SL/TP will automatically be duplicated on the second connection. Canceling an order on the parent account will also cancel the copied order on the child connection.

![](../../.gitbook/assets/image%20%28333%29.png)

The "copy trades" panel is divided into two parts:

![](../../.gitbook/assets/image%20%28335%29.png)

### Top - manager for managing the list of bots to copy the trade

This is the main bot control panel for copy trading. Here you can create new bots, stop and selectively start bots, and configure parameters for each individual bot to copy trades.

![](../../.gitbook/assets/image%20%28332%29.png)

* **Bot name** - each bot can be given its own unique name; 
* **Parent account** \(connection\) - the name of the account where the trade will be made; 
* **Child account** \(connect\) - name of the account where all trades will be automatically copied to; 
* **Status** - informative field showing the bot's status. 
  * There are two statuses: "**Working**" and "**Stopped**"; 
* **Action** - active button for starting and stopping bots from the list; 
* **Settings** - the gear opens settings of the selected trading bot; 
* **Delete** - deletes the trading bot
* 


