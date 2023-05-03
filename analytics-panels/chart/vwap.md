---
description: >-
  Volume Weighted Average Price shows a fair price of an asset and based on a
  trading volume.
---

# VWAP | Volume Weighted Average Price

**Volume Weighted Average Price** known as **VWAP** is a “benchmark” price of an asset for any period of the trading day or session. Average price is weighted by volume for evaluating the overpaying or underpaying of the current price relative to the VWAP price.

![](../../.gitbook/assets/multiple-vwap.png)

The indicator is calculated for any period of time according to the following algorithm:

* the average price (AP) is calculated for each bar or candle. The calculation is made for each price change for the current candle.  AP = (H+L+C)/3
* the average price is multiplied by the volume passed in the current candlestick or bar. For example, in real-time new trade will increase the volume and thus weigh the price. Thus, for each price or volume change we will get value AP \* V.
* the above values are summed up and divided by the total volume for the specified period.&#x20;

&#x20;      <mark style="background-color:green;">**VWAP = (Sum of Average Price \* Traded Volume) / Cumulative Volume**</mark>

## **How to add VWAP to the chart?**

The VWAP indicator is located on the Volume Analysis toolbar. When you click on it, a menu with basic settings and an indicator activation / deactivation switch will appear.

![VWAP Indicator is placed on Volume Analysis toolbar](../../.gitbook/assets/vwap-activation.png)

The quick settings menu contains:

* **Enabled** switch shows or hides the VWAP indicator on the chart
* **Base period and Value** — defines the number of bars (duration) on which VWAP will be calculated

### Advanced indicator settings

By clicking on the "**Gear"** icon, additional settings will open.&#x20;

<figure><img src="../../.gitbook/assets/image (3) (2).png" alt=""><figcaption><p>Additional settings for VWAP Indicator</p></figcaption></figure>

<mark style="color:blue;background-color:blue;">**1. Switch between different VWAPs**</mark> and set the settings for each of them.

Quantower platform provides 5 separate VWAPs, that can be placed simultaneously on a single chart.

<mark style="color:blue;background-color:blue;">**2.**</mark> <mark style="background-color:blue;">Set the</mark> <mark style="color:blue;background-color:blue;">**Main Settings**</mark> for the VWAP line:

* **Data type** — sets the type of data for the VWAP calculation: **Ticks** or **Current TF.**\
  &#x20;  **Ticks** will use tick data for VWAP calculation and will take much more time for the data loading.\
  &#x20;  **Current TF** will use Bar data from the current selected Timeframe of your chart. It will use Price type data and multiply it by Total Bar Volume.
* **Price Type** — select the desired price to be used in the calculation for the Current TF data type (Open, High, Low, Close, HL/2, HLC/3, OHLC/4)
* **Period and Value** — defines the number of bars (duration) on which VWAP will be calculated
* **VWAP line** — visual settings for VWAP itself (line style, color, thickness)
* **Sessions template** — setting allows you to select the trading session within which VWAP will be calculated. You can select predefined sessions from the list, or add your own custom sessions. For more information about creating and configuring a session, follow the instructions in the [<mark style="background-color:blue;">**Session manager**</mark>](../../miscellaneous-panels/sessions-manager.md) section.

3. <mark style="color:blue;background-color:blue;">**Forward Extensions**</mark> (type and number)

<figure><img src="../../.gitbook/assets/image (1) (2) (3).png" alt=""><figcaption></figcaption></figure>

<mark style="color:blue;background-color:blue;">**4. Standard Deviation Bands**</mark>

When the parameter is active, the standard deviation lines up and down from VWAP will be additionally calculated on the chart. Specify the number of standard deviations in the _**"Value"**_ field and colors

<mark style="color:blue;background-color:blue;">**5. Maximum Permissible Deviation (MPD)**</mark>

MPD is similar to the standard deviation but is calculated as (VWAP period high - VWAP period low)/2.

## How to use VWAP in trading?

VWAP has numerous application in the trading world. It is helpful for both institutional investors and retail intraday traders. Below are some well known applications of VWAP:

* It helps in Buying low and Selling High. If the price is below VWAP, it is considered as undervalued, while price above VWAP is considered as overvalued.
* Crossing of prices above/below VWAP line in chart indicates momentum shift or change of trend.
* VWAP is also used as a trading benchmark by institutional investors who are not worried about the timing of the trade, but who are concerned about the adverse impact of their trades on the price of the security.
* VWAP serves as a reference point for prices for one day. As such, it is best suited for intraday analysis**.** Chartists can compare current prices with the VWAP values to determine the intraday trend.
* VWAP indicator can be used as a dynamic support/resistance line during sideways market.

### #1 Return to 1 Hour VWAP

For intraday trading we have found that it is possible to trade the return of the price to VWAP on small timeframes. For example, let's consider ES (e-mini S\&P500) futures on 5-minute chart with an hourly VWAP.&#x20;

![Trading with VWAP in Quantower platform](../../.gitbook/assets/vwap-trading.png)

An important point in this tactic is that the distance between the VWAP value and the closing price should be significant.

![The distance between the VWAP value and the closing price should be significant ](../../.gitbook/assets/vwap-trading1.png)

### #2 Trading with STD bands

**Standard deviations** are an objective statistical measurement that quantify variance in a data set, with a small value indicating that most data points are close to the average and a larger value indicating a wider spread.&#x20;

By applying this tool to trading with VWAP serving as our average, we can plot these deviations as bands to create a visible unit of measurement to characterize market movement and gauge volatility

Deviation bands are plotted continuously alongside VWAP, automatically adjusting as we receive more data. They typically start off small and expand as price begins to break away from the market's average, but lacking any notable volume or volatility they remain stable throughout the day.

![](../../.gitbook/assets/stds-and-vwap.png)
