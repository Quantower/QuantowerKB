# Directional Movement Index (DMI) Indicator

### What is the Directional Movement Index (DMI) Indicator?

**Directional Movement Index (DMI)** assists in determining if an asset is trending and attempts to measure the strength of the trend. The DMI disregards the direction of the asset. It only attempts to determine if there is a trend and that trends strength.

The indicator is made up of 2 indicator lines:

1. **Positive Directional Indicator (+DMI)** shows the difference between today’s high price and yesterday’s high price. These values are then added up from the past 14 periods and then plotted.
2. **Negative Directional Indicator (–DMI)** shows the difference between today’s low price and yesterday’s low price. These values are then summed up from the past 14 periods and plotted.

![](<../../../../.gitbook/assets/image (58) (1).png>)

### How the Directional Movement Index (DMI) indicator works

A buy signal is given when DMI+ crosses above DMI-. A sell signal is given when DMI- crosses above DMI+. The ADX and ADXR lines are then used to measure the strength of these signals.

### Calculation of the Directional Movement Index (DMI) indicator

1. Calculate the True Range, +DI, and –DI for each period:\
   True Range is the greater of:\
   Current High – Current Low\
   Absolute value of Current High – Previous Close\
   Absolute value of Current Low – Previous Close\
   \
   \+DI\
   IF Current High – Previous High > Previous Low – Current Low\
   THEN +DI = the greater of Current High – Previous High OR 0\
   &#x20; \
   \-DI\
   IF Previous Low – Current Low > Current High – Previous High\
   THEN –DI = the greater of Previous Low – Current Low OR 0\
   \
   IF +DI AND -DI are both negative\
   THEN both +DI and –DI = 0\
   \
   IF +DI AND -DI are both positive AND +DI > -DI\
   THEN +DI = Current High – Previous High AND –DI = 0\
   Else IF +DI < -DI\
   THEN +DI = 0 AND –DI = Previous Low – Current Low\

2. Smooth the True Range, +DI, and –DI using Wilder’s smoothing technique.
3. Divide the smoothed +DI by the smoothed True Range and multiply by 100 (this is the +DI that is plotted for the specified period).
4. Divide the smoothed –DI by the smooth True Range and multiply by 100 (this is the –DI that is plotted for the specified period).
5. Next calculate the Directional Movement Index (DX) which equals the (absolute value of the smoothed +DI – the smoothed –DI) /( the sum of the smoothed +DI and smoothed –DI )and multiply by 100.
