---
description: >-
  Volume analysis is a powerful trading technique that allows analyzing the
  distribution of the trading volume at each price level at a certain period of
  time.
---

# Volume Analysis Tools | Volume Profiles | Footprint chart | VWAP

Quantower trading platform provides [**Volume analysis tools**](https://www.quantower.com/volumeanalysistools), an advanced analytical functionality, which allows you to see the traded volume at each price level, assess the balance between buyers and sellers and understand the intentions of traders regarding the future price

Volume analysis tools include proprietary and well-known analytics:

* [**Cluster Chart**](https://help.quantower.com/analytics-panels/chart/volume-analysis-tools/cluster-chart) (a.k.a. Footprint chart or OrderFlow chart)
* [**Volume Profiles**](https://help.quantower.com/analytics-panels/chart/volume-analysis-tools/volume-profiles) — Step, Right, Left and Custom volume profiles
* [**Time Statistics**](https://help.quantower.com/analytics-panels/chart/volume-analysis-tools/time-statistics) — volume data per each bar in table form
* [**Time Histogram**](https://help.quantower.com/analytics-panels/chart/volume-analysis-tools/time-histogram) — volume data per each bar in the form of a vertical histogram
* [**Custom VWAP (Anchored VWAP)**](../anchored-vwap.md) — can be attached to any selected bar as a starting calculation point
* [**VWAP**](../vwap.md) — multiple VWAP lines for a single chart
* [**Historical Time & Sales**](https://help.quantower.com/analytics-panels/chart/volume-analysis-tools/historical-time-and-sales) — the table of all trades for the any selected bar

{% embed url="https://youtu.be/duOmadSFN4Y" %}

&#x20;The GIF below shows how you can activate the toolbar of volume analysis tools:

![Enable the toolbar of Volume Analysis Tools ](../../../.gitbook/assets/volume-analysis-tools.gif)

{% hint style="info" %}
<mark style="color:green;">**Green color**</mark> indicates that the selected volume analysis tool has fully downloaded the data. \
<mark style="color:orange;">**Yellow color**</mark> indicates that the selected tool is still downloading the data.
{% endhint %}

### Data Types of Volume Analysis Tools

Almost all volume analysis tools have the same **Data Types**, which can be set in the settings:

* **Trades** — the number of contracts (trades) executed at each price level.
* **Buy (or Sell) Trades** — the number of Buy (or Sell) trades executed at each price level.
* **Volume** — the total size of all trades executed at each price level or price range.
* **Buy (or Sell) Volume** — the total size of all Buy (or Sell) trades executed at each price level or price range.
* **Buy (or Sell) Volume, %** — shows how many percent of the total volume related to Buy (or Sell) trades.
* **Buy / Sell Volume** — displays Buy and Sell volume simultaneously on one histogram.
* **Delta and Delta %** — shows the difference in traded Volume between Buyers and Sellers, helping to see who controls the market at a given time.\
  &#xNAN;_<mark style="color:red;">Delta % = Delta / Volume \* 100</mark>_
* **Cumulative Delta** — the data is built by adding the current delta to each subsequent delta for a certain period (or number of bars).

![Use various data types for all volume analysis tools](../../../.gitbook/assets/volume-profiles-data-types.png)

* **Average size** — the average volume of the position that was executed at a certain price or price range.
* **Average Buy size** — the average volume of a Buy position that was executed at a specific price or price range.
* **Average Sell size** — the average volume of a Sell position that was executed at a specific price or price range.
* **Max one trade volume (value and %)** — shows the maximum volume of a single trade that has executed at a certain price or price range (depending on the Custom Step (ticks) setting).
* **Filtered volume (value and %)** — this parameter displays volumes that exceed the size specified in the filter. If the volume size is smaller than the one specified in the filter, then the values will be zero.
* **Buy (or Sell) filtered volume** — the parameter displays Buy (or Sell) volumes that exceed the size specified in the filter.
