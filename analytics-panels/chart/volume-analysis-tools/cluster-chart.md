---
description: >-
  Cluster or Footprint chart is a professional analytical tool that shows OHLC
  prices and trading volume on a single chart.
---

# Cluster chart

{% embed url="https://youtu.be/xnUxEjMrKKM" %}

### What is a Cluster chart?

**Cluster chart**, known as a Footprint chart in other trading platforms, is an advanced chart type that shows a comprehensive view of the candle chart. It allows to look inside the price and see all market actions. Cluster chart combines several important characteristics like time, OHLC prices, trading volume, number of buy and sell trades.

Using this information, a trader can evaluate:

* trading volume, which executed for each price
* zones of maximum volume accumulation
* zones of high trading interest (the maximum number of trades)
* the number of buyers and sellers at each price level

![Cluster chart with Imbalance view ](../../../.gitbook/assets/cluster-chart.png)

### How to enable cluster chart?

To activate a cluster chart, you first need to enable the Volume Analysis Toolbar. Click the "_<mark style="background-color:green;">**Magnifier**</mark>_" icon in the upper right corner of the chart panel.&#x20;

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Activate the Volume Analysis Toolbar</p></figcaption></figure>

This will display a toolbar with Volume Analysis tools at the bottom of the chart, including _**Cluster,**_ [_**Step Profile, Left Profile, Right Profile**_](volume-profiles.md)_**,**_ [_**Time Statistics**_](time-statistics.md)_**,**_ [_**Time Histogram**_](time-histogram.md)_**,**_ [_**Historical Time & Sales**_](historical-time-and-sales.md)_**, and**_ [_**Custom Volume Profile**_](volume-profiles.md#custom-volume-profile).

1. Click on the **Cluster** tool to Enable it
2. Select the **Type** of visualization (Single, Double, or Imbalance view)
3. Select the **Data type**(s) (you can choose one or two different data types at once)
4. Customize Data **Visualization** — Cluster or Histogram
5. Choose your preferred **Coloring mode** (by delta, by volume, by trades, etc.)
6. For more detailed chart customization, use the advanced settings (gear icon).

<figure><img src="../../../.gitbook/assets/activation of cluster chart .gif" alt=""><figcaption><p>Here is how you can activate Cluster chart in Quantower platform</p></figcaption></figure>

{% hint style="info" %}
For more efficient analysis with a cluster chart, you can display two different data types on one bar at once.
{% endhint %}

### Types of Cluster Chart in Quantower

Quantower provides 3 types of cluster charts for better data visualization:

<figure><img src="../../../.gitbook/assets/image (428).png" alt=""><figcaption><p>Types of cluster charts (footprint) in Quantower</p></figcaption></figure>

* **Single cluster** shows only one data type per bar. The list of main [**Data types**](cluster-chart.md#data-types-for-cluster-chart) you will find below

![Cluster chart in Quantower with single type visualization](<../../../.gitbook/assets/image (357) (1) (1) (1).png>)

* **Double cluster** allows you to select two data types that will be shown in each bar. For example, you can select Volume for the first data type and Delta for the second data type.

![Cluster chart in Quantower with a double type visualization](<../../../.gitbook/assets/image (361) (1).png>)

* **Imbalance** in the footprint chart highlights the price levels where a buy trade volume is excess over a sell trade volume. Diagonal Bid/Ask imbalance displays aggressive buy market orders lifting the offer and aggressive sell market orders hitting the bid.

![Cluster chart in Quantower with an Imbalance view](<../../../.gitbook/assets/image (359) (1) (1) (1).png>)

{% hint style="info" %}
In the Imbalance mode, by default, the **Sell volume (Bid)** is selected on the left side of the bar, and the **Buy volume (Ask)** on the right side. Other data types cannot be selected in this mode.
{% endhint %}

### General settings of cluster chart

Cluster chart has various settings allowing to display of volume data from different sides. For example, you can choose different types of data for each bar, as well as configure colors, which will simplify the perception and analysis of volumes, trades, etc.

![Select different data types for Cluster chart](../../../.gitbook/assets/cluster-data-type.gif)

### Data Types for Cluster Chart

* **Trades** — it's the number of contracts (trades) that are executed at each price level.
* **Buy (or Sell) trades** — it's the number of Buy (or Sell) trades that are executed at each price level.
* **Volume** — the total size of all positions that are executed at each price level or price range.
* **Buy (or Sell) Volume** — the total size of all Buy (or sell) positions that are executed at each price level or price range.
* **Buy (or Sell) Volume, %** — shows how many percent of the total volume relates to Buy (or Sell) trades
* **Delta and Delta %** — shows the difference in traded Volume between Buyers and Sellers. It allows evaluating who controls the price on the market at a given time. \
  Delta % = Delta / Volume \* 100
* **Average size** — the average volume of the position that was executed at a certain price or price range.
* **Average Buy size** — the average volume of a Buy position that was executed at a specific price or price range.
* **Average Sell size** — the average volume of a Sell position that was executed at a specific price or price range.
* **Max one trade volume (value and %)** — shows the maximum volume of a single trade that has been executed at a certain price or price range (depending on the Custom Step (ticks) setting).
* **Filtered volume (value and %)** — this parameter displays volumes that exceed the size specified in the filter. If the volume size is smaller than the one specified in the filter, then the values will be zero.
* **Buy (or Sell) filtered volume** — the parameter displays Buy (or Sell) volumes that exceed the size specified in the filter.

### How to set the filtered volume?

For all volume analysis tools, there are general settings that allow you to set Filtered volume, and configure the step for aggregating volume data. On highly liquidity assets like Bitcoin or futures on the S\&P500, the trading volume for a trading session is large. Set the minimum volume values that will be displayed on the chart. This will allow you to focus on significant price levels and more clearly see zones of support/resistance.

{% hint style="info" %}
Each instrument has individual settings for the filtered volume depending on liquidity.
{% endhint %}

![Filtered volume in general settings of Volume Analysis](../../../.gitbook/assets/filtered-volume.png)

Select **Filtered Volume** as the data type in clusters to display them on the chart. All values that are less than the filtered volume are presented as zeros.

![](<../../../.gitbook/assets/image (79).png>)

### What is Custom step and how to set it properly?

Cluster chart shows volume data at each price level for a specified period. But with a large number of levels, the cluster chart becomes difficult to read.&#x20;

**Custom step** summarizes the volume data of as many price levels as specified in the setting. By default, the value of the custom step is set to 1 tick, which means the volume data are shown at each price level.
