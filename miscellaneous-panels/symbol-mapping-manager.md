---
description: >-
  This panel is used to receive data from one broker that provides it and trade
  with another broker.
---

# Symbol Mapping Manager

For example, Interactive Brokers doesn't provide the necessary data for using Cluster chart. But a trader can use dxFeed data provider which offers such data and a trader can use it for trading on IB. Watch the video for more details

{% embed url="https://www.youtube.com/watch?v=V_v4VXTXd2c" %}

### General overview of Symbol Mapping panel

The panel is a table where the trader adds symbols for trading, and also selects from which connection and which symbol to receive quotes for analysis. After creating a mapping, the trader must open the chart of the symbol that he will trade (for example, from Interactive Brokers connection). In this case, all data for this symbol will come from the second connection (for example from IQFeed or from dxFeed).

![General view of Symbol Mapping panel](../.gitbook/assets/symbolMapping.png)

### How to create a mapping between two symbols?

* Launch the **Symbol Mapping** panel from the Control Center. The panel is located in the _Misc_ category.

![](<../.gitbook/assets/image (347) (1) (1).png>)

* Add a symbol where all trade operations (orders, positions) will be sent.

![](<../.gitbook/assets/image (356) (1) (1) (1) (1) (1) (1).png>)

* Select the symbol for getting historical and real-time data (Level1 and Level2)

![](<../.gitbook/assets/image (357) (1) (1) (1) (1) (1).png>)

{% hint style="info" %}
_**Mapping Type has two modes:**_

**Simple mode** where you can select 1 symbol for all real-time quotes (Level1 and Leve2 data) + Historical data (bars and volume)

**Custom mode** where you can select different symbols for different quotes and historical data. For example, you can set the real-time data from one data provider, but historical data from another source.

<img src="../.gitbook/assets/image (356) (1) (1) (1) (1) (1).png" alt="" data-size="original">
{% endhint %}

* After the mapping of symbols is set up, you need to open the trading panel with the desired symbol to start trading

![Select the symbol on the chart where you want to make trading operations](<../.gitbook/assets/image (349) (1) (1).png>)
