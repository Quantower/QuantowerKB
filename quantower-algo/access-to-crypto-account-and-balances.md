---
description: Get access to current crypto account information.
---

# Access to crypto account and balances

## **Theory**

While developing a trading strategy script, you will definitely need to use a trading account. For example, to send a “place order’ request, you need to use an account ID. Or, if you need to calculate the trade quantity for the request, you need to check the available balance. All strategies must have trading account as input parameter.

Quantower API supports two types of user accounts - [Account](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.Account.html) and [CryptoAccount](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.CryptoAccount.html) classes.

### **Account class**

[Account](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.Account.html) ****is a base class that contains general information about a user. Let's take a look at the main properties.

* **Id -** unique account identifier
* **Name** - current account name
* **AccountCurrency** - base currency 
* **Balance** - available balance
* **ConnectionId** - connection id associated with this account
* **AdditionalInfo** - collection of fields with specific info

For getting all available accounts from all open connections you can use ['Accounts'](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.Core.html#TradingPlatform_BusinessLayer_Core_Accounts) main property from [Core](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.Core.html) object.

```csharp
var allAccountsCollection = Core.Instance.Accounts;

foreach (var account in allAccountsCollection)
{
    // to do something
}
```

### **CryptoAccount class**

This class derives from [Account](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.Account.html) ****and describes a crypto trading account. Since trading on crypto-exchanges is possible with different crypto-currencies this class contains ‘**Balances**’ property that stores information about all available crypto-balances.

* **Balances** - array that contains current balance information for each available cryptocurrencies.Each item is an instance of '‘[CryptoAssetBalances](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.CryptoAssetBalances.html)’ class

### CryptoAssetBalances class

This class contains general information about a specific cryptocurrency.  Let's take a look at the main properties.

* **AssetId** - base currency identifier
* **TotalBalance** - total amount of currency
* **ReservedBalance** - amount of reserved currency \(submitting limit orders etc.\)
* **AvailableBalance** - amount of available currency \(TotalBalance - ReservedBalance\)
* **TotalInBTC** - converted total amount of currency in ‘BTC’
* **TotalInUSD** - converted total amount of currency in ‘USD’

## Practice  





