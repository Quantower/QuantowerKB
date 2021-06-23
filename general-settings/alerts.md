---
description: Setting up alerts in Quantower
---

# Alerts

**Alert** on the financial market is a standard signal that notifies you when the price reaches a certain level on the chart, pre-set in the settings. A notification comes in the form of: sound, a notification opened on the monitor, a [telegram](../miscellaneous-panels/quantower-telegram-bot.md) email sent instantly as soon as the price has approached a specific value.

![](../.gitbook/assets/image%20%28210%29.png)

**Alerts** are already available by default in any Quantower. You can choose sound files for the Alerts from the offered ones or set your own signal that you like as a soundtrack. All the other options for alerts in Quantower, relevant to the usual graphic shapes - color change, drag and drop, double click menu call, etc.

### How to set up Quantower Alerts on chart

In the **alert settings,** you can specify single or multiple triggers. To make sure you don't miss an Alert, I leave the multiple triggers. This can be annoying at times. 

![](../.gitbook/assets/124.gif)

### Managing the alerts in Quantower

Sometimes you will have a lot of alerts. Use the Object manager to manage them. A double-click on an Alert will move you to the point on the chart where that Alert is set.You can also edit it or delete unnecessary alerts.

{% hint style="danger" %}
**Important:** The alert will only work on an open chart. If you switch the chart on which you set the alert from one symbol to another alert will not work
{% endhint %}

### How to set up Quantower Alerts on watchlist

[Watchlist](../analytics-panels/watchlist.md) panel shows brief pricing information on selected instruments, which you can group into lists. There are two ways to get to the settings menu. 

* From the menu of this window, select Setup Actions
* Right-click on the desired symbol and find Alert in the menu

![](../.gitbook/assets/animaciya-3-.gif)

And so let's look at how to set up an alert. To do this, we need to do a few actions. Activate the alert / Enable Action Give a name to the alert. Specify the symbol of interest. Add a condition. Select an action when the condition occurs

![](../.gitbook/assets/animaciya-2-.gif)



{% hint style="danger" %}
Do not forget to activate the Enable Action button
{% endhint %}

### How to copy conditions of Alerts

![](../.gitbook/assets/image%20%28215%29.png)

You can also copy the Alert state and change only some parameters, such as the symbol and its values

### 5 steps for working with alerts on a chart

{% hint style="danger" %}
**Important:** The alert will only work on an open chart. If you switch the chart on which you set the alert from one symbol to another alert will not work

To get around this limitation, we will make a 10-step pattern
{% endhint %}

1\) Create a Watchlist and add the necessary coins to it. In fact, It is recommend no more than 20 coins. Better yet, only the ones that we are going to trade today or in the near term.  Assign a color to this panel, Choose any of the available colors.



![](../.gitbook/assets/image%20%28247%29.png)

2\) We need to have a chart on which we spend analytics, levels and alerts. Let us call it an analytical diagram. For each of it will be its own set-up as desired. We need to associate the analysis chart with the Watchlis by color. In my case I chose green. 

3\) Create a simple chart and remove all the controls and charts from it as much as possible. Let's call it a signal chart.  Synchronize the objects on the signal and analysis chart. Manually set a coin or symbol from Watclist on the Signal Chart. 

![](../.gitbook/assets/image%20%28248%29.png)

4\) Duplicate this signal chart as many times as there are symbols in Watclist and set other coins on them. Create a group of tabs from the resulting Signal Graphs. 

![](../.gitbook/assets/image%20%28251%29.png)

Go to the analytical chart and analyze and set levels and alerts. All alerts must be duplicated in our group of charts for a particular coin. We check that all levels are set on the signal chart. 

![](../.gitbook/assets/image%20%28250%29.png)

5\) Wait for the alert to trigger, evaluate the market action and earn profits

{% hint style="success" %}
So we have Watchllist for fast switching between charts. Analysis on our favorite chart and notification signals from our levels.
{% endhint %}



