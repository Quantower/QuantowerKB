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

<figure><img src="../../../.gitbook/assets/reset order to default.gif" alt=""><figcaption></figcaption></figure>

