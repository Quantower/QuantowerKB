---
description: >-
  Local Stop loss & Take profit orders allow to set these types of orders for
  all connections that don't natively support them.
---

# Local SL/TP

Quantower provides this functionality using the Orders placing strategy feature, meaning that all of the Local orders are solely handled on the platform side (literally "on your machine"). Such behavior leads to some important notices and limitations that users should understand before use of Local closing orders:

{% hint style="warning" %}
<mark style="color:orange;">**We insist that you read, practice, and understand how the Local closing orders work before using them for live trading.**</mark>&#x20;
{% endhint %}

{% hint style="info" %}
**Local SL/TP orders exist and managed on the platform side ("on your machine").**&#x20;
{% endhint %}

{% hint style="danger" %}
**When you close the platform, it will permanently **<mark style="color:red;">**delete ALL Local SL/TP orders**</mark>**.**&#x20;
{% endhint %}

{% hint style="danger" %}
**When your platform loses connection, it will permanently **<mark style="color:red;">**delete all Local SL/TP orders related to this connection**</mark>**, and you won't be able to restore them after reconnecting.**
{% endhint %}

{% hint style="warning" %}
**Please, do not use **<mark style="color:blue;">**Reverse**</mark>** and **<mark style="color:blue;">**Breakeven**</mark>** buttons with orders and positions containing Local SL/TP orders to avoid unexpected behavior.**
{% endhint %}

