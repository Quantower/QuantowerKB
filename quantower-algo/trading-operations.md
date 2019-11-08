---
description: >-
  Placing a different type of orders, modifying and canceling them using
  Quantower API
---

# Trading operations

A key part of each strategy is a trading algorithm it implements. In most cases it requires possibilities of placing a different type of orders, modifying and canceling them. In this topic, we will show you how to get access to this operations via [**Quantower API**](https://api.quantower.com/).

## Placing orders

As we wrote in the previous topic, [**Core**](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.Core.html) class is the main entry point for all major functions and placing orders \(as well as all other trading operations\) are not the exception. The most flexible way of placing orders is using the [**PlaceOrder**](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.Core.html#TradingPlatform_BusinessLayer_Core_PlaceOrder_TradingPlatform_BusinessLayer_PlaceOrderRequestParameters_) method, that accepts [**PlaceOrderRequestParameters**](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.PlaceOrderRequestParameters.html) object as input parameter. This object provides you with more than 15 parameters and using them you can customize your order request according to your needs. It is not necessary to fill all, usually, you will need only main, such as:

| Parameter | Description |
| :--- | :--- |
| Account  | An account for order  |
| Symbol  | A symbol for order  |
| Side  | Side of order: Buy or Sell |
| Price | Price for Limit or Stop Limit order |
| TriggerPrice | Trigger price for Stop or Stop Limit Order  |
| Quantity | Amount of the order \(in lots\) |
| StopLoss | An instance of SlTpHolder object, where you can specify price or offset for Stop Loss order  |
| TakeProfit | An instance of SlTpHolder object, where you can specify price or offset for Take Profit order |
| OrderTypeID | An ID of required order type. For most cases you will need only basic types, so you can use predefined constants: OrderType.Limit, OrderType.Stop, OrderType.Market and OrderType.StopLimit |

   And code example of using this method:

```csharp
// Full form, allows you to specify all parameters
Core.Instance.PlaceOrder(new PlaceOrderRequestParameters()
{
    Account = this.account,
    Symbol = this.symbol,
    Side = Side.Buy,
    Price = this.symbol.Bid - this.symbol.TickSize * 10,
    TimeInForce = TimeInForce.Day,
    Quantity = 2,
    StopLoss = SlTpHolder.CreateSL(20, PriceMeasurement.Offset),
    TakeProfit = SlTpHolder.CreateSL(10, PriceMeasurement.Offset),                   
    OrderTypeId = OrderType.Limit
});
```

Another option to send order request is using the overloaded [**PlaceOrder**](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.Core.html#TradingPlatform_BusinessLayer_Core_PlaceOrder_TradingPlatform_BusinessLayer_Symbol_TradingPlatform_BusinessLayer_Account_TradingPlatform_BusinessLayer_Side_TradingPlatform_BusinessLayer_TimeInForce_System_Double_System_Double_System_Double_System_Double_) method, which accepts only basic order parameters. The shortest form will send Short or Long 1 lot position using a specified symbol and account:

```csharp
Core.Instance.PlaceOrder(this.symbol, this.account, Side.Buy);
```

You can also add other parameters, for example if you want to place a Limit order just need to specify Price:

```csharp
Core.Instance.PlaceOrder(this.symbol, this.account, Side.Buy, price: this.symbol.Bid - this.symbol.TickSize * 5)
```

Or Trigger price for Stop order:

```csharp
Core.Instance.PlaceOrder(this.symbol, this.account, Side.Buy, triggerPrice: this.symbol.Bid - 5 * this.symbol.TickSize);
```

## Modifying orders

Once you created your order you can modify its parameters - use [ModifyOrder](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.Core.html#TradingPlatform_BusinessLayer_Core_ModifyOrder_TradingPlatform_BusinessLayer_Order_TradingPlatform_BusinessLayer_TimeInForce_System_Double_System_Double_System_Double_System_Double_) function in Core class for this. You can specify only parameter you want to change, for example, if you want to change Quantity of order:

```csharp
Core.Instance.ModifyOrder(orderToModify, quantity: 5);
```

If you need to change the price of the order:

```csharp
Core.Instance.ModifyOrder(orderToModify, price: this.symbol.Bid - 10 * this.symbol.TickSize);
```

Or, if you want, you can request changing all parameters simultaneously: quantity, time in force, price:

```csharp
Core.Instance.ModifyOrder(orderToModify, quantity: 5, timeInForce: TimeInForce.GTC, price: this.symbol.Bid - 10*this.symbol.TickSize);
```

## Cancelling orders

As expected there is a function for canceling Order - [**CancelOrder**](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.Core.html#TradingPlatform_BusinessLayer_Core_CancelOrder_TradingPlatform_BusinessLayer_Order_). All you need to specify is Order object:

```csharp
Core.Instance.CancelOrder(orderToCancel);
```

You can use also Cancel method of Order class as an alternative way:

```csharp
orderToCancel.Cancel();
```

## Closing positions

The closing of positions is very similar to canceling orders. Use [**ClosePosition**](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.Core.html#TradingPlatform_BusinessLayer_Core_ClosePosition_TradingPlatform_BusinessLayer_Position_System_Double_) method from [**Core**](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.Core.html):

```csharp
Core.Instance.ClosePosition(positionToClose);
```

Or method **Close** from **Position** class:

```csharp
positionToClose.Close();
```

{% hint style="info" %}
If allowed by your current connection, you can request partial closing of position. Both ways of closing positions accept CloseQuantity parameter, which determines an amount that should be closed.
{% endhint %}

## Result of trading operations

All trading operations return special object **TradingOperationResult** which contains information about the result of the processing request: 

| Parameter | Description |
| :--- | :--- |
| Status | **Success** if a request was sent to server or **Failure** if some problems occurred |
| Message  | Text with detail information in case of errors |

Using these set of trading functions you can simply create any algorithm for your trading strategy. In our further articles, we will cover more specific and practical cases, such as specifying parameters for advanced order types and creating universal trading logic, for different connections.

