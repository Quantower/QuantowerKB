# DOM Trader Columns

You can choose which columns to display in the DOM Trader panel by activating them through the Settings of the panel or through the context menu (right-click).

<details>

<summary><mark style="background-color:blue;">Available Columns</mark></summary>

**Price**

**Bids/Asks**

<mark style="color:orange;">**Bids**</mark> <mark style="color:orange;"></mark><mark style="color:orange;"></mark> <mark style="color:orange;"></mark>_<mark style="color:orange;">(optional)</mark>_

<mark style="color:orange;">**Asks**</mark> <mark style="color:orange;"></mark>_<mark style="color:orange;">(optional)</mark>_

**Buy/Sell**

<mark style="color:orange;">**Buy**</mark> <mark style="color:orange;"></mark>_<mark style="color:orange;">(optional)</mark>_

<mark style="color:orange;">**Sell**</mark> <mark style="color:orange;"></mark>_<mark style="color:orange;">(optional)</mark>_

****[**Liquidity changes**](dom-trader-columns.md#liquidity-changes-column-known-as-pulling-and-stacking)****

****[**Number of changes**](dom-trader-columns.md#number-of-changes)****

****[**Cumulative changes**](dom-trader-columns.md#cumulative-changes)****

**Comments**

**Last Trade Size**

**Bid Trade Size**

**Ask trade Size**

****[**Cumulative Size**](dom-trader-columns.md#cumulative-size)****

****[**Imbalance**](dom-trader-columns.md#imbalance)****

**Profit & Loss**

**Profiles**

</details>

### Liquidity changes column (known as Pulling and Stacking)

Pulling and Stacking describe the summary of the Liquidity Order Book (LOB) for Bid and Ask Side separately. Stacking shows an increasing Volume in the Order Book for the Sell-Side (Ask) or Buy-Side (Bid) and reflects therefore a supportive intention for the price to move in the corresponding direction. Whereas the Pulling shows a decrease in the Volume in the Order Book and therefore a lack of interest.

![](../../.gitbook/assets/image.png)

### **Number of changes**

It shows how many times the values have changed at a particular price level (Bids x Asks) since the panel launched.

### **Cumulative changes**

It shows the total volume that changed at a specific price level since the panel launched.

#### _Why Number of Changes and Cumulative changes are important?_

The liquidity in the Depth of market is constantly changing due to very different types of reasons. The fast changes occurring simultaneously on the bid and ask sides are very difficult to track with the naked eye. It becomes even worse when you have over 10 levels.

This is the part where the number of changes and cumulative changes comes on handy. For a buy trade, you would expect to see an increasing number of changes combined with higher cumulative changes showing increasingly adding liquidity at a higher pace. Even better, would it be combined with a higher cumulative change on the ask side to the downside, showing participants eager pulling out the liquidity.

### **Cumulative Size**&#x20;

It shows the sum of Limit order volumes for each subsequent level. This histogram allows estimating the dominating side of the market.

### **Imbalance**&#x20;

It shows how many percents of buyers are more than sellers (and vice versa) for each price level.
