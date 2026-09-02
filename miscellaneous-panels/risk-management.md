---
description: >-
  Create risk plan templates with daily profit and loss limits, max order and
  position sizes, then assign them to any account or connection in Quantower.
---

# Risk Management

<figure><img src="../.gitbook/assets/Template of risk plan in Quantower (1).png" alt=""><figcaption></figcaption></figure>

The **Risk Management** panel lets you define and enforce trading rules across your accounts — automatically. Instead of monitoring positions and P\&L by hand, you create a **risk plan template** that sets hard limits and pairs each limit with an action. Quantower then watches those limits in real time and acts the moment one is breached.

The panel is currently in **Beta**, so some behaviors may change in upcoming releases.

### Opening the Panel

Go to **Control Center → Risk Management**. The panel opens with one active control at the top:&#x20;

* **\[+]** button for creating a new risk template for further assignment.

<figure><img src="../.gitbook/assets/Risk management panel Quantower.png" alt=""><figcaption></figcaption></figure>

### Create a Risk Plan Template

A template is the set of rules Quantower will enforce. Click **\[+]** button to open the template editor.

Give the template a name, then work through the **Rules list**. Each rule has a checkbox — only checked rules are active. Unchecked rules are saved with the template but ignored at runtime, so you can prepare rules without enabling them yet.

<figure><img src="../.gitbook/assets/Template of risk plan in Quantower.png" alt=""><figcaption></figcaption></figure>

#### Order and Position Limits

These rules cap how much you can trade at any moment. They trigger a hard block — Quantower will refuse the order or prevent the position from opening.

| Rule                                 | What it controls (meaning)                                                              |
| ------------------------------------ | --------------------------------------------------------------------------------------- |
| Max order quantity                   | Maximum size of a single order                                                          |
| Max total orders quantity            | Combined size of all orders at once                                                     |
| Max position quantity                | Maximum size of a single open position                                                  |
| Max total positions quantity         | Combined size of all open positions                                                     |
| Max position quantity by side        | Maximum position size on one side (Buy **or** Sell — select the side from the dropdown) |
| Max total positions quantity by side | Same as above but across all positions on that side                                     |

For the **by side** rules, use the dropdown next to the value to specify which side the limit applies to.

#### P\&L Limits

These rules watch your realized and unrealized profit and loss throughout the session. Each one has an **action** — what Quantower does the moment the threshold is crossed.

| Rule                          | What it controls (meaning)                     |
| ----------------------------- | ---------------------------------------------- |
| Day profit limit              | Maximum intraday realized profit               |
| Day loss limit                | Maximum intraday realized loss                 |
| Open profit limit             | Maximum unrealized profit across all positions |
| Open loss limit               | Maximum unrealized loss across all positions   |
| Open profit limit by position | Unrealized profit cap per individual position  |
| Open loss limit by position   | Unrealized loss cap per individual positio     |

#### Account State Limits

These rules monitor your account balance and equity directly.

| Rule                      | What it controls      |
| ------------------------- | --------------------- |
| Max account balance limit | Upper balance ceiling |
| Min account balance limit | Lower balance floor   |
| Max account equity limit  | Upper equity ceiling  |
| Min account equity limit  | Lower equity floor    |

#### Available Actions

Each P\&L and account-state rule has its own action that fires when the limit is hit:

* **Do nothing** — the rule is logged but no automatic trade is placed. Useful for monitoring before you're ready to enforce.
* **Flatten** — Quantower immediately closes all open positions and cancels working orders.
