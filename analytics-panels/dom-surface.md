---
description: >-
  It's an advanced Order Flow Surface panel that shows past and current
  liquidity in a Heatmap view. Actual trades are represented as Volume Circles
  with corresponded sizes.
---

# DOM Surface

DOM Surface panel shows all past and current changes in the order book — placing, modifying orders, and executing trades.

### Additional DOM Surface columns

On the right side of the panel, there are three histograms — **Size, Cumulative Size, Order Book Imbalance**.

![Additional DOM Surface columns with Order Book Size, Cumulative size and Order Book Imbalance](../.gitbook/assets/dom-surface-histograms.png)

* **Size \(Current Order Book\)** This histogram shows the volume of limit orders at each price level. User can visually compare the size of each bar for determining the most strong level.
* **Cumulative Size** This histogram displays the sum of sizes of limit orders for each subsequent level. This histogram allows estimating the dominating side of the market.
* **Imbalance \(Order Book Imbalance\)** This histogram shows the percentage of how much the volume of buy orders exceeds the amount of sell orders \(and vice versa\) for each price level. It measures whether the limit order book is buy or sell heavy. The more the imbalance exceeds one side, the higher the probability of price movement towards the imbalance. In fact, it is a good predictor of price direction.





