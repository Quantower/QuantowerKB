# View Settings

<figure><img src="../../../.gitbook/assets/DOM Trader View settings.png" alt=""><figcaption><p>General View of DOM Trader Settings</p></figcaption></figure>

* **Custom title**\
  You can rename your DOM Trader panel as desired.
* **Refresh rate (ms)**\
  The setting controls the rate at which market data is updated. This determines how often the platform processes changes in the depth of market. With a value of 1, all changes to the level2 data will be processed immediately. We recommend using value 50.
* **Ticks to scroll**\
  This setting determines how many ticks the price scale will move with each scroll of the mouse. For instance, setting this parameter to 10 means that the minimum scroll action will shift the price scale by 10 ticks.
*   **Use custom tick size**\
    This setting changes the price step by aggregating the level2 data. There are two ways to change the aggregation of ticks in the DOM trader:

    1. By holding the <mark style="background-color:blue;">**CTRL button**</mark> and spinning the mouse wheel
    2. Set the parameter manually in the panel's settings

    ![Applying of custom tick size by holding CTRL button](<../../../.gitbook/assets/DOM Trader aggregation of ticks.gif>)

    ![Applying of custom tick size via DOM trader settings](<../../../.gitbook/assets/image (356).png>)


* **Short price format**\
  This setting allows you to hide part of the digits in the price column. It's useful for simplifying the display and focusing on the most significant price movements.

<figure><img src="../../../.gitbook/assets/Short price format in DOM Trader.png" alt=""><figcaption><p>Short price format in the DOM Trader</p></figcaption></figure>

* **The Abbreviation Rules** \
  This option gives you the ability to simplify the values of trading sizes for easier readability. There are 3 options for Format Mode:\
  \
  **Default:** This option displays values as is, without any abbreviation or rounding.\
  \
  **Round to:** This option rounds values after the decimal point to the specified number of decimal places.\
  \
  **Abbreviate:** This option abbreviates values to the shortest form, such as "K" for thousands, "M" for millions, etc.
