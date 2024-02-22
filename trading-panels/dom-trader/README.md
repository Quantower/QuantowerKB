---
description: >-
  DOM Trader panel shows the number of buy and sell orders placed at various
  price levels around the current price for a particular instrument
---

# DOM Trader

## General info about DOM Trader

**The Depth of Market** or **DOM Trader** panel shows the number of Buy and Sell orders placed at various price levels around the current price for a particular instrument (most often for futures). The more the number of orders is at a certain price level, the higher the interest in this level. The trading functionality of the panel allows you to quickly and efficiently place the required number of orders at the selected price, and also drag-and-drop, change or cancel them.

![General view of DOM Trader panel](../../.gitbook/assets/dom.png)

## Trading with DOM Trader

DOM Trader allows to send trading orders in three ways  — **Mouse Trading mode,** **Order Entry and Hotkeys.**

To place an order via Mouse Trading mode:

* Select an account and order restriction (TIF) in the order entry;
* Enter an order quantity;
* Left-click at a specific price in the left column will place a Buy Limit order (below the current market price);
* Left-click at specific prices in the right column will place a Sell Limit order (above the current market price). If you place the order below the current price it will be executed by market price;
* _To place a **Stop order**_ is necessary to press and hold down the _**Shift**_ key and click at the required price.

![Mouse trading mode in DOM Trader](<../../.gitbook/assets/DOM trader trading.gif>)

To place an order via Order Entry:

* Select an account and order restriction (TIF) in the order entry;
* Enter an order quantity;
* Click on the Bid, Ask or Market button to place your order;
* Set Stop Loss and Take Profit orders (Bracket Orders)
* Confirm your placement by first checking all the parameters.

![Placing a new position via Order Entry in DOM Trader](<../../.gitbook/assets/DOM trader trading OE.gif>)

{% embed url="https://www.youtube.com/watch?v=8a19rPvy2nQ" %}
DOM Trader panel in Quantower
{% endembed %}

### Position Bar settings

At the bottom of the DOM Trader is the Position Bar, which displays brief info about an open position on the current trading instrument  — the number of contracts, the average open price, current Profit/Loss and Liquidation price.

![Position Bar in DOM trading](../../.gitbook/assets/dom-position-bar1.png)

![Settings of position bar in DOM Trader panel](<../../.gitbook/assets/image (145).png>)

### Hotkeys

The quick change order amount buttons will help you to change the specified amount in one click, based on your trading strategy. **It is  starts from 1 to 9 numbers on keybord.** You can set by default any parameters you need for quick change of values. And the buttons can change not only the specified position volume, but also apply any (!!!) formulas to calculate the order volume. To set personal values for a quick change of the order, you need to go to the settings of the chart in the menu section "Order entry" and find the field "OE buttons"&#x20;

This tab is for configuring your keyboard shortcuts. Here you can configure the order size with one button and place it to the market. Cancel orders and many other useful functions.

![](<../../.gitbook/assets/image (146).png>)

## DOM Trader Columns

### Liquidity changes column (known as Pulling and Stacking)

Pulling and Stacking describe the summary of the Liquidity Order Book (LOB) for Bid and Ask Side separately. Stacking shows an increasing Volume in the Order Book for the Sell-Side (Ask) or Buy-Side (Bid) and reflects therefore a supportive intention for the price to move in the corresponding direction. Whereas the Pulling shows a decrease in the Volume in the Order Book and therefore a lack of interest.

### **Number of changes**

It shows how many times the values have changed at a particular price level (Bids x Asks) since the panel launched.

### **Cumulative changes**

It shows the total volume that changed at a specific price level since the panel launched.

#### _Why Number of Changes and Cumulative changes are important?_

The liquidity in the Depth of market is constantly changing due to very different types of reasons. The fast changes occurring simultaneously on the bid and ask sides are very difficult to track with the naked eye. It becomes even worse when you have over 10 levels.

This is the part where the number of changes and cumulative changes comes on handy. For a buy trade, you would expect to see an increasing number of changes combined to higher cumulative changes showing increasingly adding liquidity at a higher pace. Even better, would it be combined to a higher cumulative change on the ask side to the downside, showing participants eager pulling out the liquidity.

