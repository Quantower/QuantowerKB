---
description: >-
  Setup Actions feature allows you to setup certain behavior on some data change
  in the table.
---

# Setup Actions & Advanced filters

Setup Actions feature allows you to setup certain behavior on some data change in the table. This feature 

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
| **Play sound** | Plays some user selected sound file |
| **Color row** | Changes the styling of the whole row, where the condition was met. Allows changing the background and/or text colors. |
| **Color cell** | Changes the styling of the specified cell\(s\) of the row, where the condition was met. Allows changing the background and/or text colors. |

{% hint style="warning" %}
Be careful with the frequently occurring conditions. Some may be met several times per second, so tasks like “_Play sound_” can become disturbing. The “_Show message_” task, fired several times, will be shown as one message box.
{% endhint %}

### Advanced table filter

In case you would like to apply some more complex filtering \(multi-filtering\) you can open an advanced filter from panel’s context menu, option “_**Setup Actions**_”. This screen has two tabs on the left side, where the first one is an Advanced filter.

![](https://gblobscdn.gitbook.com/assets%2F-LD6FsRvQ3jgwJIg6O7r%2F-LFqorWfAjWaGYwswV2L%2F-LFqqvJ1QgfZwbLwX8-P%2FTableAdvancedFiltering.png?alt=media&token=15bb2602-9410-4a9b-8acf-7f594c01c2e2)

This screen allows you to Enable/disable filtering as well as set up filtering Conditions. These conditions are set up as:

$$
IF (condition1AND condition2 ...) OR (conditionN...) …
$$

You can setup as many conditions as you like. Due to the possible complex logic of filtering, you are required to apply the changes once you finished the filter set up.



