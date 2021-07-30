---
description: >-
  Order Types allow you to specify how an order behaves when it enters the
  market.
---

# Order Types

Order Types allow you to specify how an order behaves when it enters the market. For example, you may want an order to immediately fill at the current best price \(market order\) or to fill only at a particular price \(limit order\).

Order Types differ from order restrictions which set how the order behaves during the session. For example, an order may delete if not filled by the end of the session \(Day\) or may exist until filled or canceled \(GTC\).

<table>
  <thead>
    <tr>
      <th style="text-align:left">Connection</th>
      <th style="text-align:left">Order Types</th>
      <th style="text-align:left">Brackets</th>
      <th style="text-align:left">OCO</th>
      <th style="text-align:left">Additional</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">CQG</td>
      <td style="text-align:left">Market, Limit,
        <br />Stop, Stop Limit</td>
      <td style="text-align:left">
        <p>Server-side</p>
        <p>(Single or Multiple)</p>
      </td>
      <td style="text-align:left">Server-side</td>
      <td style="text-align:left">
        <p>Algorithmic orders</p>
        <p>(Iceberg, Trailing Limit)</p>
        <p>Trailing Stop is not available</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Rithmic</td>
      <td style="text-align:left">Market, Limit,
        <br />Stop, Stop Limit</td>
      <td style="text-align:left">Server-side</td>
      <td style="text-align:left">Server-side</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Binance (Spot)</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Binance Futures</td>
      <td style="text-align:left">Market, Limit,
        <br />Stop market, Stop Limit, Trailing Stop</td>
      <td style="text-align:left">
        <p>Server-side</p>
        <p>(only for existed position)</p>
      </td>
      <td style="text-align:left">Not available</td>
      <td style="text-align:left">Behaviour (Open or Close)*</td>
    </tr>
  </tbody>
</table>

Orders can be divided into 2 groups by side:

* **Buy** order which opens a long position is sent if the trader believes in the further growth of the asset;
* **Sell** order which opens a short position is sent if the trader believes in the further decrease of the asset.

![Order&apos;s side - Buy and Sell](../../.gitbook/assets/image%20%28220%29.png)

Quantower supports the following order types:

* Market
* Limit
* Stop order 

