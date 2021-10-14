---
description: >-
  Order Types allow you to specify how an order behaves when it enters the
  market.
---

# Order Types

Order Types allow you to specify how an order behaves when it enters the market. For example, you may want an order to immediately fill at the current best price (market order) or to fill only at a particular price (limit order).

Order Types differ from order restrictions which set how the order behaves during the session. For example, an order may delete if not filled by the end of the session (Day) or may exist until filled or canceled (GTC).

| Connection      | Order Types                                                                       | Brackets (SL/TP)                                     | OCO           | Additional                                                                                     |
| --------------- | --------------------------------------------------------------------------------- | ---------------------------------------------------- | ------------- | ---------------------------------------------------------------------------------------------- |
| CQG             | <p>Market, Limit, <br>Stop, Stop Limit</p>                                        | <p>Server-side</p><p>(Single and Multiple)</p>       | Server-side   | <p>Algorithmic orders</p><p>(Iceberg, Trailing Limit)</p><p>Trailing Stop is not available</p> |
| Rithmic         | <p>Market, Limit, <br>Stop, Stop Limit, Trailing Stop (server-side). MIT, LIT</p> | Server-side (single only)                            | Server-side   |                                                                                                |
| Binance (Spot)  | Market, Limit,                                                                    | Not available                                        | Not available |                                                                                                |
| Binance Futures | <p>Market, Limit, <br>Stop market, Stop Limit, Trailing Stop</p>                  | <p>Server-side</p><p>(only for existed position)</p> | Not available | Behaviour (Open or Close)\*                                                                    |
| Bybit           |                                                                                   |                                                      |               |                                                                                                |

Orders can be divided into 2 groups by side:

* **Buy** order which opens a long position is sent if the trader believes in the further growth of the asset;
* **Sell** order which opens a short position is sent if the trader believes in the further decrease of the asset.

![Order's side - Buy and Sell](<../../.gitbook/assets/image (220).png>)

Depending on a trading connection Quantower supports the following order types:

*   **Market** **order** is an order placed without a price with the intention of hitting the best Bid or taking the best Offer currently available in the market. The order fills at the current best price.

    Note, that Market orders may partially fill at multiple price levels.\

* **Limit order** allows you to submit an order at a specific (desired) limit price. Like market orders, limit orders allow for partial fills however, the remaining quantity continues to work in the market at the original limit price.
* Stop order\
