# Example: Simple Moving Average

In this example we will develop a simple moving average indicator. Let's, create an indicator template project and start.

{% hint style="info" %}
See examples of some strategies, integrations and indicators in our [Github repository](https://github.com/Quantower/Examples)
{% endhint %}

### Input parameters

First of all it is important to decide what parameters will our indicator have. We are building a simple moving average, so it will have only two parameters: **Period** and **Price type,** that will be used for calculations

```csharp
#region Parameters
// First input parameter
[InputParameter("Period of Simple Moving Average", 0, 1, 999, 1, 1)]
public int Period = 10;

// Second input parameter
[InputParameter("Sources prices for MA", 1, variants: new object[]{
    "Close", PriceType.Close,
    "Open", PriceType.Open,
    "High", PriceType.High,
    "Low", PriceType.Low,
    "Typical", PriceType.Typical,
    "Median", PriceType.Median,
    "Weighted", PriceType.Weighted
})]
public PriceType SourcePrice = PriceType.Close;
#endregion Parameters
```

Ok, done let's go ahead 

### Indicator's general info

Our next step is to set a general indicators info, all this information you will see in Indicator's lookup, when you decide to select it. Also, here we need to define how many data series will our indicator have and should it be drawn in separate window or directly on a chart.

All these tasks we can solve in constructor function, ok great, let's do it

```csharp
public SMA()
    : base()
{
    // Here we set an indicator's name and description
    Name = "Simple Moving Average Example";
    Description = "Average price for the last N periods";
    ShortName = "SMA (" + Period + ":" + SourcePrice.ToString() + ")";

    // Our indicator has only one line 
    AddLineSeries("SMA", Color.Red, 1, LineStyle.Solid);

    //Indicator will be drawn directly on chart 
    SeparateWindow = false;
}
```

### Core logic

We will save **OnInit** function empty, because our indicator does not require any one-time logic that should be executed when we add indicator on a chart

```csharp
protected override void OnInit()
{

}
```

All calculations will occur when we receive a new quote, to process it we need to override **OnUpdate** function

```csharp
protected override void OnUpdate(UpdateArgs args)
{
    // Checking, if current amount of bars
    // more, than period of moving average. If it is
    // then the calculation is possible
    if (Count <= Period)
        return;

    double sum = 0.0; // Sum of prices
    for (int i = 0; i < Period; i++)
        // Adding bar's price to the sum
        sum += GetPrice(SourcePrice, i);

    // Set value to the "SMA" line buffer.
    SetValue(sum / Period);
}
```

Pay your attention at: 

```csharp
if (Count <= Period)
    return;
```

Here we check is it enough historical bars to calculate one indicator's point, if yes - we continue calculation otherwise skip it.

To calculate average price we need to request price data, we can do it by calling **GetPrice** function

```csharp
sum += GetPrice(SourcePrice, i);
```

Once, all calculations are done we set the result value to indicators data serie

```csharp
// Set value to the "SMA" line buffer.
SetValue(sum / Period);
```

### All source code

That is all, that was easy. As a conclusion take a look at all source code

```csharp
// Copyright QUANTOWER LLC. © 2017-2018. All rights reserved.
using System;
using System.Drawing;
using TradingPlatform.BusinessLayer;

namespace MovingAverages
{
    public class SMA : Indicator
    {
        #region Parameters
        // First input parameter
        [InputParameter("Period of Simple Moving Average", 0, 1, 999, 1, 1)]
        public int Period = 10;
        
        // Second input parameter
        [InputParameter("Sources prices for MA", 1, variants: new object[]{
            "Close", PriceType.Close,
            "Open", PriceType.Open,
            "High", PriceType.High,
            "Low", PriceType.Low,
            "Typical", PriceType.Typical,
            "Median", PriceType.Median,
            "Weighted", PriceType.Weighted
        })]
        public PriceType SourcePrice = PriceType.Close;
        #endregion Parameters

        /// <summary>
        /// Indicator's constructor. Contains general information: name, description, LineSeries etc. 
        /// </summary>
        public SMA()
            : base()
        {
            // Here we set an indicator's name and description
            Name = "Simple Moving Average Example";
            Description = "Average price for the last N periods";
            ShortName = "SMA (" + Period + ":" + SourcePrice.ToString() + ")";
        
            // Our indicator has only one line 
            AddLineSeries("SMA", Color.Red, 1, LineStyle.Solid);
        
            //Indicator will be drawn directly on chart 
            SeparateWindow = false;
        }

        /// <summary>
        /// This function will be called after creating an indicator as well as after its input params reset or chart (symbol or timeframe) updates.
        /// </summary>
        protected override void OnInit()
        {

        }

        /// <summary>
        /// Calculation entry point. This function is called when a price data updates. 
        /// Will be runing under the HistoricalBar mode during history loading. 
        /// Under NewTick during realtime. 
        /// Under NewBar if start of the new bar is required.
        /// </summary>
        /// <param name="args">Provides data of updating reason and incoming price.</param>
        protected override void OnUpdate(UpdateArgs args)
        {
            // Checking, if current amount of bars
            // more, than period of moving average. If it is
            // then the calculation is possible
            if (Count <= Period)
                return;

            double sum = 0.0; // Sum of prices
            for (int i = 0; i < Period; i++)
                // Adding bar's price to the sum
                sum += GetPrice(SourcePrice, i);

            // Set value to the "SMA" line buffer.
            SetValue(sum / Period);
        }
    }
}

```

