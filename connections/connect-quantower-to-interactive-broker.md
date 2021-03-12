---
description: >-
  Follow the steps in this guide to connect the Quantower platform to the
  Interactive Brokers. The manual contains a detailed description, which will
  allow you to correctly configure the connection.
---

# Connection to Interactive Brokers

* \*\*\*\*[**Data Limitations**](connect-quantower-to-interactive-broker.md#data-limitations)\*\*\*\*
* \*\*\*\*[**Necessary steps for successful connection to Quantower**](connect-quantower-to-interactive-broker.md#necessary-steps-for-successful-connection-to-quantower)\*\*\*\*
* \*\*\*\*[**Problems during the connection to Interactive Brokers**](connect-quantower-to-interactive-broker.md#problems-during-the-connection-to-interactive-brokers)\*\*\*\*

### Data Limitations

Interactive Brokers places the following limitations on real-time and historical data accessible to 3rd party applications

* **Pacing Violations** – TWS limits the number of requests for data. If too many requests for data occur in a short period of time, you may see error messages indicating “Pacing Violation”. If this happens you may need to wait a few minutes before trying to load data again. 
* **Real-Time Quotes** – TWS does impose limits on the number of active tickers \(typically around 100\). Additional booster packs can be purchased from IB to work around this issue: [Booster Packs](https://www.interactivebrokers.com/en/index.php?f=14193). 
* **Delayed Data Not Supported** – TWS does not provide access to delayed historical data and quotes. 

For more details on these limitations see [IB Data Limitations](https://interactivebrokers.github.io/tws-api/historical_limitations.html#gsc.tab=0).

{% hint style="warning" %}
* IB does not currently offer full depth market data for futures.
* Market data updates are not frequent; therefore, we do not recommend using IB data \(instead we recommend using dxFeed or Iqfeed as market data provider\).
{% endhint %}

### Necessary steps for a successful connection to Quantower

This guide will help you to configure the connection to the Interactive Brokers and start working on Quantower platform.

{% embed url="https://youtu.be/dhz2OkwfDSg" caption="Video connection guide to Interactive Brokers" %}

1. [**Download**](https://www.quantower.com/) ****and install Quantower trading platform \(if you haven’t it yet\) of an appropriate version \(32 bit or 64 bit\), and make sure that your PC complies with the [**minimum requirements**](../getting-started/installation.md#pc-requirements) 
2. After installing the platform, you need to create a [**demo**](https://www.interactivebrokers.co.uk/en/index.php?f=1286) or [**real account**](https://www.interactivebrokers.com/en/home.php) by clicking the appropriate links on the Interactive Brokers official website.

![Creating a demo or real account on Interactive Brokers](../.gitbook/assets/create-demo-and-real-account-interactive-brokers.png)

     3. Download and install IB Software — [**TWS \(Trader Workstation\)**](https://www.interactivebrokers.co.uk/en/index.php?f=14099#tws-software) or [**IB Gateway**](https://www.interactivebrokers.co.uk/en/index.php?f=16454) on their website. The difference between IB Gateway and TWS is that IB Gateway has a lighter and less sophisticated graphical user interface \(GUI\) than TWS.

![Download Trader Workstation \(TWS\) or IB Gateway](../.gitbook/assets/download-tws-or-ib-gateway.png)

     4.  Launch TWS or IB Gateway and enter your **User name** and **Password** into it, that you received from the broker and click **Login** button.

{% hint style="warning" %}
For **IB Gateway** in the API Type section select **IB API** only!
{% endhint %}

![Select API type and enter Login and password for IB Gateway](../.gitbook/assets/ib-gateway-credentials.png)

     5. Once you are logged in, open the additional settings in IB Gateway or TWS:  **Configure**-&gt; **Settings**. Select **API** section - &gt;  **Precautions** and activate all checkboxes.

Also necessary in the **Settings** section deactivate the **Read-Only API** to perform trading operations.

![Activate all checkboxes in the IB Gateway or TWS API settings](../.gitbook/assets/api-settings-for-ib.png)

     6. If you connect via the TWS platform, please select **API** section - &gt; **Settings** and check to **Enable ActiveX and Socket Clients** box as well ****uncheck **Read-Only API**:

![Diactivate Read-Only API and check Socket Clients in TWS platform](../.gitbook/assets/trader-workstation-api-settings.png)

     7. Open the [**Connections Manager**](connections-manager.md) in Quantower platform, select Interactive Brokers connection and click on the **CONNECT** button. 

![Click on the Connect button once you are logged in to TWS or IB Gateway](../.gitbook/assets/connections-manager-for-ib.png)

### Problems during the connection to Interactive Brokers

* _**Wrong Connection Parameters**_
* _**Trader Workstation is not running \(below\)**_
* _**The Price Does Not Conform to the minimum price variation for this contract \(FOREX symbols\)**_

There may be some problems during the connection to Interactive Brokers, for example, _**Wrong Connection Parameters**_

![Wrong parameteres during connection to Interactive Brokers](../.gitbook/assets/connections-manager-for-ib_error.png)

In this case, you need to check the connection settings in our platform and in the TWS platform \(or IB Gateway\). In our platform, go to the **Connection Settings.**

![Connection settings in Quantower for Interactive Brokers](../.gitbook/assets/connections-manager-for-ib_settings.png)

Select the application through which you are connecting  — TWS platform or IB Gateway.

![Select the necessary connection port type](../.gitbook/assets/connection-settings-for-ib.png)

If the problem persists even after choosing the right application, you need to configure the _**Socket port**_ in TWS \(or IB Gateway\) and Quantower.

![This Socket port in TWS \(or IB gateway\) should be the same as in Quantower](../.gitbook/assets/socket-port.png)

Select the _**Custom**_ connection port type in the Connection settings of Quantower and set the _**Port Value**_

![This Socket port in Quantower should be the same as in TWS \(or IB gateway\)](../.gitbook/assets/custom-socket-port.png)

    2. _**Trader Workstation is not running**_

![Trader Workstation is not running. Please launch it to connect to IB](../.gitbook/assets/connections-manager-for-ib_tws_error.png)

Connection to Interactive Brokers is made through their TWS trading platform or the IB Gateway application. To successfully connect to IB you need to run their applications.

If you have any other problems during the connection to Interactive Brokers, please contact us in support and we will help you. [https://www.quantower.com/contact-us](https://www.quantower.com/contact-us)

3. _**The Price Does Not Conform to the minimum price variation for this contract \(FOREX symbols\)**_

By default, placing orders on Forex pairs in IB is carried out at prices equal to 1/2 pip. Like on the screenshot below:

![](../.gitbook/assets/image%20%2899%29.png)

If you place orders in Quantower at prices between those specified, for example 1.19382, you will get a message: _**The Price Does Not Conform to the minimum price variation for this contract \(FOREX symbols\).**_ 

To solve this problem and to be able to place orders at any desired prices, you need to activate the setting in the TWS platform \(or in IB Gateway\)

![](../.gitbook/assets/image%20%2898%29.png)



