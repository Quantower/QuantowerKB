# Order Entry for CQG

The general view of the Order Entry panel for CQG connection is as follows, and is divided into the following categories:

* Account and symbol selection -  [The same as for the general pane](./)
* Order side and its quantity -         [**The same as for the general pane**](./)\*\*\*\*
* \*\*\*\*[**How to set up traling order**](order-entry-for-cqg.md#how-to-set-up-traling-order)\*\*\*\*
* [Order parameters — type, TIF, price](order-entry-for-cqg.md#cqg-ordertypes-time-in-force-tif-algorithmic-in-quantower)
* \*\*\*\*[**How to set up Profit and Stop orders**](order-entry-for-cqg.md#how-to-set-up-profit-and-stop-orders)\*\*\*\*
* \*\*\*\*[**How to set up  multiple Profit and Stop orders for one position**](order-entry-for-cqg.md#how-to-set-up-multiple-profit-and-stop-orders-for-one-position)\*\*\*\*

![](../../.gitbook/assets/image%20%28270%29.png)

### How to set up traling order

AMP/CQG support **server-side trailing orders**. To set such an order you must Select order type select TRAIL item in Algorithmic trading Specify the parameters of this Price and the offset for the movement



![](../../.gitbook/assets/animaciya-8-.gif)



## CQG OrderTypes, Time in Force \(TIF\), Algorithmic in Quantower

CQG provides various order types for trading via the Order Entry panel:

* Market order
* Limit order
* Stop order
* Stop limit order

![Order types in Quantower for CQG connection](../../.gitbook/assets/image%20%28218%29.png)

**Time-in-force \(TIF\)** instructions define the length of time over which an order will continue working before it is canceled. CQG provides various TIFs:

![Time in Force \(TIFs\) for CQG connection](../../.gitbook/assets/image%20%28217%29.png)

* **GTC \(Good till canceled\)** — orders will remain working until they are canceled by trader or the contract expires;
* **FOK \(or Fill or Kill\)** —  order will be canceled if it is not executed in the entire volume as soon as it becomes available;
* **IOC \(Immediate or cancel\)** — requires that any portion of an order that is not filled as soon as it becomes available in the market is canceled;
* **DAY** — order will be canceled if it is not executed within the current trading day;
* **GTD \(Good till date\)** — order will remain working within the system and in the marketplace, until it executes or until the close of the market on the date specified.
* **GTT \(Good till time\)** — order that remains open until a specified time. At that time, any unfilled lots are canceled.
* **FAK** \(**Fill and Kill\)** — ****orders require that any remaining quantity after a partial fill be canceled.
* **ATC \(At the Close Order\)** — order to buy or sell a stock at the closing price. One of the benefits of this type of order is that it can be placed prior to the actual end of the trading day requested. This would be the opposite of an at-the-open order.
* **ATO \(At-The-Open Order\)** — order to buy or sell a stock at the opening price. ATO order is allowed during pre-open sessions \(morning and afternoon\) or even the night before.



### How to set up Profit and Stop orders

Then you can set **automatic stop loss and profit** in pips. It's very convenient to set the lot size and protect it. Specify your values in the appropriate fields.

{% hint style="info" %}
Some brokers such as Binance do not allow stop orders for limit orders. \(Until the position is NOT open\) In this case, use limit orders of the opposite direction
{% endhint %}

![](../../.gitbook/assets/animaciya-3-%20%281%29.gif)

* Use the Qquick Ttrade toolbar 
* Set your values for stop loss or profit. You can also use any one parameter only. 
* Use the button to activate the trade with the mouse to set a limit order

{% hint style="warning" %}
If you execute an order at market, the specified stop parameters will retain their values and will be set immediately.
{% endhint %}

### How to set up  multiple Profit and Stop orders for one position

![](../../.gitbook/assets/animaciya-4-.gif)

* To set multiple stop orders for a single position, do the following Switch the bracket \(stop\) settings to multi mode 
* Enter data for setting the first limit orders and how many lots or coins should be closed 
* For the next stops, enter similar data on the next line.
*  You can set orders in multiples of your total volume.



