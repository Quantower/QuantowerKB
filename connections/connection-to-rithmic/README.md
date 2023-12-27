---
description: >-
  Rithmic technology provides access for trading futures and options on CME,
  CBOT, NYMEX and other exchanges. Full market depth, reliable data and great
  execution are main features of Rithmic.
---

# Connection to Rithmic

To connect Quantower to a broker that uses Rithmic technology, it is sufficient to have (or create a new) account.

* [**Connection for Existed Accounts**](./#connection-for-existed-accounts)
* [**Connection for New Accounts**](./#connection-for-new-accounts)
* [**Connection via RTrader Plugin Mode**](./#connection-via-rtrader-plugin-mode)
* [**How to activate Market by Order (MBO) data**](./#how-to-activate-market-by-order-mbo-data)
* [**Problems during the connection to Rithmic**](./#problems-during-the-connection-to-rithmic)\
  &#x20;<mark style="color:blue;">**-**</mark> [_**Market Data Connection Closed (Broken)**_](./#market-data-connection-closed-broken)\
  &#x20;<mark style="color:blue;">**-**</mark> [_**No Level2 data for some symbols**_](./#no-level2-data-for-some-symbols)\
  &#x20;<mark style="color:blue;">**-**</mark> [_**ERROR: Only Admins Can Place Trades**_](./#error-only-admins-can-place-trades)

## Connection for Existed Accounts

* [**Download and install R Trader Pro**](http://yyy3.rithmic.com/?page\_id=16) from Rithmic official website.
* Open the connection manager, select **Rithmic** and enter your credentials. Make sure that you've selected the correct server. By default, the Rithmic Paper Chicago server is set for demo accounts and the Rithmic Aurora Chicago server is set for real accounts.
* _<mark style="background-color:orange;">**{Optionaly}**</mark>_ Click on **Connection Settings** and **activate Use RTrader** option to avoid additional fees for subscription to market data. Below, you can find more information on [how to connect and trade with an account via **Plugin Mode**](./#connection-via-plugin-mode).
* Enter your login and password and click **Connect.**

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Enter login data for connection to Rithmic</p></figcaption></figure>

{% hint style="info" %}
Starting from May 1, the [CME exchange сhanged the rules for determining a professional market participant](http://yyy3.rithmic.com/?p=1069), and as a result, increased the fee for the market data. In order to correctly define the professional participant, Ritmic has changed the connection parameters in their platform, as well as in API for platforms such as Quantower.

To avoid additional fees for subscription to market data, a trader needs to login through the R Trader Pro platform and activate the setting in Quantower, which is called **Use RTrader**.
{% endhint %}

<div data-full-width="false">

<figure><img src="../../.gitbook/assets/Rithmic plugin mode.gif" alt=""><figcaption><p>Activate Use RTrader option to avoid additonal fees for subscription to market data</p></figcaption></figure>

</div>

## Creating a New Accounts and further connection

* [**Create a new demo**](https://rithmic.com/demo.html#sign-up) or open a real account with any broker supporting Rithmic technology, accept agreements, and start using our platform.

{% embed url="https://youtu.be/3kpiOCiqE5Q" %}

* To register [**Rithmic Demo**](https://rithmic.com/demo.html#sign-up) go to their official website or follow this [link](https://rithmic.com/demo.html#sign-up)
* Fill in all the required fields
* Accept _**"Market Data Subscription Agreement"**_ and _"**Market Data Self-Certification"**_
* The account will be activated within 30-60 minutes.

## Connection via RTrader Plugin Mode

Please keep in mind that connecting to Rithmic using the plugin mode requires the following steps:

* RtraderPro platform must be installed and running on your computer.
* RtraderPro platform must be enabled in the Plugin mode and use the same credentials and server as in Quantower.
* Quantower must also be enabled in the Plugin mode and use the same Rithmic credentials and server.
* The first step is to launch the RtraderPro platform with Plugin mode. Once you've successfully logged in there, you can then connect using the Quantower platform.
* Make sure your firewall is not blocking the connection from Quantower to RtraderPro.

Also, note that the Plugin Mode allows you to connect multiple different platforms simultaneously using the same Rithmic credentials.

<figure><img src="../../.gitbook/assets/Rithmic plugin mode (1).gif" alt=""><figcaption></figcaption></figure>

## **How to activate Market by Order (MBO) data**

**Market by Order (MBO) data** shows the order size of an individual position inside the level2 data for a certain price. To activate the displaying of this data, open the Connection settings and tick on "**Enable 'Market by Order' (MBO) mode**".

<div data-full-width="true">

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Enable Market by Order MBO data for Rithmic in Quantower platform</p></figcaption></figure>

</div>

After activation, you can see this data in the DOM Trader panel.&#x20;

Open **Settings** in the DOM trader panel -> **Columns** -> **Bids/Ask** (if you use split mode or **Bids** and **Asks** as single columns) -> **Size coloring scheme** -> **MBO.**  Also, you can set **Filter orders more than (MBO)** if you want to see orders with a certain size.

![Activating MBO data in Quantower platform](<../../.gitbook/assets/image (353) (1).png>)

![Visual comparison between Market by Oder (MBO) and Market by Price (MBP)](<../../.gitbook/assets/MBO vs MBP.png>)

## **Problems during the connection to Rithmic**

### **Market Data Connection Closed (Broken)**

Sometimes, when connecting to the Rithmic, you may see the error **"**_**Market Data Connection Closed (Broken)".**_ Below we will describe possible reasons and solutions.

{% hint style="warning" %}
This error message is most commonly encountered by _**new Rithmic users for various reasons**_ and is not within the control of the Quantower platform.&#x20;
{% endhint %}

![Rithmic error "Market Data Connection Closed" in Quantower](../../.gitbook/assets/connections-error-with-rithmic.png)

![Rithmic error "Market Data Connection Broken" in Quantower](<../../.gitbook/assets/image (348) (1) (1) (1).png>)

#### Connection to Rithmic can be done in two ways:

* directly, without using RTrader Pro platform. This approach allows only one platform to be connected.

<figure><img src="../../.gitbook/assets/image (385).png" alt=""><figcaption></figcaption></figure>

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

### No Level2 data for some symbols

This problem can be due to the fact that you do not have a subscription to this Level2 data. To check this, launch the **RTrader Pro platform** and open the **Order Book** panel.

If you don't have Bid/Ask values in the RTrader platform, you need to subscribe to this data via Rithmic's support. After that, you will see level2 data in our platform as well.&#x20;

![](<../../.gitbook/assets/image (297).png>)

### ERROR: Only Admins Can Place Trades

This means that the Evaluation account has been failed and has been disabled.&#x20;

It either means you have reached your Trailing Threshold Drawdown or that you have held a trade past 4:59 PM ET.

To resolve this issue, please contact support team of your Prop Trading company
