---
description: >-
  Anchored VWAP or Custom VWAP tool allows drawing a VWAP line within a
  specified range or from a specified starting point.
---

# Anchored VWAP

Specify the start point on the chart and anchored VWAP will draw a line to the current moment. Also, you can specify the endpoint for the line, set Standard Deviation and Maximum Permissible Deviation.

![](../../.gitbook/assets/anchored-vwap.gif)

By clicking on the "**Gear"** icon, you can customize the settings of the selected VWAP

![Settings of Custom VWAP \(Anchored VWAP\)](../../.gitbook/assets/image%20%28105%29.png)

* **VWAP line** — set the main line type, its thickness and color 
* **Data type** — set the data for VWAP calculation: **Ticks** or **Current TF.    Ticks** will use tick data for VWAP calculation and will take much more time for loading    **Current TF** will use Bar data from the current selected Timeframe of your chart. It will use Price type data and multiple it to Bar Volume. 
* **Price Type** — select the price for the Current TF data type \(Open, High, Low, Close, HL/2, HLC/3, OHLC/4\)

![](../../.gitbook/assets/image%20%28106%29.png)

* **Standard Deviation Bands**. When the parameter is active, the standard deviation lines up and down from VWAP will be additionally calculated on the chart. Specify the number of standard deviations in the _**"Value"**_ field and colors
* **Maximum Permissible Deviation \(MPD\).** MPD is similar to the standard deviation but is calculated as \(VWAP period high - VWAP period low\)/2.
* **Points coordinates** — defines the starting point for custom VWAP
* **Visible on specified timeframes** — this setting allows you to specify on which timeframes VWAP will be displayed.

