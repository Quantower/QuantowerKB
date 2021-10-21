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

![](../.gitbook/assets/Screenshot\_7.png)

### How to create a mapping between two symbols?

* Launch the **Symbol Mapping** panel from the Control Center. The panel is located in the _Misc_ category.

![](<../.gitbook/assets/image (347).png>)

* Add a symbol where all trade operations (orders, positions) will be sent

![](<../.gitbook/assets/image (356).png>)

