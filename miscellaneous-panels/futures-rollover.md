# Futures Rollover

Traders should roll the current futures contract to avoid delivery or settlement at the contract's expiration. Rolling a contract involves closing the existing position and opening a new one in a later-dated contract, ensuring continuity in trading and managing positions more effectively while adapting to market conditions.

We offer two ways to roll over to the next futures contract (in case to keep your drawings valid on the next contract):

1. Through the **chart panel's context menu**.
2. Via the **Futures Rollover** panel.

## How to roll to the next contract via chart

To roll over a futures contract via the chart's context menu, simply <mark style="color:green;">**right-click on the chart**</mark>, select the nearest (or desired) contract under the **Rollover** submenu, and choose how to adjust your drawings. The platform will automatically switch to the new contract and preserve the position of your drawings relative to their placement on the previous contract.

<figure><img src="../.gitbook/assets/rollover futures via chart.gif" alt=""><figcaption></figcaption></figure>

## How to roll to the next futures contract using the Futures Rollover panel

1. In the platform's main menu, open the '<mark style="background-color:purple;">**Futures Rollover**</mark>' panel located in the '**Misc**' section.

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

2. Here, select the **Connection** for contract rollover, like a specific one (e.g., Rithmic) or for All active connections.

<figure><img src="../.gitbook/assets/image (3) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

3. Choose a **Rollover method**:
   * '**By Volume**': This method rolls over when the daily volume of the upcoming contract surpasses the current one.
   * '**Expired**': Identifies and rolls expired contracts to the current front contract.
   * '**Expiring Soon**': Rolls the current contract to the next if its expiration is within the specified days.

<figure><img src="../.gitbook/assets/image (392).png" alt=""><figcaption></figcaption></figure>

4. **Chart Drawing Adjustment** option allows you to modify the positioning of chart drawings concerning futures contract changes:
   * '**None**': Keeps drawings at the same price levels as the expired futures contract, without any adjustment.
   * '**By last price**': Adjusts drawings based on the price difference between the current and previous contracts.
   * '**By custom value**': Modifies drawing positions using a specified value to align with new pricing.
