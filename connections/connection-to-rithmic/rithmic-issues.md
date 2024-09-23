# Rithmic Issues

* **Market Data Connection Failed. Please contact the FCM/IB**
* [**No Level2 data for some symbols**](rithmic-issues.md#no-level2-data-for-some-symbols)
* [**Error: Only Admins Can Place Trades**](rithmic-issues.md#error-only-admins-can-place-trades)
* [**Error: No handle**](rithmic-issues.md#error-no-handle)
* [**Issue: No historical market data on a chart**](rithmic-issues.md#issue-no-historical-market-data-on-a-chart)
* [**Chart Data is incorrect or has gaps**](rithmic-issues.md#chart-data-is-incorrect-or-has-gaps)

## **Market Data Connection Failed. Please contact the FCM/IB**

Sometimes, when connecting to the Rithmic, you may see the error **"**_<mark style="background-color:green;">**Market Data Connection Failed**</mark>**".**_ Below we will describe possible reasons and solutions.

{% hint style="warning" %}
This error message is most commonly encountered by _**new Rithmic users for various reasons**_ and is not within the control of the Quantower platform.&#x20;
{% endhint %}

<figure><img src="../../.gitbook/assets/Starter_gotBdOHdgC.png" alt=""><figcaption><p>Rithmic error "Market Data Connection Login Failed"</p></figcaption></figure>

### Connection to Rithmic can be done in two ways:

* **Directly**, <mark style="color:green;">**without**</mark> using **RTrader Pro** platform. This allows only one platform to be connected.

<figure><img src="../../.gitbook/assets/image (384).png" alt=""><figcaption></figcaption></figure>

* <mark style="color:green;">**Through RTrader Pro**</mark>, using **Plugin Mode**, which lets you connect **multiple platforms at the same time (!)**.&#x20;

![Use Rithmic plugin mode for multiple access](<../../.gitbook/assets/image (352) (1) (1) (1).png>)

### Here are the most common reasons for connection errors:

* **Agreements not accepted**: You may have missed accepting the "_<mark style="background-color:orange;">Market Data Subscription Agreement</mark>_" or "_<mark style="background-color:orange;">Market Data Self-Certification</mark>_" during registration on Rithmic’s website or in RTrader Pro.\
  _<mark style="background-color:green;">**Solution:**</mark> Log in to the RTrader Pro platform and accept the agreements._
* **New account**: If your account was created less than an hour ago, **full activation can take 30 minutes to 1 hour**.\
  _<mark style="background-color:green;">**Solution:**</mark>_ _Log in to RTrader Pro. If the connection works, your account is fully activated._
*   **Wrong server, login & password**: Ensure you're connecting to the correct server and use correct login credentials without extra symbols (Apex, Topstep, or Rithmic).&#x20;

    _<mark style="background-color:green;">**Solution:**</mark>_ _Try switching servers that match your login. Check your login credentials._

<figure><img src="../../.gitbook/assets/image (370).png" alt=""><figcaption></figcaption></figure>

*   **RTrader Plugin issue**: If Quantower was previously connected via the RTrader Plugin and RTrader Pro isn’t currently running or the "<mark style="background-color:orange;">**Allow Plugins**</mark>" option is disabled, Quantower won’t connect.

    \
    _<mark style="background-color:green;">**Solution**</mark>** ****(several different options, not step-by-step):**_

    _1) start RTrader Pro in Allow Plugins mode and reconnect to your account in Quantower._

    _2) alternatively, try a direct connection by closing RTrader Pro, disabling the "**Use RTrader**" option in Quantower, and restarting Quantower._

![Plugin Mode in RTrader Pro is disabled but active in Quantower](<../../.gitbook/assets/image (351) (1) (1).png>)

*   **Direct connection limitation**: When using a direct connection (without RTrader Plugin), you cannot use the same login on multiple platforms at once. If you try, the first platform may disconnect, and the second will fail to connect.

    _<mark style="background-color:green;">**Solution:**</mark>_ _use RTrader Plugin mode for multiple connections or close all platforms and connect to Quantower directly._

![](<../../.gitbook/assets/image (345).png>)

* **Server unavailable**: If the Rithmic server is down, this error commonly occurs on weekends.\
  <mark style="background-color:green;">**Solution**</mark><mark style="background-color:green;">:</mark> _Wait until Sunday evening to try reconnecting._
* **Expired demo account**: Rithmic demo accounts are limited to 14 days. If you've used a demo before, you won’t be able to log in with a new demo username. Moreover, your account can be blocked by prop company because of drawdown limitation.
* **Persistent issues**: If you can't connect for several days, contact your broker or prop company.

If you’ve enabled "<mark style="background-color:green;">**Use RTrader Plugin**</mark>" in the connection settings but still can’t connect, check that you have more than one active session for market data.

![](<../../.gitbook/assets/image (100).png>)

***

## No Level2 data for some symbols

<figure><img src="../../.gitbook/assets/No level2 data in Quantower.png" alt=""><figcaption></figcaption></figure>

This problem can be because you do not have a subscription to this Level2 data. To check this, launch the **RTrader Pro platform** and open the **Order Book** panel.

If you don't have Bid/Ask values in the RTrader Pro platform, **you need to subscribe to this data via the support of your broker or prop company**. After that, you will see level 2 data in our platform as well.

<figure><img src="../../.gitbook/assets/No level2 data in Rithmic.png" alt=""><figcaption></figcaption></figure>

***

## Error: Only Admins Can Place Trades

**This means that the Evaluation account has failed and has been disabled.**&#x20;

It either means you have reached your Trailing Threshold Drawdown or that you have held a trade past 4:59 PM ET.

To resolve this issue, please get in touch with the support team of your Prop Trading company.

***

## Error: No handle

The 'No handle' error typically occurs if <mark style="background-color:green;">**your login is already in use**</mark> on another platform or a different PC.\
To resolve this issue, ensure that you are not logged in with your credentials anywhere else, neither in Rtrader Pro nor any other platform. This step is crucial to prevent simultaneous login conflicts and to address the error effectively.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

## Error: No trade routes

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

## Issue: No historical market data on a chart

Users may sometimes encounter a lack of historical market data for one or several trading instruments on their charts. This issue is _**often due to a problem with the data provider**_, typically Rithmic, for a specific server, or reaching the limit of tick data downloads.

{% hint style="warning" %}
**NOTE:** Rithmic has a weekly tick data download limit of 40 gigabytes. Exceeding this limit means no historical data until the next week. Real-time data will work correctly.
{% endhint %}

To diagnose and resolve this issue, follow these steps:

1. Check if the issue occurs with other trading instruments, especially standard futures contracts with month indications (e.g., ESH4, NQH4).

<figure><img src="../../.gitbook/assets/Screenshot_3 (2).png" alt=""><figcaption></figcaption></figure>

2. Reload data from the server by right-clicking on the chart and selecting '<mark style="background-color:orange;">**Reload history (server)**</mark>'.

<figure><img src="../../.gitbook/assets/Screenshot_4 (3).png" alt=""><figcaption></figcaption></figure>

3. If the problem persists, open the [<mark style="background-color:yellow;">**Event Log**</mark>](../../informational-panels/event-log.md) panel to view all types of error messages. If you see '<mark style="background-color:red;">**Permission Error**</mark>', confirm whether the issue is with Rithmic or your account.

<figure><img src="../../.gitbook/assets/Screenshot_2 (3).png" alt=""><figcaption></figcaption></figure>

4. Open (or install) the [<mark style="background-color:yellow;">**Rtrader Pro platform**</mark>](https://yyy3.rithmic.com/?page\_id=16), the official platform of Rithmic. Log in with your account and open the <mark style="background-color:orange;">**Chart panel**</mark> with the exact ticker, for example, **ESH4.CME**.

<figure><img src="../../.gitbook/assets/image (410).png" alt=""><figcaption></figcaption></figure>

5. If there is also no data on their chart, the issue likely lies with the Rithmic server. Contact support for your broker, prop trading company, or Rithmic directly. Include screenshots as evidence of the server-related issue.
6.  If your broker or prop firm confirms that you've reached the tick data download limit,&#x20;

    to avoid future blocks, we recommend:

    * Reducing the number of panels using numerous volume analysis tools (volume profiles, clusters).
    * Decreasing the depth of data on your charts (avoid loading more than 6 months of volume analysis data).
    * It is advisable to use the '**Reload data (server)**' option only when necessary and in moderation.

***

## Chart Data is incorrect or has gaps

Sometimes, non-market gaps can occur due to a weak Internet connection, a broken connection to your data provider, or other reasons. To solve this problem, **Right-click on the chart** and select **Reload history (server).**

<figure><img src="../../.gitbook/assets/QT SC 3.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
