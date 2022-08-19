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
* _To place a **Stop order**_ is necessary to press and hold down the _**Shift**_ key and click at a required price.

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

## DOM Trader settings

Additional settings of the DOM Trader allow you to customize the general view for convenient display of data and the panel in general. To open DOM Trader settings, click on the Menu button on the left upper corner and select Settings item.

The general view of DOM Trader settings menu has the following subsections. Let's take a closer look at them:

* **View**
* **Columns**
* **Order Entry**
* **Positions Bar**
* **Hotkeys**

### View settings

![](<../../.gitbook/assets/image (147).png>)

* **Custom title.** You can rename the DOM Trader panel as you wish.
* **Refresh rate (ms)** controls the rate at which market data is updated. This determines how often the platform processes changes in depth of market. With a value of 1, all changes to the level2 data will be processed immediately. We recommend using value 50.
* **Use custom tick size.** This setting changes the price step by aggregating the level2 data.&#x20;

There are two ways to change the aggregation of ticks in the DOM trader:

1. By holding CTRL button and spinning the mouse wheel
2. Set the parameter manually in the panel's settings

![Applying of custom tick size by holding CTRL button](<../../.gitbook/assets/DOM Trader aggregation of ticks.gif>)

![Applying of custom tick size via DOM trader settings](<../../.gitbook/assets/image (356).png>)

* **Short price format**
* **Split size columns.** A mode that allows you to place Ask and Bid volume on one or different sides of the Size column;
* **Custom session.** This item is for selecting trading sessions for Volume Analysis data primarily.
* **Full-size cells.** Color scheme for Size column;
* **Show order entry.** This option shows/hides an Order Entry on the panel for quick order placement;
* **Collapse spread.** Hide or show the spread between the current Bid / Ask prices on the price ladder;
* **Show day map.** Display the upper horizontal scale, which shows the current price position relative to the High and Low of the day;
* **Show toolbar.**  This option shows/hides the top toolbar with the trading symbol and expands the "useful" area of the panel. It is recommended to use this option with the symbol link.
* **Show Level 1 bar.** Shows/hides the header pane, which contains Level 1 market data for the selected instrument.

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

