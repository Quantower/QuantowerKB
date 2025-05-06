---
description: Multiple ways to enter orders on the CQG connection
---

# Order Entry for CQG

### [Quick order entry](order-entry-for-cqg.md#quick-order-entry)

### [Keyboard trading](order-entry-for-cqg.md#keyboard-trading)

### [How to place an OCO order](order-entry-for-cqg.md#how-to-place-an-oco-order)

## **General view of the Order Entry panel with CQG connection**

![General view of Order Entry panel with CQG connection](<../../.gitbook/assets/image (304).png>)

The entire panel is conventionally divided into several **zones**:

* choice of trading instrument and trading account;
* setting the required order type, TIF condition, order quantity, and the order side (Buy or Sell);
* setting of the order price, stop loss and take profit prices;
* order placing strategy for advanced trading algorithms
* information on current Ask and Bid prices, spread size, as well as an order placement button

## CQG OrderTypes, Time in Force (TIF), Algorithmic in Quantower

CQG provides various order types for trading via the Order Entry panel:

* Market order
* Limit order
* Stop order
* Stop limit order

![Order types in Quantower for CQG connection](<../../.gitbook/assets/image (218).png>)

**Time-in-force (TIF)** instructions define the length of time over which an order will continue working before it is canceled. CQG provides various TIFs:

![Time in Force (TIFs) for CQG connection](<../../.gitbook/assets/image (217).png>)

* **GTC (Good till canceled)** — orders will remain working until they are canceled by trader or the contract expires;
* **FOK (or Fill or Kill)** —  order will be canceled if it is not executed in the entire volume as soon as it becomes available;
* **IOC (Immediate or cancel)** — requires that any portion of an order that is not filled as soon as it becomes available in the market is canceled;
* **DAY** — order will be canceled if it is not executed within the current trading day;
* **GTD (Good till date)** — order will remain working within the system and in the marketplace, until it executes or until the close of the market on the date specified.
* **GTT (Good till time)** — order that remains open until a specified time. At that time, any unfilled lots are canceled.
* **FAK** (**Fill and Kill)** — orders require that any remaining quantity after a partial fill be canceled.
* **ATC (At the Close Order)** — order to buy or sell a stock at the closing price. One of the benefits of this type of order is that it can be placed prior to the actual end of the trading day requested. This would be the opposite of an at-the-open order.
* **ATO (At-The-Open Order)** — order to buy or sell a stock at the opening price. ATO order is allowed during pre-open sessions (morning and afternoon) or even the night before.

Algorithmic orders for CQG

### **How to set TP (take profit) and SL (stop loss)**

To set a bracket order with Sl and Tp, follow these steps as shown in the picture below:&#x20;

* Set the necessary lot to enter&#x20;
* Set Sl in pips&#x20;
* Set Tp in pips

If one of the orders Sl or Tp is executed, the opposite order will be automatically deleted.

### How to set up multiple TP and SL orders for one position

![](<../../.gitbook/assets/animaciya-1- (2).gif>)

Тo set multiple stop orders or take profit for a single position, you need to switch the **Brackets** to the **Multiple mode**:

* Set the quantity of the initial position.&#x20;
* For the next stops, enter similar data on the next line.
* You can set orders in multiples of your total volume

## **How to place an order from the Chart trading sidebar**

The general view of the Chart trading sidebar for AMP/CQG connection looks like the following and is divided into the following categories:&#x20;

* Account and symbol selection&#x20;
* Order volume selection, TIF, algorithmic settings
* Brackets Mode for Stop Loss and Take Profit.&#x20;
* Order placement parameters (strategy)
* Quick buttons for managing existed orders and positions

![Sidebar Order Entry on the chart ](<../../.gitbook/assets/image (314).png>)

### **Quick order quantity buttons**

To set an order, you need to specify the volume in lots according to the chosen symbol. You can do this in several ways.&#x20;

* Specify the volume directly in the quantyti field&#x20;
* Preset your normal trading volume in lots.

![](<../../.gitbook/assets/image (309).png>)

### Quick change order amount buttons&#x20;

The quick change order amount buttons will help you change the specified volume in one click, based on your trading strategy. You can set by default any parameters that you need to quickly change the values. Moreover, the buttons can change not only the specified position volume, but also apply any (!!!) formulas to calculate the order volume. To set your personal values for a quick change of the order, you need to go to the settings of the chart in the menu section "Order entry" and find the field "OE buttons"

![](<../../.gitbook/assets/animaciya-2- (2).gif>)

You can set standard values of the order amount, which corresponds to your risks. This is very convenient for manual trading.

{% hint style="success" %}
Buttons can change not only to a given amount of position, but also apply any formulas
{% endhint %}

### How to set up Profit and Stop orders&#x20;

Then you can set **automatic stop loss and profit** in pips. It's very convenient to set the lot size and protect it. Specify your values in the appropriate fields.

* Use the Qquick Ttrade toolbar&#x20;
* Set your values for stop loss or profit. You can also use any one parameter only.&#x20;
* Execute an order on the market

![](<../../.gitbook/assets/animaciya-5- (1).gif>)

### How to set up  **several** Profit and Stop orders foe one position

![](<../../.gitbook/assets/animaciya-6- (1).gif>)



To set multiple **Stop loss and Take profit** **orders** for a single position, do the following :

* Press the multi-mode button
* Enter data for setting the first limit orders and how many lots should be
* For the next Stop loss orders, enter similar data on the next line.
* Execute an order on the market

### **Quickly placing orde**r buttons

1. Next comes a block of buttons for **quickly placing an orde**r

![](<../../.gitbook/assets/image (310).png>)

2\.  Next comes a large block of functions for managing the current position. You can cancel or limit orders or stops. You can also reverse your position with one button or set it to break even. These are very functional buttons, do not miss them.

## Mouse trading

### How to set up Profit and Stop orders for limit order

You can set **automatic stop loss and profit** in pips. It's very convenient to set the lot size and protect it. Specify your values in the appropriate fields.

![](<../../.gitbook/assets/animaciya-3- (1).gif>)

* Use the Quick trade toolbar&#x20;
* Set your values for stop loss and profit. You can also use any one parameter only.&#x20;
* Use the **mouse trading button** to activate the trade with the mouse to set a limit order

{% hint style="warning" %}
If you execute an order at market, the specified stop parameters will keep their values and will be set immediately.
{% endhint %}

### How to set up several Profit and Stop orders for the limit order

![](../../.gitbook/assets/animaciya-4-.gif)

To set multiple **Stop loss and Take profit** **orders** for a single position, do the following :

* Press the multi-mode button
* Enter data for setting the first limit orders and how many lots should be
* For the next Stop loss orders, enter similar data on the next line.
* You can set orders in multiples of your total volume.

### **How to set up many limit orders**

![](<../../.gitbook/assets/animaciya-4- (2).gif>)

{% hint style="warning" %}
To place several orders in a row hold down CTRL
{% endhint %}

If the mouse position i**s higher than the current price** then&#x20;

* right click of the mouse will set a **Sell limit order**&#x20;
* left click of the mouse will set a **Buy stop marke**t order

If position of the mouse is **under the current price** then

* right click of the mouse will set **Sell stop market**&#x20;
* left click of the mouse will set **Buy limit order**



## Quick order entry

### How to open Quick order entry

To access the quick trade toolbar, click the button in the upper right corner. If you don't see this button, turn it on in the[ settings](../../analytics-panels/chart/chart-settings.md)

![](<../../.gitbook/assets/animaciya-8- (1).gif>)

### How to set volume quantity

{% hint style="warning" %}
Note that in order to make a transaction from the Quick order entry panel, you must enter the lot volume. And this volume does not coincide with the Quick trading panel&#x20;
{% endhint %}

## Keyboard trading

### How to activate trading with hot keys

To access the quick trade toolbar, click the button in the upper right corner. If you don't see this button, turn it on in the[ settings](../../analytics-panels/chart/chart-settings.md)

![](<../../.gitbook/assets/image (307).png>)

You can set your own values for the hot buttons in the chart settings

## How to place an OCO order

{% embed url="https://youtu.be/GrJBUYSxvHE" %}

