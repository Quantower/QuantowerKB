---
description: How to export Real-Time data to Exel
---

# Excel and RTD function

Start from version 1.39 Quantower supports **Real-Time Data \(RTD\)** for sending data and other market information to Microsoft Excel®. This feature opens up many opportunities for creating custom displays and other ways to better manage your workflow. 



RTD is a newer protocol that offers several advantages over DDE, including more flexibility and better performance and reliability.

We prepared the spreadsheet that outlines the basic syntax of RTD formulas with details more complex formulas. Included is a collection of popular RTD formulas, which you can simply copy and paste into your own spreadsheet. [**Download the sample file**](https://updates.quantower.com/misc/RTD/rtd_samples.xlsx)**.**

Here is the General Syntax for getting symbol info via RTD function:

![](../../.gitbook/assets/screenshot_128%20%281%29.png)

{% embed url="https://www.youtube.com/watch?v=k1pbtSadX8I" %}

## **How to activate RTD function in Quantower platform**

{% hint style="warning" %}
For the function to work properly, **Quantower platform and Excel must have the same version — 64 or 32 bit**
{% endhint %}

Launch Excel and after open the Task Manager to check the version of Excel \(32-bit or 64-bit\). The platform should have the same version in order to work with RTD function correctly.

![](../../.gitbook/assets/image%20%28150%29.png)

Go to the [**General Settings**](../../general-settings/general-settings-1.md) of the platform, then to _section **Excel RTD**_ and tick off _**"Enable Microsoft Excel RTD"**_

![Activation of RTD function in Quantower](../../.gitbook/assets/assets_-ld6fsrvq3jgwjig6o7r_-lme4wbmrbk0ai3rafld_-lmeyazmdvqpbsftpr9b_rtd.png)

Also in the settings, there are two important settings:

* **Custom RTD formula name** — depending on the language of your operating system, the name of the RTD function in Excel may be called differently. The original name of the function in the English version of Excel is RTD, but for the Russian version it's called "ДРВ".
* **Custom argument separator** — the separator that participates in the formula. It depends on the localization of your operating system. Get to know [how to check argument separator in your system](./#how-to-check-argument-separator).

## How to get the instrument data from Quantower?

### 1. Getting data through copying a formula

The easiest way to get data to Excel is to copy the necessary data through the panel context menu. For example, after activating RTD, an additional item in the context menu will appear in the Watchlist panel — **Copy RTD Formula**.

* Select a necessary symbol or multiple symbols, right-click and select **Copy RTD Formula**. You can copy formulas for specific columns or for all columns.

![](../../.gitbook/assets/rtd-watchlist.png)

* Go to Excel and paste the copied formulas. Now the data will be updated automatically.

![Boadcasting real-time data to Excel](../../.gitbook/assets/rtd-quick-copying.gif)

{% hint style="info" %}
You may notice that the data is updated with some delay. This is a throttling interval that is set by default in Excel \(2000 milliseconds\). If you want to [increase the speed of updating data, read the instructions on how to do it](https://help.quantower.com/miscellaneous-panels/excel-rtd-trading/changing-rtd-throttle-interval-in-excel).
{% endhint %}

### 2. Getting data through writing a formula

When retrieving instrument data using RTD, you need to specify the ID of the instrument and the properties you want to retrieve.

RTD formula uses the following basic structure:

```text
=RTD("TradingPlatform";"";"Param1";"Param2";"Param3";....")
```

{% hint style="info" %}
The second parameter is the name of the external server running the RTD Server. As the Quantower RTD Server always runs locally, you must omit a value for the second parameter or supply an empty string \(“”\). However, you must account for the parameter in the formula.
{% endhint %}

### Examples of the most popular RTD formulas with description 

Examples of the most popular RTD formulas are described below with description of the basic syntax by the example of Binance exchange. Using them, you can get exactly the data you need for analysis and paste into your spreadsheet. You can also download these examples from this Excel file.

### 1.GetSymbolInfo - information about a specific symbol

{% hint style="success" %}
Provides access to specific symbol information such as Description, **ExchangeName, NettingType and others**. You can simply copy/paste this formula for use in Excel files or get it directly from the Symbol Information panel for the selected symbol. Right-click on the panel and select the menu option: "**Copy RTD Formula**" -&gt; "Value".
{% endhint %}

\*\*\*\*

```text
=RTD("TradingPlatform";"";"GetSymbolInfo";"BTCUSDT";"SymbolType";"Binance")
```

#### Options

| Options | Description |
| :--- | :--- |
| **"TradingPlatform"** | Quantower RTD server name. You can use it in all formulas. |
| **"GetSymbolInfo"** | Name of method |
| **"BTCUSDT"** | The ID of the symbol for which you want to get data. You can get it from the SymbolInfo panel. |
| **"SymbolType"** | Specifies the type of data you want to receive. For example: Name, Description. |
| **"Binance"** | The name of the connection you want to use to search for the desired character. You can leave this parameter blank if you only have one connection. |

![](https://gblobscdn.gitbook.com/assets%2F-M__G3zsA7jr_pKwIdiz%2F-MdD7Xd-0rMcvc9PCdnw%2F-MdDAb_29__xMcMGoTaX%2F%D0%B5%D0%BA%D1%81%D0%B5%D0%BB%D1%8C%20%D0%BA%D1%80%D0%B8%D0%BF%D1%82%D0%BE1.gif?alt=media&token=f409533f-8cb3-4ed5-b7dd-1fd04a677bdf)

![](https://gblobscdn.gitbook.com/assets%2F-M__G3zsA7jr_pKwIdiz%2F-MdDEfWoJWngCgyWqWIJ%2F-MdDFjuvLdNdsY-i1mSp%2F%D0%B5%D0%BA%D1%81%D0%B5%D0%BB%D1%8C%20%D0%BA%D1%80%D0%B8%D0%BF%D1%82%D0%BE%20%D1%81%D1%82%D0%B0%D1%82%D1%83%D1%81.gif?alt=media&token=113f6eba-d2c3-4fa4-888a-63275f006a1b)

### 2. GetAccounInfo - information about a particular account <a id="2-getaccouninfo-informaciya-o-konkretnoi-uchetnoi-zapisi"></a>

{% hint style="success" %}
Provides access to specific account information such as name, balance, NettingType, and others. You can simply copy/paste this formula for use in Excel files or get it directly from the Account Information panel for the selected account. Right-click on the pane and select the menu option: "Copy RTD Formula" -&gt; "Value".
{% endhint %}

```text
=RTD("tradingplatform";"";"GetAccountInfo";"binance";"fullLicense";"Binance")
```

_**Options**_

| _**Options**_ | Description |
| :--- | :--- |
| **"TradingPlatform"** | Quantower RTD server name. You can use it in all formulas. |
| **"GetMarketData"** | Name of method |
| **"BTCUSDT"** | The ID of the symbol for which you want to get data. You can get it from the SymbolInfo panel. |
| **"Bid"** | Specifies the type of data you want to receive. For example: Bid, Ask, Last, Open, High |
| **"Binance Futures"** | The name of the connection you want to use to search for the desired character. You can leave this parameter blank if you only have one connection. |

![](https://gblobscdn.gitbook.com/assets%2F-M__G3zsA7jr_pKwIdiz%2F-MdDYvNg3fltYBR__rmI%2F-MdDdK5vki_349k34zfM%2FGetMarketData%20-%20%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D0%B5%20%D1%81%D0%B8%D0%BC%D0%B2%D0%BE%D0%BB%D0%B0.gif?alt=media&token=b7653eb0-9b6d-42d6-8f99-df221d76a6ad)

###  GetLevel2Data - Level2   <a id="4-getlevel-2-data-level2-dannye-glubiny-rynka"></a>

Provides access to Tier 2 data for a specific symbol. You can simply copy/paste this formula and use it in your Excel files.

```text
 =RTD("tradingplatform";"";"GetLevel2Data";"BTCUSDT";"BidSize";"0";"Binance")
```

_**Options**_

| _**Options**_ | Description |
| :--- | :--- |
| **"TradingPlatform"** | Quantower RTD server name. You can use it in all formulas. |
| **"GetLevel2Data"** | Name of method |
| **"BTCUSDT"** | The ID of the symbol for which you want to get data. You can get it from the SymbolInfo panel. |
| **"BidSize"** | Указанный тип данных, которые вы хотите получать. Например: Bid, Ask, BidSize, AskSize. |
| **"0"** | The sequence number of the level in the Depth of Market. Starts with 0. |
| **"Binance"** | The name of the connection you want to use to search for the desired character. You can leave this parameter blank if you only have one connection. |

![](https://gblobscdn.gitbook.com/assets%2F-M__G3zsA7jr_pKwIdiz%2F-MdDeP1om5YlPw02mvCy%2F-MdDpQrD1zm6GSE_ZR-C%2FGetLevel2Data%20-%20Level2%20%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D0%B5%20%D0%B3%D0%BB%D1%83%D0%B1%D0%B8%D0%BD%D1%8B%20%D1%80%D1%8B%D0%BD%D0%BA%D0%B0%20.gif?alt=media&token=b50021c3-179a-49e1-b8d0-6294abce718f)

### 5. GetHistory - history for the specified symbol <a id="5-gethistory-istoriya-dlya-ukazannogo-simvola"></a>

Returns the history for the specified character, aggregation and date range. You can simply copy/paste this formula and use it in your Excel files.

```text
 =RTD("tradingplatform";"";"GetHistory";"BTCUSDT";"1Day";"Low";"10Day";"0";"Last";"Binance")
```

_**=RTD\("tradingplatform";"";"GetHistory";"BNBUSDT";"1Minute";"Close";"30Minute";"0";"Last";"Binance Futures"\)**_

_**=RTD\("tradingplatform";"";"GetHistory";"BTCUSDT";"5Minute";"Open";"300Minute";"0";"Last";"Binance Futures"\)**_

_**=RTD\("tradingplatform";"";"GetHistory";"ADAUSDT";"1Hour";"Low";"24Hour";"0";"Last";"Binance "\)**_

_**​**_

_**Options**_

| _**Options**_ | _Описание_ |
| :--- | :--- |
| **"TradingPlatform"** | Quantower RTD server name. You can use it in all formulas. |
| **"GetHistory"** | Name of method |
| **"BTCUSDT"** | The ID of the symbol for which you want to get data. You can get it from the SymbolInfo panel. |
| **"1Day"** | Aggregation type: 1 day, 3 days, 5 minutes, etc. Available aggregates:Tick, Second, Minute, Hour, Day, Week, Month, Year. |
| **"Close"** | Specifies the type of data you want to receive. For example: Open, High, Low, Close, Volume, Bid, Ask. |
| **"10Day"** | Required history range: 10 days, 300 minutes, etc. Available ranges: Minute, Hour, Day, Month, Year. |
| **"0"** | The index of the bar / tick in the returned history array. 0 means the newest bar. |
| **"Last"** | Bid, Ask, Last history type. Leave the field empty to get the default history for the specified character. |
| **"Binance"** | The name of the connection you want to use to search for the desired character. You can leave this parameter blank if you only have one connection. |

![](https://gblobscdn.gitbook.com/assets%2F-M__G3zsA7jr_pKwIdiz%2F-MdE86l5W8HjMUupdd2P%2F-MdE8AgutchiL75g8edf%2FGetHistory%20-%20%D0%B8%D1%81%D1%82%D0%BE%D1%80%D0%B8%D1%8F%20%D0%B4%D0%BB%D1%8F%20%D1%83%D0%BA%D0%B0%D0%B7%D0%B0%D0%BD%D0%BD%D0%BE%D0%B3%D0%BE%20%D1%81%D0%B8%D0%BC%D0%B2%D0%BE%D0%BB%D0%B0.png?alt=media&token=e8008edd-a627-47b0-81c2-060c6963014f)

\*\*\*\*

### **Frequently Asked Questions**

### **How to check argument separator?**

For Windows 10: 

* go to **Start &gt;type Control Panel  and press enter &gt; Region**
* click **Additional Settings**
* for **List Separator** check the argument. ****It must be the same as in RTD settings.

![](../../.gitbook/assets/regional_settings.png)

![](../../.gitbook/assets/regional2.jpg)

