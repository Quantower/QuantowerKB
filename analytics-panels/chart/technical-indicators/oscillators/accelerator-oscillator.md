---
description: >-
  Use the Accelerator Oscillator (AC) in Quantower to measure momentum
  acceleration and detect shifts before they show up in price
---

# Accelerator Oscillator

## Description

Accelerator Oscillator was introduced by Bill Williams in his book "Trading Chaos". According to Bill Williams' theory, the market price is the latest element that will be changed and prior to this change, the market-driven forces will change its direction.  The AC indicator measures acceleration and deceleration of these forces.  If the indicator rises, it means that the market is imbalanced now and buy power is greater than sell power, and vice versa. &#x20;

![](<../../../../.gitbook/assets/image (30).png>)

## Formula

MEDIAN PRICE = (HIGH + LOW) / 2\
AO = SMA (MEDIAN PRICE, 5) - SMA (MEDIAN PRICE, 34)\
AC = AO - SMA (AO, 5)<br>

Where:\
MEDIAN PRICE — median price;\
HIGH — the highest price of the bar;\
LOW — the lowest price of the bar;\
SMA — Simple Moving Average;\
AO — Awesome Oscillator.



## Most useful cases

* **Divergence/Convergence** - Divergence/Convergence pattern is a form of price action when a new high(low) of the price is not confirmed with a new high/low of  AC. Such price and indicator’s behavior can be interpreted as the weakness of the current existing trend.

![](<../../../../.gitbook/assets/image (32).png>)

* **Crossing the zero line** - this is a trend-reversing signal, and it can be very useful in case of determining a correction of the existing trend, the beginning of a new trend wave, or starting a new trend.
