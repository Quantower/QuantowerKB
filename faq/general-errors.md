# General Errors

* [**How to Fix the ‘You’ll need a new app to open this ms-gaming overlay’ Error on Windows 10?**](general-errors.md#how-to-fix-the-youll-need-a-new-app-to-open-this-ms-gaming-overlay-error-on-windows-10)
* [**Error 'Application is already running'**](general-errors.md#error-application-is-already-running)
* [**An error occurred during platform initialization: Exception has been thrown by the target of an invocation**](general-errors.md#an-error-occurred-during-platform-initialization-exception-has-been-thrown-by-the-target-of-an-invoc)
* [**An error occurred during platform initialization: Fail to load DLL signatures**](general-errors.md#an-error-occurred-during-platform-initialization-fail-to-load-dll-signatures)
* **Trendlines are moving on tick charts. How to resolve it?**
* [**Incorrect view of icons inside the application (for Mac via Parallels)**](general-errors.md#incorrect-view-of-icons-inside-the-application-for-mac-via-parallels)
* [**Сan not find a stock ticker with the dxfeed data provider (F, SO, META etc)**](general-errors.md#san-not-find-a-stock-ticker-with-the-dxfeed-data-provider-f-so-meta-etc)
* [**How to replace the main Toolbar to another screen (monitor)?**](general-errors.md#how-to-replace-the-main-toolbar-to-another-screen-monitor)

## How to Fix the ‘You’ll need a new app to open this ms-gaming overlay’ Error on Windows 10?

![](<../.gitbook/assets/image (164).png>)

The easiest method is starting troubleshooting with simply **disabling Game Bar**. This could be helpful to remove the key combination and use it for other purposes.&#x20;Now, you can take these steps:

* Press the **Win + I** combination key to open Windows Settings
* Go to **Gaming > Gaming bar**.
* Switch the toggle of **Xbox Game Bar for things like recording game clips, screenshots, and broadcast using Game bar** to **Off**. Next, press **Win + G** to see if the error is solved.

![](<../.gitbook/assets/image (165).png>)

More details you can find here [https://www.minitool.com/news/ms-gaming-overlay-popup.html](https://www.minitool.com/news/ms-gaming-overlay-popup.html)

## Error 'Application is already running'

![](<../.gitbook/assets/image (161).png>)

* This message is displayed if you try running multiple Quantowers in parallel on the same computer or you have closed Quantower a few seconds ago and it did not finish closing yet. In 20 seconds or sooner Quantower can be started again.
* If even after a few minutes the platform fails to start, go to the **Task Manager**. Press **Ctrl+Shift+Esc** to open the Task Manager with a keyboard shortcut or right-click the Windows taskbar and select “Task Manager.”\
  Find the process with the name **"Starter"**, select it and click on **End task**.

![](<../.gitbook/assets/image (163).png>)

## An error occurred during platform initialization: Exception has been thrown by the target of an invocation

This error occurs due to the removal of the file by the **Avast antivirus or AVG antivirus**, which is necessary for the correct work of the platform.&#x20;

![](<../.gitbook/assets/image (196).png>)

Our developers informed Avast and AVG companies that the file CefSharp.BrowserSubprocess.exe is a part of the CefSharp library — HTML5, JavaScript and PDF supported Web browser based on Chromium Embedded Framework. It allows using web browsing services in applications to create the user interface. We use this library in our platform as well. More information about it you can read here [https://cefsharp.github.io](https://cefsharp.github.io)

We don't know a reason why antivirus sometimes recognizes this file as suspicious, but if you search in google, you can see that there are already many reports from users about the same problem: [https://www.google.com/search?q=cefsharp.browsersubprocess.exe+antivirus](https://www.google.com/search?q=cefsharp.browsersubprocess.exe+antivirus) In general case antivirus developers recommend reporting a problem as false positive.

To be 100% sure, that this file is not dangerous, you can check it manually using different web services like [https://www.virustotal.com](https://www.virustotal.com) They will display your results received from different antiviruses.

![CefSharp.BrowserSubprocess.exe is checked by all major antiviruses](<../.gitbook/assets/image (214).png>)

As a solution, we recommend you remove Avast or AVG antiviruses (completely) and reinstall the platform.

Some times Kaspersky delete our files.&#x20;

![](<../.gitbook/assets/image (223).png>)

## An error occurred during platform initialization: Fail to load dll signatures

![Quantower error "Fail to load dll signatures"](../.gitbook/assets/quantower-error.png)

This error can occur for several reasons:

* There is <mark style="color:red;">**no internet connection**</mark>** or a weak connection**. Please check that the connection is stable with your browser.
* It appears that you are currently utilizing an <mark style="color:red;">**outdated version**</mark>** of our platform that is no longer supported**. We strongly advise that you [**download the newest version**](https://www.quantower.com/download) from our official website and [<mark style="color:green;">**transfer all of your settings**</mark>](https://help.quantower.com/quantower/getting-started/reset-settings-to-default) from the old version to the updated one.
* The platform has **not fully installed the files** to work correctly. Please reinstall the platform.

![Full list of folders and files for Quantower](<../.gitbook/assets/image (216).png>)

## Trendlines are moving on tick charts. How to resolve it?



## **Incorrect view of icons inside the application (for Mac via Parallels)**

Sometimes users may encounter the problem of incorrect display of icons of various functions inside the application. For example, the picture below is such a situation.

<figure><img src="../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>

This situation occurs when using the Parallels emulator for Mac. To solve this problem, Parallel itself offers a solution at the link below [https://kb.parallels.com/112983](https://kb.parallels.com/112983)

> **Isolate Windows from Mac** to exclude Mac OS X influence. (**Virtual Machine > Configure… > Options > Security** > check on **Isolate Mac from Windows**)

## **Сan not find a stock ticker with the dxfeed data provider (F, SO, META etc)**

Sometimes, users face the problem of finding a company's stock by its exact ticker on a dxfeed data provider. For example, users can not find F (Ford company), META (ex-Facebook) etc.

The problem is related to the fact that the search for stocks is performed by the **description** (name) of the company, especially for tickers with a small number of symbols (1-2 letters).

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

## **How to replace the main Toolbar to another screen (monitor)?**

<figure><img src="../.gitbook/assets/image (369).png" alt=""><figcaption><p>Quantower Main toolbar</p></figcaption></figure>

There are two ways to move the main toolbar to another monitor:

* To move the main toolbar to another monitor, <mark style="background-color:orange;">**click and hold the mouse cursor on it and drag it to the desired monitor**</mark>. Make sure <mark style="background-color:blue;">**both monitors are aligned at the same level**</mark>, which you can verify in your monitor settings.

<figure><img src="../.gitbook/assets/image (368).png" alt=""><figcaption></figcaption></figure>

* click on the main toolbar and use the key combination <mark style="background-color:blue;">**Win + Shift + Arrow**</mark> <mark style="background-color:blue;"></mark><mark style="background-color:blue;">(left / right)</mark>.
