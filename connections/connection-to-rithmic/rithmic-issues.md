# Rithmic Issues

* [**Market Data Connection Closed (Broken)**](rithmic-issues.md#market-data-connection-closed-broken)
* [**No Level2 data for some symbols**](rithmic-issues.md#no-level2-data-for-some-symbols)
* [**Error: Only Admins Can Place Trades**](rithmic-issues.md#error-only-admins-can-place-trades)
* [**Error: No handle**](rithmic-issues.md#error-no-handle)
* [**Issue: No historical market data on a chart**](rithmic-issues.md#issue-no-historical-market-data-on-a-chart)
* [**Chart Data is incorrect or has gaps**](rithmic-issues.md#chart-data-is-incorrect-or-has-gaps)

## **Market Data Connection Closed (Broken)**

Sometimes, when connecting to the Rithmic, you may see the error **"**_**Market Data Connection Closed (Broken)".**_ Below we will describe possible reasons and solutions.

{% hint style="warning" %}
This error message is most commonly encountered by _**new Rithmic users for various reasons**_ and is not within the control of the Quantower platform.&#x20;
{% endhint %}

![Rithmic error "Market Data Connection Closed" in Quantower](../../.gitbook/assets/connections-error-with-rithmic.png)

![Rithmic error "Market Data Connection Broken" in Quantower](<../../.gitbook/assets/image (348) (1) (1) (1).png>)

#### Connection to Rithmic can be done in two ways:

* directly, without using RTrader Pro platform. This approach allows only one platform to be connected.

<figure><img src="../../.gitbook/assets/image (384).png" alt=""><figcaption></figcaption></figure>

* through their RTrader Pro platform. This connection uses Plugin Mode and **allows you to connect multiple platforms at the same time (!)**

![Use Rithmic plugin mode for multiple access](<../../.gitbook/assets/image (352) (1) (1) (1).png>)

More often such error occurs for the following reasons:

*   You didn't accept agreements "_Market Data Subscription Agreement"_ and _"Market Data Self-Certification"_  during the registration on Rithmic's website or in R Trader platform. _We recommend connecting through **R Trader** or **R Trader Pro** platforms to check your account._

    _**Solution:** accept agreements in RTrader Pro platform_
*   A new account was created less than an hour ago. Usually, the **full activation of a new account takes from 30 minutes to 1 hour**.

    _**Solution:**_ _open RTrader Pro platform and connect with your login. If the connection is successful, then your account is active in Rithmic system_
*   Make sure that your login matches the correct server&#x20;

    _**Solution:**_ _try to use another server according to your login (Apex, Topstep or Rithmic itself)_

<figure><img src="../../.gitbook/assets/image (370).png" alt=""><figcaption></figcaption></figure>

*   If Quantower was connected to Rithmic before via the RTrader Plugin (i.e. the checkbox Use RTrader is active), and at the moment the RTrader Pro platform is not connected or the **Allow Plugins** option is not active there, then Quantower will not be able to connect.

    _**Solution (several different options, not step-by-step):**_

    _1) start RTrader Pro platform with **Allow Plugins** mode and connect again to your account in Quantower_

    _2) try to connect to Rithmic as a direct connection: close RTrader Pro platform, disable **Use Rtrader** option in Quantower settings and restart Quantower. After start Quantower again and connect to your account as a direct connection_

![Plugin Mode in RTrader Pro is disabled but active in Quantower](<../../.gitbook/assets/image (351) (1) (1).png>)

*   In the case of a direct connection (without RTrader Plugin mode), you cannot use the same login on different platforms at the same time. The connection can be only one login on one platform (!).&#x20;

    When trying to connect with one login on different platforms, it can log out from the first platform (which was connected), but the login on the second platform will not be successfully connected (on which we are trying to log in).

    _**Solution:** use RTrader Plugin mode for multiple connections or close all platforms and connect via Quantower as direct connection (without Rtrader plugin mode)_

![](<../../.gitbook/assets/image (345).png>)

* The error can be encountered because the Rithmic server is unavailable to be connected to. This error commonly can be encountered over the weekend. In this case, it is best to wait until Sunday evening to see if you can connect to determine if this is the problem or there is some other problem.
* Rithmic demo accounts are limited to 14 days per exchange guidelines on providing live, streaming data. If you have used a Rithmic demo previously you will _not_ be able to login with a new Rithmic demo Username.
* If you are unable to connect within a few days, you need to contact your broker about this issue.

If you enable Use RTrader plugin in Connection Settings and still can not connect to Rithmic, please check that you have more than 1 active session for Market data.

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
