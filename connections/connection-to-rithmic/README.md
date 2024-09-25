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
* [**Problems during the connection to Rithmic**](./#problems-during-the-connection-to-rithmic)

## Connection for Existed Accounts

* [**Download and install R Trader Pro**](https://www.rithmic.com/rtraderpro) from Rithmic official website.
* Open the connection manager, select **Rithmic** and enter your credentials. Make sure that you've selected the correct server. By default, the Rithmic Paper Chicago server is set for demo accounts and the Rithmic Aurora Chicago server is set for real accounts.
* _<mark style="background-color:orange;">**{Optionaly}**</mark>_ Click on **Connection Settings** and **activate Use RTrader** option to avoid additional fees for subscription to market data. Below, you can find more information on [how to connect and trade with an account via **Plugin Mode**](./#connection-via-plugin-mode).
* Enter your login and password and click **Connect.**

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Enter login data for connection to Rithmic</p></figcaption></figure>

{% hint style="info" %}
Starting from May 1, the [CME exchange сhanged the rules for determining a professional market participant](http://yyy3.rithmic.com/?p=1069), and as a result, increased the fee for the market data. To correctly define the professional participant, Ritmic has changed the connection parameters in their platform, as well as in API for platforms such as Quantower.

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

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Enable Market by Order MBO data for Rithmic in Quantower platform</p></figcaption></figure>

</div>

After activation, you can see this data in the DOM Trader panel.&#x20;

Open **Settings** in the DOM trader panel -> **Columns** -> **Bids/Ask** (if you use split mode or **Bids** and **Asks** as single columns) -> **Size coloring scheme** -> **MBO.**  Also, you can set **Filter orders more than (MBO)** if you want to see orders with a certain size.

![Activating MBO data in Quantower platform](<../../.gitbook/assets/image (353) (1).png>)

![Visual comparison between Market by Oder (MBO) and Market by Price (MBP)](<../../.gitbook/assets/MBO vs MBP.png>)

## **Problems during the connection to Rithmic**

{% hint style="info" %}
Below is a link where we've outlined the most common mistakes our users might encounter when working with Rithmic servers. This includes both the original Rithmic servers and those accessed through various broker companies. [**Link to Rithmic Issues**](https://help.quantower.com/quantower/connections/connection-to-rithmic/rithmic-issues).
{% endhint %}
