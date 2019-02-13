---
description: >-
  Follow the steps in this guide to connect the Quantower platform to the
  Interactive Brokers. The manual contains a detailed description, which will
  allow you to correctly configure the connection.
---

# Connection to Interactive Brokers

### Necessary steps for successful connection

This guide will help you to configure the connection to the Interactive Brokers and start working on Quantower platform.

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

     5. Once you are logged in, open the additional settings in IB Gateway or TWS:  **Configure**-&gt; **Settings**. Select **API** section - &gt;  **Precautions** and activate all checkboxes

![Activate all checkboxes in the IB Gateway or TWS API settings](../.gitbook/assets/api-settings-for-ib.png)

     6. Open the [**Connections Manager**](connections-manager.md) in Quantower platform, select Interactive Brokers connection and click on the **CONNECT** button. 

![Click on the Connect button once you are logged in to TWS or IB Gateway](../.gitbook/assets/connections-manager-for-ib.png)

### Problems during the connection to Interactive Brokers

There may be some problems during the connection to Interactive Brokers, for example _**Wrong Connection Parameters**_

![Wrong parameteres during connection to Interactive Brokers](../.gitbook/assets/connections-manager-for-ib_error.png)

In this case, you need to check the connection settings in our platform and in the TWS platform \(or IB Gateway\). In our platform, go to the **Connection Settings.**

![Connection settings in Quantower for Interactive Brokers](../.gitbook/assets/connections-manager-for-ib_settings.png)

Select the application through which you are connecting  — TWS platform or IB Gateway.

![Select the necessary connection port type](../.gitbook/assets/connection-settings-for-ib.png)

