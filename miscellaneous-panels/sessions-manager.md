---
description: >-
  With the new Sessions manager functionality, you can create sessions templates
  and assign them on the symbol, exchange, or even connection levels.
---

# Sessions manager

## General

You can find a new Sessions manager screen in a Miscellaneous section of the Quantower's control center. Once launched, you will see a table where Quantower will display the list of custom sessions assignments. Initially, it is empty, meaning that Quantower will use the sessions data coming from the symbols vendor. Generally, Sessions manager functionality is based on the work with sessions templates - creation and assignment - so its flow is simple: create a template and then assign it to some symbol (exchange, connection).

## Create sessions template

![Sessions ate creation screen](<../.gitbook/assets/image3 (1).png>)

Click the <mark style="background-color:blue;">**Sessions templates**</mark> button on the toolbar and <mark style="background-color:blue;">**Create new**</mark> to open the Session template creation screen. Here you can set up a new template's parameters, such as:&#x20;

* template name
* basing timezone&#x20;
* sessions list&#x20;
  * session name&#x20;
  * type: pre-market, main, post-market&#x20;
  * start and end time days of the week when is valid

You may create as many sessions per one template as you need, but be attentive to avoid intersection sessions (the platform will notify you about it). Once you finish setting the sessions template, click the <mark style="background-color:blue;">**Save**</mark> button and proceed to the assignment process.

## Assign template to symbols/connections

![Sessions template assignment screen](<../.gitbook/assets/image2 (2).png>)

To assign previously created templates to some symbol, you need to call the Sessions assignment screen by clicking the "Assign sessions" button on the toolbar. The following screen allows you to specify the "accuracy" of the assignment based on the symbol's hierarchy levels:

* Connection (all connections or the specific one)&#x20;
* Exchange (all or specific exchanges of the selected connection)&#x20;
* Symbol (all or specific symbols of the selected exchange of the selected connection)

## Manage session assignments

![Sessions manager screen](../.gitbook/assets/image4.png)

Next, select the Sessions template to assign and click the "Assign" button. From this moment, you will find a new row in a Sessions manager screen, stating that there is an active custom sessions assignment available in your Quantower. Here you can:&#x20;

* quickly Enable/Disable this assignment (using the checkbox) and see how the corresponding Status column value changes;&#x20;
* open the assignment parameters;&#x20;
* create a copy of the current assignment and modify it;&#x20;
* completely delete some assignments.

**To edit the Sessions templates**, click the corresponding button and find them below the "Create new" option in the context menu. By clicking on the existing template, you will find its editing screen and the possibility to update or delete it.

## Apply template via the panel settings

![Apply custom sessions template in panel settings](../.gitbook/assets/image1.png)

While the above workflow is about the centralized session's assignment, we left a possibility to quickly assign some sessions templates on a panel basis. Just open the panel's settings and find the Custom session parameter (usually in the General section). Initially, it is set up to Default mode, meaning that the panel will use the Sessions manager setting or the defaults provided by the vendor. Still, you can easily override it and use any available sessions template (use the Sessions manager to manage your templates).

The new Sessions manager screen significantly raises the level of custom sessions control, bringing you outstanding possibilities and ease of use. We put a considerable effort into covering possible scenarios of using the custom sessions but are still sure that you can find even more ideas on this functionality, so please share them in the comments or write on our socials.
