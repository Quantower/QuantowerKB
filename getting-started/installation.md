---
description: System requirements and 3 simple steps to successfully install the platform
---

# Installation

* [**System Requirements**](installation.md#pc-requirements)
* [**Installation Steps**](installation.md#installation-steps)
* [**Uninstalling**](installation.md#uninstall)

***

After downloading the [**Quantower platform**](https://www.quantower.com/download) from the official website, you can begin the installation process. It's important to understand the differences between the Quantower "installation process" and the default Windows® install process that most users are familiar with.

{% embed url="https://youtu.be/155Ha6Rku0E" %}

{% hint style="success" %}
Quantower does not copy its files to the system folders (AppData or Program Files) of the OS, nor does write changes to the system registry
{% endhint %}

What does it mean? The program doesn't violate the integrity of the OS, and in case of removal, it will not leave any prints of its presence on your computer. Quantower’s "installer" literally extracts files to the user-specified folder.

With this approach, you can save the Quantower on a removable drive and use it as a portable application on any other computer. This is especially useful when you need to transfer Quantower along with all its settings to a different PC. Copy the Quantower folder and paste it where you want it.

### PC requirements

{% hint style="info" %}
* Windows 10, 11
* [.NET 7](https://dotnet.microsoft.com/en-us/download/dotnet/7.0) or [.NET 8](https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/runtime-desktop-8.0.1-windows-x64-installer). In most cases, the platform will ask to update .NET to the latest version from the Microsoft official website.
* Available disk space — 1 GB (depends on the volume of loaded history)
* **The hardware requirements for Quantower depend upon what you are doing with it.** Most desktop systems can run Quantower without any difficulty.&#x20;
* The following hardware specifications are very much recommended for a fast system: 16 GB RAM, a minimum of 4-core CPU, and an SSD (solid-state drive).
{% endhint %}

{% hint style="warning" %}
**Microsoft has officially stopped supporting Windows 8 and Windows 7**. Therefore, the platform may not start or may work incorrectly. [For more information on supported versions, please check the official Microsoft website.](https://support.microsoft.com/en-us/help/13853/windows-lifecycle-fact-sheet)\
\
We recommend using Windows 10 or 11.
{% endhint %}

### Installation steps

![Quantower installer screen](../.gitbook/assets/extract-files-quantower.png)

1. [**Download the app installer**](https://updates.quantower.com/Quantower/x64/latest/Quantower.exe) and launch the _**Quantower.exe**_ file
2. Select the folder to extract application files (preferably the Downloads folder or a secondary drive, not the System drive). Some features may not work correctly if you install the platform on the C: system drive due to administrative rules and restrictions.
3. Once an extraction process is finished the platform will start automatically. A window will appear where you can choose which connection to enable by default with the default [**workspace**](../general-settings/workspaces-binds-groups.md).

***

<mark style="background-color:blue;">**DxFeed Simulated**</mark> provides market data for a limited number of symbols with a 24-hour data delay. This type of connection is intended solely for getting acquainted with the platform's functionality.

{% hint style="info" %}
To receive **real-time data** or access a larger number of symbols from the DxFeed provider, it is necessary to [**subscribe to their paid service**](https://get.dxfeed.com/orders/new/quantower) on their official website.
{% endhint %}

If you choose <mark style="background-color:blue;">**Binance**</mark>, the platform will connect in **Info mode** without the ability to execute trades. This connection type is meant for exploring the platform's features or for viewing and analyzing real-time cryptocurrency charts.

{% hint style="info" %}
To execute trading operations on the Binance exchange, you need to switch to Trading mode and paste your API keys. Learn more about [**how to connect to the Binance exchange**](../connections/connection-to-binance-futures/).
{% endhint %}

<figure><img src="../.gitbook/assets/image (386).png" alt=""><figcaption></figcaption></figure>

Within a minute, a window will appear with the platform's terms of use, which you should review and accept for further platform usage.

<figure><img src="../.gitbook/assets/image (387).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Please note, that you may need to allow an in-going and outgoing connection for _**Starter.exe**_ file (the main executable of Quantower platform) in your Firewall settings
{% endhint %}

<figure><img src="../.gitbook/assets/image (388).png" alt=""><figcaption><p>Default workspace with DxFeed Simulated data</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (389).png" alt=""><figcaption><p>Default workspace with Binance Spot connection</p></figcaption></figure>

### Uninstalling

If you need to uninstall the application, simply _**delete the folder containing all application files**_. You can also keep your personal settings (connection information & workspaces) by copying the "Settings" folder (located directly in the Quantower folder) before deleting the application. Later, you can paste this "Settings" folder into any other Quantower folder.

You may also refer to [**Backup & Restore manager**](backup-and-restore-manager.md) to backup your settings in one file and restore them later.
