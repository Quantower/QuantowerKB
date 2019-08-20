# Excel and RTD function

Start from the version 1.39 Quantower supports RealTimeData \(RTD\) for sending data and other market information to Microsoft Excel®. This feature opens up many opportunities for creating custom displays and other ways to better manage your workflow. 

RTD is a newer protocol that offers several advantages over DDE, including more flexibility and better performance and reliability.

Here is the General Syntax for getting symbol info via RTD function:

![](../.gitbook/assets/screenshot_128%20%281%29.png)

## **How to activate RTD function in Quantower platform**

Go to the [**General Settings**](../getting-started/general-settings.md) of the platform, then to _section **Excel RTD**_ and tick off _**"Enable Microsoft Excel RTD"**_

![Activation of RTD function in Quantower](../.gitbook/assets/assets_-ld6fsrvq3jgwjig6o7r_-lme4wbmrbk0ai3rafld_-lmeyazmdvqpbsftpr9b_rtd.png)

Also in the settings there are two important settings:

* **Custom RTD formula name** — depending on the language of your operating system, the name of the RTD function in Excel may be called differently. The original name of the function in the English version of Excel is RTD, but for Russuian version it's called as "ДРВ".
* **Custom argument separator** — the separator that participates in the formula. It depends on the localization of your operating system. Get to know [how to check argument separator in your system](excel-rtd-trading.md#how-to-check-argument-separator).



## **Frequently Asked Questions**

### **How to check argument separator?**

For Windows 7:

* go to **Start &gt; Control Panel &gt; Regional and Language Options**
* Click on **Formats Tab** **&gt; Additional Settings**
* for **List Separator** check the argument. ****It must be the same as in RTD settings.

For Windows 10: 

* go to **Start &gt;type Control Panel  and press enter &gt; Region**
* click **Additional Settings**
* for **List Separator** check the argument. ****It must be the same as in RTD settings.

![](../.gitbook/assets/regional_settings.png)

![](../.gitbook/assets/regional2.jpg)





