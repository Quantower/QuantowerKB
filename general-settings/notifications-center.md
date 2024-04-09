---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# 📢 Notifications center

## General concept

Quantower platform features numerous operations requiring user engagement. To effectively communicate the outcome of a user's action, the platform employs familiar pop-up notifications. The Notifications Center acts as a dedicated engine, overseeing and categorizing all actions before determining the necessity of notifying users about their results.

<figure><img src="../.gitbook/assets/Group 13706.png" alt=""><figcaption><p>Notifications center</p></figcaption></figure>

Notifications center consists of several UI elements in Quantower terminal:&#x20;

* An icon in a Control center
* Notifications center sidebar
* Pop-up windows
* Notifications Settings screen

## Notifications icon on Control center

The portal to the Notifications Center is an icon located on the Control Center toolbar. This icon serves two primary functions:

1. **Opening the Notifications Sidebar:** A single click on the icon reveals the sidebar where you can view all notifications.
2. **Unread Notification Count:** The icon also displays the count of unread notifications, providing a quick glance at how many messages you've yet to see.

{% hint style="warning" %}
**Important:** The icon on the Control Center toolbar is the **sole access point** to the Notifications Sidebar. Should you choose to remove or hide this icon from the Control Center, accessing the complete list of notifications becomes impossible. However, you will still receive notification pop-ups, granted they were set up in advance.
{% endhint %}

## Notifications sidebar

Notifications are stored in the Notifications sidebar, which is attached to the Control Center toolbar on the right screen side. It overlays all other panels and automatically hides when you interact with any UI element outside of it.

Sidebar consists of two sections: the **Quick actions toolbar**, and **notifications list**.

### Quick actions toolbar

The Quick actions toolbar allows you to (from left to right):

* <mark style="color:green;">**Disable ALL pop-ups**</mark> ("No disturb mode") regardless of other pop-up settings
*   <mark style="color:green;">**Quick "Read -> Delete"**</mark><mark style="color:green;">.</mark> \
    This feature lets you swiftly manage your notifications. Clicking this button marks all unread notifications as "Read". Once all notifications are marked as read, the button changes to "Delete", allowing you to clear the entire list with another click. Essentially, two clicks - "Read" then "Delete" - make all notifications disappear.

    **Please note!** The "Read -> Delete" button affects all notifications, even with active filters.
*   #### <mark style="color:green;">Categories Filter</mark>

    This feature lets you filter notifications in a list by category. You can configure these categories in the Notification Center settings.
* <mark style="color:green;">**Notifications center Settings**</mark>. Opens the respective settings screen.

### Notifications list

Notifications in the Quantower terminal have two states: **New (Unread)** and **Read**. Opening the Notifications sidebar automatically marks all new notifications as read when the sidebar is closed. You can delete notifications individually via the "Cross" icon that appears on hover.

All notifications from the beginning of the Quantower terminal session are available in the sidebar.&#x20;

{% hint style="warning" %}
Please note, restarting your terminal will erase all notifications from the previous session.
{% endhint %}

If you click any notification it will trigger the corresponding action:

* open a detailed view of notification (most cases)
* open an about screen (for Terminal updates type)
* etc.

<figure><img src="../.gitbook/assets/Group 13712.png" alt=""><figcaption><p>Common notification item</p></figcaption></figure>

Every Notification tile contains:

* Title (main message)
* Description (Optional)
* Tmestamp (in miliseconds)
* Category
* Accent color
* Delete icon

## Pop-ups

Notification pop-ups are designed to draw user attention and can be customized broadly or for specific notification categories. These settings, including appearance and color theme, are adjustable in the Settings menu. Pop-ups display the same details found in the Notifications sidebar and can be dismissed by clicking the cross icon that appears when hovering over an item.

<figure><img src="../.gitbook/assets/Group 13713.png" alt=""><figcaption><p>Customized notifications pop-ups</p></figcaption></figure>

The number of visible pop-ups at a time can be configured in the settings screen. If you have set to display a maximum of 5 pop-ups and receive 8 notifications at once, you will see only the first 5 of 8 in chronological order. Pop-ups will appear and automatically disappear after a specified amount of time (configured in the settings). If you hover your cursor over the appeared pop-ups block, it will remain visible until you remove your cursor. You can click the "Hide them all" button to hide all visible pop-ups immediately.

## Notifications settings

Notification Center settings are utilized by the notifications engine to alert you of certain actions being completed. There are default parameters in the General section and specific overrides in Custom categories. Each custom category has a priority value, known as its weight, that is used when generating a message. A higher priority results in a lower place in the order of parameter application.

### General settings

<figure><img src="../.gitbook/assets/image 101.png" alt=""><figcaption><p>Default notification parameters</p></figcaption></figure>

Here, you can configure the default behavior for all notifications, regardless of type. These parameters will be applied to any notification if no other specific settings are established.

* <mark style="color:green;">**Enable Notifications**</mark><mark style="color:green;">:</mark> Allows you to completely disable all notifications, while the "No Disturb" button on the Quick Action Toolbar only disables pop
* <mark style="color:green;">**Accent Color**</mark><mark style="color:green;">:</mark> Select a special color to mark notifications, adding a corresponding color line to the notification list for visual variety.
* <mark style="color:green;">**Maximum Pop-Ups at Once**</mark><mark style="color:green;">:</mark> Specify the maximum number of initial pop-ups to show if several appear at once (up to 10 items).
* <mark style="color:green;">**Auto Hide Pop-Ups Delay (sec)**</mark><mark style="color:green;">:</mark> Set the time in seconds before pop-ups are automatically hidden. You can pause the auto-hide feature by hovering over the pop-up.
* <mark style="color:green;">**Pop-Ups Placement**</mark><mark style="color:green;">:</mark> Choose a corner of the screen for pop-up notifications.
* <mark style="color:green;">**Show Pop-Up**</mark><mark style="color:green;">:</mark> Enable or disable pop-ups by default, as well as set up their style, including background and text colors.
* <mark style="color:green;">**Play Sound**</mark><mark style="color:green;">:</mark> Enable or disable sound playback when a notification arrives. Supports sound files in .WAV format.
* <mark style="color:green;">**Send to Telegram**</mark><mark style="color:green;">:</mark> Enable or disable sending notification copies to you using the [Quantower Telegram bot.](../miscellaneous-panels/quantower-telegram-bot.md)

### Custom categories

<figure><img src="../.gitbook/assets/image 102.png" alt=""><figcaption><p>Custom categories for notification styling</p></figcaption></figure>

Custom categories enable you to tailor specific notifications away from the main stream by overriding their parameters. A category with a lower priority value will surpass those with higher values. For instance, if you configure two categories (with priorities 1 and 2) for the notifications engine to apply after filtering, the engine will adhere to the following sequence of parameters: General parameters -> Category with Priority 2 -> Category with Priority 1.

Custom categories come with default creation parameters similar to those found in the General settings. However, they also include unique options tailored for specific needs. Below, we outline these specific options:

* <mark style="color:green;">**Enable.**</mark> Enable/disable this custom category.
* <mark style="color:green;">**Category Name:**</mark> \
  The name for this notifications segment that will be used as the Notification tile's Category value.
* <mark style="color:green;">**Priority:**</mark> \
  This category's weight in the order of parameter application when multiple categories apply to one notification item. A higher value indicates it will be applied earlier in the order.
* <mark style="color:green;">**Notifications Filter**</mark>\
  This section allows you to specify filtering parameters to segment specific notifications from the general flow. Use a set of `[IF+AND] |OR| [IF+AND]` conditions. Each row should contain Condition -> Equation -> Value. The conditions are as follows:
  * <mark style="color:blue;">**Title, Message, Connection Name, Symbol, Account**</mark> — are values that can be directly equal (=), directly unequal (!=), contain, and not contain specific text related to this notification.
  * <mark style="color:blue;">**Notification Types**</mark>\
    A list of general types based on the objects of provocation at the terminal. These can be either directly equal (=) or directly unequal (!=) only.
    * <mark style="color:purple;">**Info.**</mark> General notifications from terminal, that doesn't have a specific category
    * <mark style="color:purple;">**Refuse.**</mark> Any general refusals not specifically received from the order management servers.
    * <mark style="color:purple;">**Order opened.**</mark> Received from remote server (connection)
    * <mark style="color:purple;">**Order filled.**</mark> Received from remote server (connection)
    * <mark style="color:purple;">**Order partially filled.**</mark> Received from remote server (connection)
    * <mark style="color:purple;">**Order cancelled.**</mark> Received from remote server (connection)
    * <mark style="color:purple;">**Trading operation request.**</mark> Produced by the platform when requesting an operation from a remote server.
    * <mark style="color:purple;">**Trading operation success.**</mark> Produced by the platform when the remote server accepted the request
    * <mark style="color:purple;">**Trading operation refuse.**</mark> Produced by the platform when the remote server refused the request.
    * <mark style="color:purple;">**Trading signal.**</mark> Produced by the trading signails provider (special connection).
    * <mark style="color:purple;">**Terminal update.**</mark> When a platform has an update available.
    * <mark style="color:purple;">**License.**</mark> Any notifications about your Quantower account and license operation.
    * <mark style="color:purple;">**Connection success.**</mark> When the platform connects to the remote server (connection)
    * <mark style="color:purple;">**Connection lost.**</mark> When the platform dsiconnects from the remote server (connection)
* <mark style="color:green;">**Accent Color, Show Pop-up, Play Sound, Send to Telegram**</mark> — these are the same parameters as in the General settings. Each of these options will override the General parameters, meaning that if you disable pop-ups in a category, they will become hidden. These options are specifically useful for changing the various colors, styling, and placement of pop-ups for each custom category.

When you make any changes to Custom category parameters you must Apply them, in order to make any effect.
