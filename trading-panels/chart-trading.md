---
description: >-
  Here you can find out what are the possibilities for manual trading on
  Quantower directly from the chart.
---

# Chart Trading

Placing orders on the Quantower platform can be done using various panels, such as Order Entry, DOM Trader, and Chart. In this guide, we will show you how to place orders via the **Chart panel** using the sidebar trading toolbar and **mouse mode**.

***

## <mark style="color:blue;">**Chart Order Entry**</mark>

* [**How to open the chart trading toolbar**](chart-trading.md#how-to-open-quick-trade-toolbar)
* [**How to manage Quick Quantity buttons**](chart-trading.md#how-to-manage-quick-quantity-buttons)
* [**How to save order as the default**](chart-trading.md#how-to-save-order-as-default)
* [**How to create order templates and switch between them**](chart-trading.md#how-to-create-order-templates-and-switch-between-them)
* [**Slider to enter the volume of the position**](chart-trading.md#slider-to-enter-the-volume-of-the-position-in-dollars)
* [**How to set up Take Profit and Stop Loss orders**](chart-trading.md#how-to-set-up-profit-and-stop-orders)
* [**How to set up  several Take profit and Stop Loss orders for one position**](chart-trading.md#how-to-set-up-several-take-profit-and-stop-loss-orders-for-one-position)
* [**A set of buttons for quick order and position management**](chart-trading.md#a-set-of-buttons-for-quick-order-and-position-management)

## [Quick order entry](chart-trading.md#quick-order-entry)

* [**How to open Quick order entry**](chart-trading.md#how-to-open-quick-order-entry)

## [Mouse trading](chart-trading.md#mouse-trading)

* **Chart trading mode with the mouse**
* **Quick order placement through the chart area with a mouse.**
* **How to set up multiple limit orders**

## [Keyboard trading](chart-trading.md#keyboard-trading) (Hotkeys)

* **How to activate trading with hotkeys**

***

### How to open the chart trading toolbar

To activate the quick trading toolbar, click on the button in the upper right corner.

{% hint style="info" %}
The general view of Chart Trading Toolbar may differ depending on the available functions for each trade connection.\
This panel will be slightly different for crypto connections, as well as for those that do not allow to create Brackets or server-side Stop Loss / Take Profit orders. For more details about available order types for each connection, please check the [**Order Types section**](order-entry/order-types.md)
{% endhint %}

![Opening of sidebar Order Entry](../.gitbook/assets/chart-trading-toolbar.gif)

### How to manage Quick Quantity buttons

The Quick Quantity buttons are designed to help you adjust the specified volume with a single click based on your trading strategy. You can set default parameters that you frequently use and need to adjust the values quickly. Additionally, these buttons can apply any formula to calculate the order volume, allowing greater flexibility in order sizing. To personalize your Quick Quantity buttons, access the chart settings in the "[**Order Entry**](../analytics-panels/chart/chart-settings/order-entry.md)" menu section and locate the "<mark style="background-color:orange;">**Quick buttons**</mark>" field.

<figure><img src="../.gitbook/assets/Quick quantity buttons (1).gif" alt=""><figcaption><p>Editing of Quick quantity buttons</p></figcaption></figure>

You can set standard values of the order amount, which corresponds to your risks. This is very convenient for manual trading.

{% hint style="success" %}
Buttons can not only change to a given position but also apply any formulas.
{% endhint %}

![](../.gitbook/assets/vvod-baibit-ordera-kolvo.gif)

### How to save order as default

**Right-clicking** on the Order Entry sidebar -> Context menu -> <mark style="background-color:green;">**Set order as default**</mark>. This option will allow you to save the current default order settings for all symbols and all accounts.

<figure><img src="../.gitbook/assets/image (418).png" alt=""><figcaption><p>Save order parameters as default</p></figcaption></figure>

### **How to create order templates and switch between them**

To create order templates and switch between them, you can follow these steps:

* **Configure Order**: Set up the order according to your preferred parameters, such as quantity, TIF, and Breckets mode with SL/TP.
* **Save as Template**: Right-clicking on the Order Entry sidebar -> Context menu -> <mark style="background-color:green;">**Save order template**</mark>.
* **Name Your Template:** Choose a clear name that helps you remember the specifics of this template for future use.\
  As soon as you save the template, it will immediately be added to the dropdown menu list. You can create multiple templates with parameters tailored to different trading symbols or market conditions.

<figure><img src="../.gitbook/assets/save order as template (1).png" alt=""><figcaption><p>Save order template on the chart order entry sidebar</p></figcaption></figure>

* **Switching Between Templates**: When placing a new order, you can select any of your saved templates, and the order parameters will automatically adjust to match the template you chose.\
  Click on the necessary template and <mark style="background-color:green;">**Apply**</mark> it.

<figure><img src="../.gitbook/assets/applying the template.png" alt=""><figcaption><p>Applying the neccesary order template</p></figcaption></figure>

### Slider to enter the volume of the position in dollars

There are two ways to enter the quantity of a position&#x20;

* Entering an order in lots of a traded symbol or coin - this was described above
* Entering the amount of money planned to purchase that asset.

{% hint style="danger" %}
It is important to remember that if you use margin trading, the result is counted taking into account the leverage.
{% endhint %}

![](../.gitbook/assets/animaciya-5-.gif)

{% hint style="info" %}
This example is for crypto markets
{% endhint %}

For example, at the moment you have $82 on your account and 10 leverage is set. It means that you have $820 available balance for trade. This is what you can see in the example.

### How to set up Profit and Stop orders

Then you can set **automatic stop loss and profit** in pips. It's very convenient to set the lot size and protect it. Specify your values in the appropriate fields.

{% hint style="info" %}
Some brokers such as Binance do not allow stop orders for limit orders. (Until the position is NOT open) In this case, use limit orders of the opposite direction
{% endhint %}

![](<../.gitbook/assets/animaciya-3- (1).gif>)

* Use the Quick Trade toolbar&#x20;
* Set your values for stop loss or profit. You can also use any one parameter only.&#x20;
* Use the button to activate the trade with the mouse to set a limit order

{% hint style="warning" %}
If you execute an order at market, the specified stop parameters will retain their values and will be set immediately.
{% endhint %}

### How to set up Multiple Take profit and Stop Loss orders for one position

![](../.gitbook/assets/animaciya-4-.gif)

{% hint style="info" %}
This example is for connecting a CQG/AMP
{% endhint %}

* To set multiple stop orders for a single position, do the following Switch the bracket (stop) settings to multi mode&#x20;
* Enter data for setting the first limit orders and how many lots or coins should be closed&#x20;
* For the next stops, enter similar data on the next line.
* You can set orders in multiples of your total volume

### A set of buttons for quick order and position management

1. Next comes a block of buttons for **quickly placing an orde**r into the betting slots at the appropriate price.

![](<../.gitbook/assets/image (292).png>)

2\.  Next comes a large block of functions for managing the current position. You can delete or limit orders or stops. You can also reverse your position with one button or set it to no loss. These are very functional buttons, do not miss them.

***

## Quick order entry

### How to open Quick order entry

To access the quick trade toolbar, click the button in the upper right corner.

![](<../.gitbook/assets/animaciya-1- (1).gif>)

## Mouse trading

The Mouse Trading feature enables you to conveniently place limit and stop orders directly on the chart. To activate this feature, simply click on the mouse icon located in the upper right corner of the panel.

![](<../.gitbook/assets/animaciya-2- (1).gif>)

{% hint style="info" %}
You can place multiple orders in a row by holding down the **CTRL** key.
{% endhint %}

If the mouse position is **higher than the current price** then:

* left click of the mouse will set a **Buy Stop** order;
* right click of the mouse will set a **Sell Limit** order.

If the mouse position is **lower than the current price** then:

* left click of the mouse will set a **Buy Limit** order;
* right click of the mouse will set a **Sell Stop** order.

## Keyboard trading

### How to activate trading with Hotkeys

To enable trading via hotkeys, simply click on the **keyboard icon** located in the upper right corner of the chart panel. This will activate the feature, allowing you to conveniently execute trades using your keyboard.

![](<../.gitbook/assets/image (293).png>)
