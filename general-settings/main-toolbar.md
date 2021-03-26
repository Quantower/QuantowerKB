---
description: >-
  Get to know how to use and manage Main Toolbar that is a starting panel of all
  platform
---

# Quantower Main Toolbar

**Main Toolbar** — is the main starting point of the platform, used as a launcher and informer simultaneously.

![Quantower Main toolbar](../.gitbook/assets/image%20%2873%29.png)

Main Toolbar technically is a panel, but behaves something differently: it can be dragged among your screens \(if you have more than one\) and it will be always stuck at the top of the screen. It adapts own width up to the screen width and it participates in the workspace, meaning, that other panels can be stuck to it. 

![](../.gitbook/assets/main-toolbar.png)

In this guide you will learn about the next functionalities:

* \*\*\*\*[**How to customize the Main Toolbar**](main-toolbar.md#customization-of-main-toolbar)\*\*\*\*
* \*\*\*\*[**Main menu with all panels**](main-toolbar.md#sidebar)\*\*\*\*
* \*\*\*\*[**How to add Favorite Panels on the Toolbar**](main-toolbar.md#favorite-panels)\*\*\*\*
* \*\*\*\*[**How to Lock Trading**](main-toolbar.md#lock-trading)\*\*\*\*
* \*\*\*\*[**How to create and manage your Workspaces**](main-toolbar.md#workspaces-manager)\*\*\*\*
* \*\*\*\*[**Managing trading connections**](main-toolbar.md#favorite-connections)\*\*\*\*
* \*\*\*\*[**Sidebar with all Notifications**](main-toolbar.md#notifications-center)\*\*\*\*
* \*\*\*\*[**Platform's General Settings**](main-toolbar.md#general-settings)\*\*\*\*
* \*\*\*\*[**Time & Time Zones**](main-toolbar.md#time-and-time-zones)\*\*\*\*

Due to the fact that Toolbar is the main controlling panel it has the ability to collapse all platform’s interface by clicking the “_**Minimize**_” icon. This action makes all application panels collapse to the taskbar and literally disappear from your screens; it affects all panels on all screens.

The “_**Close**_” icon just closes the platform. You may set up the “_not to ask to confirm the closing_” setting in the pop-up screen while the first closing.

### Customization of Main Toolbar

For optimal use of the space on the Main Toolbar, we have added the ability to display/hide some controls. For example, to hide the Timezones, Workspaces, Connections, etc., **Right-click** on the context menu and go to the View section. By clicking on the ticks, the controls will appear at the Toolbar.

![Right click on the Main Toolbar will bring up the addtional settings window](../.gitbook/assets/image%20%2876%29.png)

### Main Menu with all panels

All of the panels are placed in the _“Sidebar”_ screen, which is popping out once you click the **Logo icon** on the toolbar. The Main Menu consists of panel icons, grouped by functionality. Actually, in this menu, you can find all panels.

![Main menu in the Quantower platform](../.gitbook/assets/main-manu.png)

Each group in this menu can be collapsed in order to make the panels list cleaner. From this place, you can open any panel by left-clicking on its icon. Each group has its color to help you determine the functional assignment of each panel.

The footer of the Main Menu contains several functions:

* “**About**” link: opens a screen with information about terminal \(version, rollback, updates checker etc.\). If the system detects the new version of Quantower, the **“NEW VERSION”** button appears instead of this link;
* “**Exit**” button closes the application.

{% hint style="info" %}
The list of links in footer can contain more or fewer items, depending on current application requirements.
{% endhint %}

### Favorite panels

You might already have seen the Star icon in the right top corners of some panels tiles in Sidebar. This is the “**Favorite panels**” functionality, allowing you to select the most usable panels and place their icons on the Main Toolbar.

![Favorite panels](../.gitbook/assets/favorite-panels.gif)

The way to use it very simple — hover over the right top corner of any panel tile in Sidebar and click the Star icon that appeared. That is all: panel appears in Favorite panels bar in Main Toolbar. To remove from favorites just click the activated Star icon on Panel's tile or right-click on the icon in Favorites panel and select “_**Hide from toolbar**_”.

### Lock trading

If you would like to prevent manual trading operations occur, you may use the “_**Lock trading**_” button on Main Toolbar. Once clicked it displays the confirmation message that trading being locked and all of the functions, related to the opening or closing orders and positions will be disabled. Unlock trading can be done the vice-versa way.

![Lock Trading Icon](../.gitbook/assets/lock_trading.png)

This feature is useful in case you would like to only analyze the market or while editing your workspace \(mostly to avoid misclicks\).

### Workspaces manager

{% embed url="https://www.youtube.com/watch?v=A\_2gJdeP-08&t=20s" caption="Create and save your workspace in Quantower" %}

**Workspaces manager** allows you to see, create, edit and delete your working environments as well as lock their modification. It is represented with the special icon, that opens the list of available Workspaces once being clicked.

![](../.gitbook/assets/workspaces.png)

The currently active workspace is marked with the color and has a blue dot on the left side of its name. You can switch the current workspace by left-clicking any of the available items from the list. The bottom part of the list \(after separator\) consists of actions, referred to the currently active workspace and allows to:

* **Lock** — disables an ability to add, remove, move or resize any panel in current workspace;
* **Rename...** — invokes a pop-up screen where you can set up a new name for the current workspace;
* **Create new** — opens a pop-up screen with the new workspace creation form.

![New workspace creation window](../.gitbook/assets/ccnewworkspace.png)

When creating the new workspace, you have an ability to specify its future name and select whether it should be Blank, once created, or should contain some predefined panels set. 

You can also remove any of Workspaces by clicking the “_**Trash**_” icon on the right side from Workspace name \(icon appears while hovering the name\).

### Favorite connections

The list of active connections can be seen on Main Toolbar in Favorite connections block. By default, you will see several items here, each representing one of the available connections. The [Connection manager](../connections/connections-manager.md) screen will be opened by clicking any of the items in Favorite connections block. 

![Add favorite connections by clicking the &quot;Star&quot; icon](../.gitbook/assets/favorite-connections.png)

In order to show some connection on this bar, you need to click a “_**Star**_” icon at the right side of connection name in Connections manager panel. Click once more, and the connection will be removed from Favorites bar.

Being added to Favorites bar, each connection will be displayed as a tile, containing some vital info:

* **Connection name**
* **Status text** \(can be a status message or Ping time in ms when the connection is active\)
* **Status Dot**, a visual representation of connection status. Can be grey \(disconnected\), yellow \(connecting\), green \(active\).

You can remove a connection from Favorites by right-clicking on it and selecting “_**Hide from toolbar**_” item. Here you can also ask to connect or disconnect.

### Notifications center

Most actions during the platform use generate various notifications. There can be system notifications \(some connection problems or errors\) and Deal tickets. 

The **Deal tickets** — are the notifications about the trading operations. Each time you create an order or opening a new position — we will create a deal ticket for this. \(you can [disable deat tickets in general settings](general-settings-1.md#confirmations)\)

While some trading actions may be done in one click at the first sight, they usually consist of several related operations, each of them will be displayed via the Deal tickets. That is why you can see much more items in Notifications center than you did actions. 

The **Notifications center** — is the place where all notifications are stored in one list. You can open that list by clicking the Notifications icon in Control center. 

![Notifications center](../.gitbook/assets/image%20%2877%29.png)

When you have a set of new notifications, the small number will appear in the left top corner of Notification center icon. It displays how many unread notifications you have. Once you open the list — it understands that you have read them and the number will disappear. 

You will see all notifications just from the platform start. You may also clear this list by clicking the “_**Clear all**_” link. This action will hide all of the currently seen notifications from this list \(but they will be still available in Event Log panel\).

By clicking one of the notifications you will see the window with the detailed info.

### General settings

The “_**Gear**_” icon opens a general settings screen, where you can set up the most common parameters of our terminal. [More details about the **Settings**](general-settings-1.md) screen are available in the corresponding section of this documentation.

![Access to general settings](../.gitbook/assets/image%20%28134%29.png)

### Time & Time zones

The Time bar is also displayed on the Main Toolbar toolbar showing you time in the selected timezone. By default, your local timezone is used. You can change the time zones list by clicking the "_**Gear**_" icon and then select the required ones in [**General settings screen**](general-settings-1.md#time-zones). You may also select several time zones and they will appear as a list in a drop-down panel, allowing you to switch among them quickly.

![Switch between your favorite timezones](../.gitbook/assets/image%20%2878%29.png)

