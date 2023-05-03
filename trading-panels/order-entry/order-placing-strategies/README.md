---
description: Placing orders with some automation
---

# Order placing strategies

Each time you place an order in Quantower — you do it immediately by pressing a corresponding button and sending your order to the remote server. This is a usual operation for every trader, but what if you would like to schedule the order sending or split the order's quantity in time. Maybe you would like to apply some non-standard order parameters or order types not supported by your broker?

## Where and how to use it?

Here comes the functionality of Order placing strategies, allowing simple automation of complex order submission. You can find the corresponding control in every Order entry panel or sidebar.

![Order placing strategy control in Quantower Order entry](../../../.gitbook/assets/Screenshot\_4.png)

To apply some Order placing strategy, you should:

1. select the required type of automation from the dropdown list;
2. set up automation parameters;
3. press a <mark style="background-color:blue;">send</mark> button , and your automation will start immediately after that.

### Types of placing strategies

There are several placing strategies currently available for use, and this list is constantly growing, so let's find out how to set up and use them for your trading:

* **Iceberg**
* **Local SL/TP**\
  Allows Stop loss and Take profit orders for brokers that don't support them natively. [<mark style="color:blue;">**Read more about this type of automation**</mark>](local-sl-tp.md)
* **Limit if Touched**
* **Market if Touched**
* **Scheduled**\
  Specify the exact time in the future, when your platform should send this order.
* **Time split**\
  Send one order by several parts in some time interval.

### Order placing strategies panel

You can find all of the active and finished Placing strategies in the corresponding panel, which you may launch from the Quantower start menu. This panel contains the list of created Strategies and a logs section. You can click on any Strategy and see how it works and what actions it performs. Here you can also stop any active strategy or clear the finished ones.

![Order placing strategies panel](../../../.gitbook/assets/Screenshot\_6.png)

## Please pay attention!

{% hint style="warning" %}
<mark style="color:orange;">All automation of Placing strategies</mark> <mark style="color:orange;"></mark><mark style="color:orange;">**works while the platform is functioning**</mark><mark style="color:orange;">. When you close your platform, it will delete all automation without the possibility to restore it</mark>
{% endhint %}
