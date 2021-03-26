---
description: >-
  Setup Actions feature allows you to setup certain behavior on some data change
  in the table.
---

# Setup Actions & Advanced filters

**Setup Actions** feature allows you to set certain behavior on some data change in the table. This feature is available in panels:

* \*\*\*\*[**Watchlist**](../analytics-panels/watchlist.md)\*\*\*\*
* \*\*\*\*[**Time & Sales**](../analytics-panels/time-and-sales.md#setup-actions-filters-and-actions)\*\*\*\*
* \*\*\*\*[**Price Statistic**](../analytics-panels/price-statistic.md)\*\*\*\*
* \*\*\*\*[**Working Orders**](../portfolio-panels/working-orders.md)\*\*\*\*
* \*\*\*\*[**Positions**](../portfolio-panels/positions.md)\*\*\*\*
* \*\*\*\*[**Trades**](../portfolio-panels/trades.md)\*\*\*\*
* \*\*\*\*[**Orders History**](../portfolio-panels/orders-history.md)\*\*\*\*

![Setup Actions feature in Quantower platform](../.gitbook/assets/image%20%2864%29.png)

Setup Actions consists of two options:

1. **Filters** — where you can set up filters for different columns
2. **Actions** — where you can set up multiple actions, based on data in rows & columns.

## Actions

Currently, Quantower tables support four types of actions:

* Show message
* Play sound
* Color row
* Color cell

The Table actions functionality can be found under the panel’s context menu option “Setup Actions” and once launched, it opens an “Actions screen”, where you can manage your Actions. The process of Action creation is not complicated.

1. Create an Action item 
2. Set conditions \(“OR” & “AND”\) 
3. Set tasks \(Show message, Play sound, Color row, Color cell\) 
4. Save Action 
5. Enable Action

### Table actions tasks

Once some condition is met, action will execute the corresponding tasks. Each task will be executed as many times, as the condition was met.

| **Show message** | Displays a popup box with the user-specified message |
| :--- | :--- |
| **Play sound** | Plays some user-selected sound file |
| **Color row** | Changes the styling of the whole row, where the condition was met. Allows changing the background and/or text colors. |
| **Color cell** | Changes the styling of the specified cell\(s\) of the row, where the condition was met. Allows changing the background and/or text colors. |

{% hint style="warning" %}
Be careful with the frequently occurring conditions. Some may be met several times per second, so tasks like “_Play sound_” can become disturbing. The “_Show message_” task, fired several times, will be shown as one message box.
{% endhint %}

### Table filters

Rows in the table can be filtered by some data values in their column. There are two ways to apply the filtering:

* **Quick filtering** can be accessed by clicking the “_**Filter**_” icon in any table column’s header.

![Quick filtering per column](https://gblobscdn.gitbook.com/assets%2F-LD6FsRvQ3jgwJIg6O7r%2F-LSZlUr_Myk0rKIIPYb3%2F-LSZtsdnR8ZXyAorsvkj%2FQuick%20filtering.png?alt=media&token=ccff8243-c69e-427c-8825-00c8ce9e1818)

Once you select some option — the table rows will be filtered to those ones, containing the selected value. Quick filter can be canceled by pressing “_**Cancel filtering**_” option.

Quick filtering can be applied only to one column of the table. For filtering multiple columns, we recommend using “_**Setup actions**_”.

* **Advanced filtering,** for applying more complex filtering \(multi-filtering\). Select in the panel's context menu option “_**Setup actions**_”.

![](https://gblobscdn.gitbook.com/assets%2F-LD6FsRvQ3jgwJIg6O7r%2F-LvGYANuFTIQuOZAz6LM%2F-LvGfvw940y4eFZGgYt6%2Fsetup%20actions%20ts.png?alt=media&token=c7a2a5f1-ab62-49c9-b5a9-8f4753f51bbe)

This screen has two tabs on the left side, where the first one is an Advanced filter.

![Advanced filtering in Time &amp; Sales panel](https://gblobscdn.gitbook.com/assets%2F-LD6FsRvQ3jgwJIg6O7r%2F-LSZlUr_Myk0rKIIPYb3%2F-LS_5SP-opC1CiDG-iws%2Fadvanced%20filtering.png?alt=media&token=e2d74d74-7ee5-4533-ae11-09d4db0ab09c)

This screen allows you to Enable/disable filtering as well as set up filtering Conditions. These conditions are set up as:

$$
IF (condition1AND condition2 ...) OR (conditionN...) …
$$

You can setup as many conditions as you like. Due to the possible complex logic of filtering, you are required to apply the changes once you finished the filter set up.



