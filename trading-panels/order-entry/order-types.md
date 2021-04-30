---
description: >-
  Order Types allow you to specify how an order behaves when it enters the
  market.
---

# Order Types

Order Types allow you to specify how an order behaves when it enters the market. For example, you may want an order to immediately fill at the current best price \(market order\) or to fill only at a particular price \(limit order\).

Order Types differ from order restrictions which set how the order behaves during the session. For example, an order may delete if not filled by the end of the session \(Day\) or may exist until filled or canceled \(GTC\).

Orders can be divided into 2 groups by side:

* **Buy** order which opens a long position is sent if the trader believes in the further growth of the asset;
* **Sell** order which opens a short position is sent if the trader believes in the further decrease of the asset.

![Order&apos;s side - Buy and Sell](../../.gitbook/assets/image%20%28220%29.png)

Quantower supports the following order types:

* Market
* Limit
* Stop order 

