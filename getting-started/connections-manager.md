# Connections manager

Connections are the integrations with third-party providers that supply various data: trading quotes, symbols history etc. 

{% hint style="success" %}
Each integration is developed and tested by Quantower specialists and guarantees the stability and security of all transferred information. 
{% endhint %}

## Video

{% embed data="{\"url\":\"https://www.youtube.com/watch?v=7Sp2e\_N-U0E\",\"type\":\"video\",\"title\":\"How to: Connections manager\",\"description\":\"Quantower allows connecting with several integrations simultaneously. This is not complicated, but in case you\'re confused, this short video should display the connection process from scratch.\",\"icon\":{\"type\":\"icon\",\"url\":\"https://www.youtube.com/yts/img/favicon\_144-vfliLAfaB.png\",\"width\":144,\"height\":144,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://i.ytimg.com/vi/7Sp2e\_N-U0E/maxresdefault.jpg\",\"width\":1280,\"height\":720,\"aspectRatio\":0.5625},\"embed\":{\"type\":\"player\",\"url\":\"https://www.youtube.com/embed/7Sp2e\_N-U0E?rel=0&showinfo=0\",\"html\":\"<div style=\\\"left: 0; width: 100%; height: 0; position: relative; padding-bottom: 56.2493%;\\\"><iframe src=\\\"https://www.youtube.com/embed/7Sp2e\_N-U0E?rel=0&amp;showinfo=0\\\" style=\\\"border: 0; top: 0; left: 0; width: 100%; height: 100%; position: absolute;\\\" allowfullscreen scrolling=\\\"no\\\"></iframe></div>\",\"aspectRatio\":1.7778}}" %}

## General information

**Connections manager** — is a screen that allows you to select from available integrations the ones you are trading with and connect to them using your accounts. While connecting to any integration, Connections manager remembers your login credentials and will use them for further auto-connects \(reconnects in case of errors\). If you don’t want to store your login credentials in manager, just click the “Lock” icon in the login form. 

![Connections manager screen](../.gitbook/assets/connectionsscreen.png)

Connections manager screen consists of two columns: connections list & connection info. Connection info column holds an information about the active connection or Login form, in case if the current connection is not active.

Each active connection is marked with green Status dot by the left hand from its name. The "_**Star**_" icon indicates that connection is favorite and displayed on Control center toolbar. This icon is also used to **add/remove** a connection **from favorites**.

Connection login form varies depending on integration requirements. Usually, it has Login & password fields and “_**Connect**_” button. This button initiates the authorization process. Some integrations have settings \(a “_**Gear**_” icon on the right side of connection logo\) and account creation button \(a “_**User with plus**_” icon on the right side of “_**Connect**_” button\). Account creation redirects you to the integration vendor website.

Once connected, info column will contain the data about ping and current connection status text. There is a “_**Disconnect**_” button also.

## Multi-connect

{% hint style="info" %}
Quantower supports multiple connections simultaneously, but this function can be limited by your account license
{% endhint %}



