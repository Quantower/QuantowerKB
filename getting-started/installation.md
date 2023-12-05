---
description: System requirements and 3 simple steps to successfully install the platform
---

# Installation

* [**System Requirements**](installation.md#pc-requirements)
* [**Installation Steps**](installation.md#installation-steps)
* [**Uninstalling**](installation.md#uninstall)

***

After downloading the Quantower application from the official website, you can begin the installation process. It's important to understand the differences between the Quantower "installation process" and the default Windows® install process that most users are familiar with.

{% embed url="https://youtu.be/155Ha6Rku0E" %}

{% hint style="success" %}
Quantower does not copy its files to the system folders (AppData or Program Files) of the OS, nor does write changes to the system registry
{% endhint %}

What does it mean? The program doesn't violate the integrity of the OS, and in case of removal, it will not leave any prints of its presence on your computer. Quantower’s "installer" literally extracts files to the user-specified folder.

With this approach, you can save the Quantower on a removable drive and use it as a portable application on any other computer. This is especially useful when you need to transfer Quantower along with all its settings to a different PC. Simply copy the Quantower folder and paste it where you want it.

### PC requirements

{% hint style="info" %}
* Windows 10, 11
* [.NET 7](https://dotnet.microsoft.com/en-us/download/dotnet/7.0)
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
2. Select the folder to extract application files (preferably the Downloads folder or a secondary drive, not the System drive). If you install the platform on the C: system drive, some features may not work correctly due to administrative rules and restrictions.
3. Once an extraction process is finished the platform will start automatically with **Binance connection** in Info Mode and with the default workspace

{% hint style="warning" %}
Please note, that you may need to allow an in-going and outgoing connection for _**Starter.exe**_ file (the main executable of Quantower terminal) in your Firewall settings
{% endhint %}

![](../.gitbook/assets/default-workspace.png)

### Uninstalling

If you need to uninstall the application, just _**delete the folder with all application files**_. You may also keep your personal settings (connection information & workspaces) by copying the Settings folder (can be found right in Quantower folder) before application delete. These Settings folder can be pasted to any other Quantower folder later.

You may also refer to [**Backup & Restore manager**](backup-and-restore-manager.md) to backup your settings in one file and restore them later.
