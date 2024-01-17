# Connection to Topstep

* [**Possible issues with connection to Topstep account**](connection-to-topstep.md#possible-issues-with-connection-to-topstep-account-and-trading-issues)
* [**What is included in Quantower for free?**](connection-to-topstep.md#included)
* [**Most popular trading questions**](connection-to-topstep.md#most-popular-trading-questions)

***

In order to begin your work with [**Topstep**](https://www.topstep.com/), you must first register on their website and pay for access to a trading account (combine).

Once you have paid, please log in to your personal account on the Topstep website using the login and password you provided during the registration process.

<figure><img src="../.gitbook/assets/image (366).png" alt=""><figcaption><p>Login to your Topstep personal cabinet</p></figcaption></figure>

When you access the general section of your personal account, you'll find the main parameters of your account, such as your current balance, Net P\&L, and performance chart.

To access a trading account through the Quantower platform, you need to click on the icon for additional account information. Your login and password details will be displayed there.

{% hint style="warning" %}
**Please note that the password for your Topstep personal account is different from the password required to access your trading account on the platform.**
{% endhint %}

<figure><img src="../.gitbook/assets/image (367).png" alt=""><figcaption></figcaption></figure>

***

## Possible issues with connection to Topstep account & trading issues

* <mark style="background-color:red;">**Market Data Connection Login Failed. Please contact the FCM/IB who issued your login id for assistance.**</mark>

The most common issue encountered while attempting to log in to the platform is an error. This may be caused by several reasons:

**1)** Please ensure that you are entering the <mark style="background-color:blue;">**correct Login & Password**</mark> to access the platform, as it is not the same as the one used for logging into your personal account.

{% hint style="info" %}
You can find the **correct password on your personal cabinet**, as we have shown previously.
{% endhint %}

{% hint style="warning" %}
**If you selected the Tradovate platform during registration, unfortunately, you won't be able to connect to other platforms, including Quantower.** To change your selection and connect to Quantower, please contact Topstep's support team. They will assist you in updating your platform choice to ensure compatibility with Quantower.
{% endhint %}

**2)** Please ensure that you have chosen the correct server for connection, as it is crucial to use Topstep (Tostep trader Chicago Area, Topstep trader Europe, etc.)

**3)** Please make sure your account is active. To do this, open the Rtrader Pro platform and try logging in using your credentials. Make sure you've selected the correct server. If you don't have Rtrader Pro, you can [**download it**](https://yyy3.rithmic.com/?page\_id=16) from the official Rithmic website.

<figure><img src="../.gitbook/assets/image (3) (1) (1).png" alt=""><figcaption><p>Market Data Connection Login Failed</p></figcaption></figure>

**4)** For new users, please make sure to **sign two agreements first**. You can easily do this in the Rtrader Pro platform.

<figure><img src="../.gitbook/assets/Image 2023-08-03 18.33.50.png" alt=""><figcaption><p>Unsigned Agreements in Rtrader Pro platform</p></figcaption></figure>

* <mark style="background-color:red;">**Username & Password are Not Available (N/A)**</mark>

If your Username and Password are not yet available (N/A), please contact Tosptep support. Typically, the full account activation takes 1-2 business days.

<figure><img src="../.gitbook/assets/image (372).png" alt=""><figcaption><p>Username &#x26; Password are Not Available (N/A)</p></figcaption></figure>

* <mark style="background-color:red;">**No symbols found at Topstep**</mark>

<figure><img src="../.gitbook/assets/image (371).png" alt=""><figcaption><p>No symbols found at Topstep</p></figcaption></figure>

This error occurs when you were able to connect to your account, but at the moment it is not yet fully activated by Topstep. You need to contact their support with your username and account number in order for them to activate your account to receive market data.

* <mark style="background-color:red;">**Can not select an account for trading**</mark>

Sometimes users may encounter an issue of not having a trading account. Even though the platform connection is successful and the market data subscription is active, trading operations are not possible.

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Trading account is not available</p></figcaption></figure>

Most likely, your account is not fully activated. We recommend reaching out to Topstep support to resolve this matter. They will be able to assist you and ensure your account is fully activated for trading.

***

## **What is included in Quantower for free?** <a href="#included" id="included"></a>

**Topstep accounts **<mark style="background-color:green;">**will be provided**</mark>** with the Premium Feature Bundle for free:**

* [**DOM Surface**](../analytics-panels/dom-surface.md) (_requires Level2 data subscription_)
* [**TPO Chart**](../analytics-panels/tpo-chart.md)
* [**Volume Analysis Tools**](../analytics-panels/chart/volume-analysis-tools/)
* **Charting** (Maximum 2 indicators per chart)
* [**Copy Trading**](../trading-panels/copy-trading.md) (_works only under 1 login where a trader has multiple accounts_)

**Topstep accounts **<mark style="background-color:red;">**do not provide**</mark>** the following:**

* [**Market Replay**](../trading-panels/history-player.md) (requires a subscription to [Advanced Features license](https://www.quantower.com/advancedfeatures) on Quantower)
* [**Strategy Manager**](../quantower-algo/strategies-manager.md)
* [**Strategy Runner**](../quantower-algo/strategy-runner.md)
* [**Trading Simulator**](../trading-panels/trading-simulator.md)
* [**Power Trades**](../analytics-panels/chart/power-trades.md) (requires a subscription to [Power Trades license](https://www.quantower.com/pricing#extensions) on Quantower)
* [**Local order strategies**](https://help.quantower.com/quantower/trading-panels/order-entry/order-placing-strategies/local-sl-tp) (requires a subscription to [Advanced Features license](https://www.quantower.com/advancedfeatures) on Quantower)



## Most popular trading questions:

<details>

<summary>How to set custom trading sessions for particular symbols?</summary>

To create and manage trading sessions, you'll need to use the [**Sessions Manager**](../miscellaneous-panels/sessions-manager.md). By default, the platform comes pre-configured with trading sessions for major instruments (ES, NQ, CL) and is active for CQG and Rithmic connections.

To select a specific session on the chart, go to <mark style="background-color:blue;">**Chart settings -> View -> Sessions template**</mark>. From the dropdown list, choose the session you need.&#x20;

[_**More details you can find in this guide.**_](https://help.quantower.com/quantower/miscellaneous-panels/sessions-manager#how-to-set-custom-trading-sessions-for-futures-on-cqg-rithmic)

<img src="../.gitbook/assets/image (377).png" alt="" data-size="original">\


</details>

<details>

<summary>How to show/hide RTH or ETH sessions on the chart?</summary>

Sometimes, you may want to display data on the chart only for **RTH (Regular Trading Hours)** or **ETH (Extended Trading Hours)** session and hide all data that falls outside the specified session time. To do this, open the chart settings, go to the View section, and **uncheck the "**<mark style="background-color:green;">**Show out of session history**</mark>**"** option. This way, you'll see only the data relevant to the selected session.

<img src="../.gitbook/assets/image (373).png" alt="Uncheck the &#x22;Show out of session history&#x22; option to display RTH or ETH session" data-size="original">

</details>

<details>

<summary>How to place trades on Micro futures (MES) from the major futures (ES)?</summary>

Quantower allows traders to execute trades on micro futures from the chart of the main futures contract. For example, you can analyze the ES chart and place orders directly from it, but these orders will be automatically routed to the micro futures contract MES.

To achieve this, we recommend using the [**Symbol Mapping**](../miscellaneous-panels/symbol-mapping-manager.md#how-to-create-a-mapping-between-two-symbols) panel. Setting up the mapping takes just a few clicks and is thoroughly explained in our documentation.

[**How to create a mapping between Mini and Micro symbols (ES and MES) on the same connection (Rithmic or CQG only)**](../miscellaneous-panels/symbol-mapping-manager.md#how-to-create-a-mapping-between-mini-and-micro-symbols-es-and-mes-on-the-same-connection-rithmic-or)**.**

What's even more exciting is that you can configure mapping not only within one connection (Rithmic or CQG) but also across different connections (like dxFeed + Interactive Brokers).

</details>

<details>

<summary>Why Quantower does lost a connection to Rithmic after the Market closed?</summary>



</details>

<details>

<summary>How to place OCO orders?</summary>

[https://www.youtube.com/watch?v=GrJBUYSxvHE](https://www.youtube.com/watch?v=GrJBUYSxvHE)

</details>

<details>

<summary>How to place Bracket orders?</summary>



</details>

<details>

<summary>Why I can not add more than 2 indicators?</summary>

**Topstep accounts **<mark style="background-color:green;">**will be provided**</mark>** with the Premium Feature Bundle for free:**

* [**DOM Surface**](../analytics-panels/dom-surface.md) (_requires Level2 data subscription_)
* [**TPO Chart**](../analytics-panels/tpo-chart.md)
* [**Volume Analysis Tools**](../analytics-panels/chart/volume-analysis-tools/)
* **Charting** (Maximum 2 indicators per chart)
* [**Copy Trading**](../trading-panels/copy-trading.md) (_works only under 1 login where a trader has multiple accounts_)

</details>

<details>

<summary>Is there a fee for copy trading?</summary>

Topstep traders can enjoy free Copy Trading, which operates under a single login that includes multiple accounts.

</details>

<details>

<summary>How to enable cluster chart?</summary>

Before activating a cluster chart, you need to enable the Volume Analysis Toolbar. To do this, in the upper right corner of the chart panel, click on the "_**Magnifier**_" icon. A toolbar with Volume Analysis tools will appear at the bottom of the chart.\
\
[_**More details you can find in this guide**_](https://help.quantower.com/quantower/analytics-panels/chart/volume-analysis-tools/cluster-chart)

<img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1).png" alt="" data-size="original">

</details>
