# Reversal Bars

Reversal bars is a volatility-based chart type that builds a new bars after the price passes a specified amount of ticks in the opposite \(reversal\) direction.

![](../../../.gitbook/assets/image%20%28181%29.png)

## How do Reversal Bars is constructed?

There are two parameters that are involved in the calculations:

* **Length** is the minimum bar size after which a pullback can be counted.
* **Reversal Length** is the minimum size of pullback \(reversal\) after which the bar will be fixed and a new one starts to build.

