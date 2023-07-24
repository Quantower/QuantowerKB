---
description: >-
  How to install Visual Studio Community 2022 + Quantower Algo extension, and
  create your own indicators and strategies
---

# Install for Visual Studio 2022

**Visual Studio** — is an integrated development environment (IDE) from Microsoft, which includes a code editor with IntelliSense, debugger, supporting source control systems, and many other professional features. **The currently supported Visual Studio versions are 2022 and 2019**.&#x20;

{% hint style="success" %}
We recommend you to use the most basic version of **Visual Studio — the Community edition**, which is available free of charge.
{% endhint %}

You can [**download Visual Studio from an official website**](https://visualstudio.microsoft.com/ru/thank-you-downloading-visual-studio/?sku=Community\&rel=16). It requires about 10 minutes to install and \~4Gb of free space on your hard drive.

Download the web installer and run it. After initialization, you will be prompted to select the required components. For using with Quantower Algo extension we need only the "**NET desktop development**" workload. You can uncheck optional components also, to reduce installation size:



{% embed url="https://www.youtube.com/watch?v=Lw7lPIxT2xA" fullWidth="true" %}

![Minimal required installation](../.gitbook/assets/Screenshot\_3.png)

Continue installation and in a few minutes, after downloading and applying required packages, Visual Studio will start automatically:

![Default view of Visual Studio 2019](../.gitbook/assets/Screenshot\_1.png)

Now we need to install Quantower Algo extension from Visual Studio Marketplace. Use "_**Tools -> Extension and Updates...**_" main menu item to open Extensions Manager. Type "_**Quantower**_" into the search box of **Online tab** and you will find a required extension:

![Extensions and Updates window](../.gitbook/assets/Screenshot\_2.png)

Click "**Download**". Visual Studio will ask you for restarting to finish the extension installation process.

To check whether Quantower Algo is installed successfully click "_**File -> New -> Project**_" menu item, type "Indicator" and you will see a special project type for the blank indicator:

![New project window](../.gitbook/assets/Screenshot\_4.png)

Now everything is ready to [create your first indicator](simple-indicator.md).
