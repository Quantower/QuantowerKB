---
description: >-
  This category allows you to configure the necessary parameters for the Order
  Entry sidebar. Here, you can set the order size, show/hide order & position
  management buttons.
---

# Order Entry

The Order Entry sidebar settings can be accessed through:

* [**General settings**](../chart-settings.md) in a specific trading panel (Chart, DOM trader, DOM Surface, TPO)
* **Right-clicking** on the Order Entry sidebar -> Context menu -> Settings

<figure><img src="../../../.gitbook/assets/order entry settings.png" alt=""><figcaption><p>Right-click for getting settings of Order Entry</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/Chart order entry.png" alt=""><figcaption><p>General view of Order Entry sidebar settings </p></figcaption></figure>

* **Show Order Entry** setting shows/hides the Order Entry sidebar.
* **Slim mode** allows you to narrow the size of the Order Entry sidebar for a more compact view.
* **No labels** setting hides the labels above each block in the panel for a more compact view.
*   **Show additional order parameters** setting is responsible for displaying extra order parameters that a trader can use if needed. The types of parameters can vary for each type of connection:

    &#x20;**-** **CQG** includes an additional "**Algorithmic**" order parameter

    &#x20;**-** **Binance Futures** has several additional parameters (**Behavior** for orders in different hedge modes, **Post-only** mode, **Trigger price**)

<figure><img src="../../../.gitbook/assets/additional order parameters.png" alt=""><figcaption><p>Additional order parameters for different connections</p></figcaption></figure>

* **Reset quantity to default after an order was placed.** The setting returns the order size to a previously saved size after each trade. \
  For example, you set the default order size to 2 lots. After that, you increased the size to 3 lots for the current trade. Once the order with this size (3 lots) is placed, the platform will automatically revert the value to the previously saved size, i.e., 2 lots.

{% hint style="info" %}
**Note:** This setting only works if you have set a default order size value.
{% endhint %}

<figure><img src="../../../.gitbook/assets/reset order to default.gif" alt=""><figcaption><p>Reset quantity to default value after the trade</p></figcaption></figure>

* **Quick quantity buttons.** In the text block, you can modify existing trading buttons for quick switching between different order sizes. To add new buttons, simply enter new values using the separator “<mark style="background-color:green;">**;**</mark>”.

{% hint style="success" %}
<mark style="background-color:green;">**Tip #1**</mark>\
You can add mathematical signs before the values to quickly increase, decrease, or reset the current value in the Quantity field.

![](<../../../.gitbook/assets/image (413).png>)\
<mark style="background-color:green;">**Tip #2**</mark>

To create multiple rows of Quick quantity buttons, you need to move the value to a new line in the text block.

![](<../../../.gitbook/assets/image (416).png>) ![](<../../../.gitbook/assets/image (415).png>)
{% endhint %}

<figure><img src="../../../.gitbook/assets/Quick quantity buttons.gif" alt=""><figcaption><p>Editing of Quick quantity buttons</p></figcaption></figure>

* **Quick quantity buttons mode.** This setting is exclusively used for <mark style="background-color:green;">**crypto connections**</mark> and determines the mode for calculating position volume. The setting has 3 modes:\
  \
  &#x20;**-** <mark style="background-color:orange;">**Quantity mode**</mark>, which sets the position size in an absolute value (1 lot, 2 lots, etc.)\
  &#x20;**-** <mark style="background-color:orange;">**Total mode**</mark>, which sets the position size in an absolute value based on the total balance\
  &#x20;**-** <mark style="background-color:orange;">**Balance percent mode**</mark>, which sets the position size as a percentage of the total balance

<figure><img src="../../../.gitbook/assets/quantity modes.png" alt=""><figcaption><p>Quantity modes for crypto connections</p></figcaption></figure>

