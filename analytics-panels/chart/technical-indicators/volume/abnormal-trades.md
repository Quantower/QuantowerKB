---
description: >-
  The Abnormal Trades indicator is designed to quickly find bars on the chart
  and in the watchlist with an abnormally high number of trades.
---

# Abnormal Trades

This indicator helps find bars and areas on the chart where a large number of trades occurred over a selected period of time. It can also be added to the watchlist to quickly sort and select instruments with a high volume of trades at any time. The search and selection of instruments is based on the ratio of the number of trades on the current bar to the average number of trades over the specified period.

<figure><img src="../../../../.gitbook/assets/general view of Abnormal trades indicator.png" alt=""><figcaption><p>General view of Abnormal Trades indicator</p></figcaption></figure>

{% hint style="info" %}
**Abnormal Trades (K-factor)** shows how many times the number of trades on the current bar exceeds the average value over the last specified period.

The coefficient is calculated in real-time, without waiting for the bar to close, allowing you to quickly react to the appearance of a large number of trades over the selected period in the market.&#x20;

**Period (N)** — the number of previous bars to compare the number of trades on the current bar.&#x20;

**K= Number of trades on the current bar / average number of trades on this instrument for the previous N bars.**
{% endhint %}

Since different trading instruments, timeframes, and market periods have their individual average and abnormal trade values, the indicator calculates a relative value, which allows it to be applied to all instruments and timeframes.

### Adding Abnormal Trades to Chart

<figure><img src="../../../../.gitbook/assets/adding of abnormal trades to the chart.png" alt=""><figcaption></figcaption></figure>

### Adding Abnormal Trades to Watchlist

**Period** — the number of historical bars to calculate the average number of trades on the selected instrument.&#x20;

**Aggregation** — the timeframe of the bars on which the calculation and search for abnormal trades will be performed.

<figure><img src="../../../../.gitbook/assets/adding of abnormal trades to watchlist.png" alt=""><figcaption></figcaption></figure>

### How to use the Abnormal Trades indicator

Considering that Abnormal Trades can be applied to different timeframes, you can combine this parameter with other indicators on lower or higher timeframes in your watchlist.

Abnormal Trades is updated in real-time based on the data of the latest candle. Since the watchlist includes a shift parameter, you can search for a bar with a large number of trades on the previous bar. This provides advanced capabilities for searching for patterns and trading formations.&#x20;

Details on how to filter, sort, and create notifications are described in the [Setup Actions & Advanced Filters](../../../../general-settings/setup-actions-and-advanced-filters.md) guide.

Abnormal Trades does not highlight the range within the bar where these trades occurred but rather records the fact of large number of trades executed on the current bar. Therefore, if you need to visually see the abnormal trade zone within a specific bar in history or in real-time, you need to add a step-by-step profile equal to the timeframe of the current chart based on the aggregation of trades, or add [Power trades](../../power-trades.md).

<figure><img src="../../../../.gitbook/assets/step profile with abnormal trades.png" alt=""><figcaption></figcaption></figure>
