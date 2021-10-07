---
description: >-
  The "Copy trades" panel allows you to automate trading between multiple
  accounts. Creating trading bots without programming to synchronise trading
  between accounts
---

# Copy Trading

One of the frequent questions from our community is: how to copy trades between multiple accounts? Such functionality can be very useful for proprietary trading companies and managers with multiple accounts who use Quantower as their trading tool. So we decided to meet this challenge and made a new dashboard - Copy Trading.

{% embed url="https://youtu.be/qIE2BxBvuJo" %}

* [How to open the "copy trades" panel and where it is located](copy-trading.md#how-to-open-the-copy-trades-panel-and-where-it-is-located). 
* [How the "copy trades" panel works and how it differs from the "Multiorder](copy-trading.md#how-the-copy-trades-panel-works-and-how-it-differs-from-the-multiorder)" 
  * [Top panel - Manager for managing the list of bots to copy trades](copy-trading.md#top-manager-for-managing-the-list-of-bots-to-copy-the-trade) 
  * [Bottom panel - Log of all actions ](copy-trading.md#bottom-log-of-all-activities)
* [Parent and child connections ](copy-trading.md#parent-and-child-connections)
* [How to create a trade copy bot ](copy-trading.md#creating-a-trade-copying-bot)
* [QTY copy mode - two modes for selecting trading volume on child accounts](copy-trading.md#qty-copy-mode-two-modes-for-selecting-the-amount-of-trading-in-subsidiary-accounts-connectors)
  * [Percentage - % trade from the balance in proportion to the parent account](copy-trading.md#percentage-mode-per-transaction-from-child-account-balance-per-transaction-from-parent-account-balance)
  * [Multiplier - multiplier, K from the trade of the parent account](copy-trading.md#multiplier-multiplier-k-of-the-parent-account-transaction)

### How to open the "copy trades" panel and where it is located.

The panel refers to the trading panels and can be found in the "trading panels" group in the main menu of the platform by clicking on the button in the top left corner.

![](../.gitbook/assets/image%20%28338%29.png)

### How the "copy trades" panel works and how it differs from the "Multiorder"

This panel allows you to fully automate trades between multi-accounts of the same connection according to a pre-created script. Unlike the **Multi-Order** panel, in this panel once you have created an algorithm for the bot, transactions will then be fully automatically copied without the trader's involvement into the specified account whenever a trade is made.

The trade copying bot will only work if each account is actively connected. If one of the child accounts is not connected in the **Connection Manager**, no trade copying will be made for that account.

{% hint style="danger" %}
You can only create a synchronisation of all trades between accounts of the same connection, exchange or broker. 

The Trade Copy panel supports the following connections: FTX, Binance, Binance Futures, Bitfinex, Rithmic, Bybit, BitMEX, Interactive Brokers
{% endhint %}

You can visually observe the complete synchronisation of trades by opening two charts at the same time. You can see the display of those trades on the chart that the bot creates automatically. Every movement of positions, SL/TP will automatically be duplicated on the second connection. Canceling an order on the parent account will also cancel the copied order on the child connection.

![](../.gitbook/assets/image%20%28336%29.png)

The "copy trades" panel is divided into two parts:

![](../.gitbook/assets/image%20%28341%29.png)

### Top - manager for managing the list of bots to copy the trade

This is the main bot control panel for copy trading. Here you can create new bots, stop and selectively start bots, and configure parameters for each individual bot to copy trades.

![](../.gitbook/assets/image%20%28335%29.png)

* **Bot name** - each bot can be given its own unique name; 
* **Parent account** \(connection\) - the name of the account where the trade will be made; 
* **Child account** \(connect\) - name of the account where all trades will be automatically copied to; 
* **Status** - informative field showing the bot's status. 
  * There are two statuses: "**Working**" and "**Stopped**"; 
* **Action** - active button for starting and stopping bots from the list; 
* **Settings** - the gear opens settings of the selected trading bot; 
* **Delete** - deletes the trading bot

### Bottom - Log of all activities

All actions that have been performed on active bots will be shown in a list in the form of an event log at the bottom of the panel. Including information messages such as "stop" and "start" of each bot. This way you can monitor every action or event performed by the bots without the trader's intervention.

![](../.gitbook/assets/image%20%28333%29.png)

To search for past events, if necessary, you can select over a period using the filter indicated in the image.

### Parent and child connections

![](../.gitbook/assets/connections-2021-10-07-13.57.25%20%281%29.png)

1. Parent account is the name of the connection \(exchange, broker\) 
2. Parent \(connection\) account - is an account on which the main trade will be executed 
3. Affiliated \(Connect\) account - is an account or several accounts, where all trades will be copied.

### Creating a trade copying bot

To create a new trading bot, click on the "+" button in the top left corner of the panel.

![](../.gitbook/assets/image%20%28340%29.png)

**Enter the bot's name** so that you can easily identify and locate it later in the list of trading bots.

Next you need to select a parent account \(connection\), which is the main account where the main trade will be done. The parent account is the name of the connection, the exchange, the broker where you have multiple accounts. And add a child account\(s\) - These are the accounts where all trades will be copied.

![](../.gitbook/assets/image%20%28344%29.png)

Each new line will add another account to which trades will be copied

![](../.gitbook/assets/image%20%28332%29.png)

### QTY copy mode - two modes for selecting the amount of trading in subsidiary accounts \(connectors\)

#### Percentage mode - % per transaction from child account balance = % per transaction from parent account balance

{% hint style="warning" %}
**-If this mode is selected the order size in % of the balance of the child accounts will be determined automatically.**

  
**-The % of the child account balance will be the same as the % of the parent account balance.**
{% endhint %}

![](../.gitbook/assets/image%20%28337%29.png)

**Example**: Parent account has a balance of $1,000 The order amount is $100, which is 10% of the balance. The child account has a balance of $2000. When you place an order on the parent account equal to $100 \(10% of the total balance\), an order will be placed automatically on the child account, and the same order will be placed for 10% of the total balance, or 200$.

#### Multiplier - multiplier, K of the parent account transaction

When selecting this trade copying mode, you need to enter K-factor from the trade of the parent account. Each trade on the child account will be opened in the amount of the trade of the parent account multiplied by the specified K-coefficient Multiplier.

![](../.gitbook/assets/image%20%28342%29.png)

![](../.gitbook/assets/image%20%28334%29.png)

**Example**: The parent account has an order in the amount of **100$, K- 0.5** At accommodation of the order on the parental account in size of 100$, the order will be automatically placed on the child account taking into account K- 0,5, i.e. **100$**_**0.5=50$** The sum of the warrant of **100$, K - 3** At accommodation of the order on the parental account in 100$, the order will be automatically placed on the child account taking into account K - 3, i.e. **100$**_**3=300**

{% hint style="info" %}
**If the child account does not have enough balance to make a trade with the specified K, an error message can be seen at the bottom of the panel, in the event log.**
{% endhint %}



