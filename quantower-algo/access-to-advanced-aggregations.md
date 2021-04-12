---
description: Using the available aggregation types in your code
---

# Access to advanced aggregations

## Theory

As we know, chart aggregation is a type of displaying aggregated values. These values are price, volume and time. The main idea of each aggregation is to help traders analyze the state of the market in history and in real time.

At this moment, Quantower API supports **9** **aggregation types**. All of them you can use in your scripts easily. But before we continue, please read the article [how to download history](https://help.quantower.com/quantower-algo/downloading-history) by using Quantower API.

To download aggregated history we need use [**GetHistory** ](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.Symbol.html#TradingPlatform_BusinessLayer_Symbol_GetHistory_TradingPlatform_BusinessLayer_HistoryRequestParameters_)method which takes instanse of [HistoryRequestParameters ](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.HistoryRequestParameters.html)class as input parameter. This class contains the necessary properties such as FromTime, ToTime, HistoryType, etc. with which we can flexibly customize our request. But today we are interested in the [**Aggregation** ](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.HistoryRequestParameters.html#TradingPlatform_BusinessLayer_HistoryRequestParameters_Aggregation)property. This property contains instance of [HistoryAggregation ](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.HistoryAggregation.html)class which is base class for all available aggregation types. All we need to get the aggregated history is to set to this property instance of required aggregation type.

Listed below are all available aggregation classes with examples of history requests.

## Available aggregation classes

### Tick aggregation

The [**HistoryAggregationTick** ](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.HistoryAggregationTick.html)class is used to buid simple Tick ****chart.

```csharp
new HistoryAggregationTick(int ticksCount);
```

* **ticksCount** - the number of ticks for aggregation.

```csharp
var tickhistoricalData = this.Symbol.GetHistory(new HistoryRequestParameters()
{
    Symbol = this.Symbol,
    FromTime = DateTime.Now.AddHours(-3),
    ToTime = DateTime.Now,
    HistoryType = this.Symbol.VolumeType == SymbolVolumeType.Volume ? HistoryType.Last : HistoryType.BidAsk,
    Period = Period.TICK1,
    Aggregation = new HistoryAggregationTick(1),
});
```

### Time aggregation

The [**HistoryAggregationTime** ](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.HistoryAggregationTime.html)class is used to build the ****[Time ](https://help.quantower.com/analytics-panels/chart/chart-types/time-aggregation)chart.

```csharp
new HistoryAggregationTime(Period period);
```

* **period** - period of time \(8s, 30min, 4h etc\). Instance of [Period ](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.Period.html)structure.

```csharp
var timeBarHistoricalData = this.Symbol.GetHistory(new HistoryRequestParameters()
{
    Symbol = this.Symbol,
    FromTime = DateTime.Now.AddDays(-3),
    ToTime = DateTime.Now,
    HistoryType = this.Symbol.HistoryType,
    Period = Period.MIN15,
    Aggregation = new HistoryAggregationTime(Period.MIN15),
});
```

### Heiken-Ashi aggregation

The [**HistoryAggregationHeikenAshi** ](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.HistoryAggregationHeikenAshi.html)class is used to build the ****[Heiken-Ashi](https://help.quantower.com/analytics-panels/chart/chart-types/heiken-ashi) ****chart.

```csharp
new HistoryAggregationHeikenAshi(HeikenAshiSource source, int value);
```

* **source** - enum, base period of time \(Tick, Seconds. Minutes etc\).
* **value** - the amount of 'source' time.

```csharp
var heikenAshiHistoricalData = this.Symbol.GetHistory(new HistoryRequestParameters()
{
    Symbol = this.Symbol,
    FromTime = DateTime.Now.AddDays(-3),
    ToTime = DateTime.Now,
    HistoryType = this.Symbol.HistoryType,
    Aggregation = new HistoryAggregationHeikenAshi(HeikenAshiSource.Minute, 1),
});
```

### Range Bars aggregation

The [**HistoryAggregationRangeBars** ](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.HistoryAggregationRangeBars.html)class is used to build the ****[Range Bars](https://help.quantower.com/analytics-panels/chart/chart-types/range-bars) ****chart.

```csharp
new HistoryAggregationRangeBars(int rangeBars);
```

* **rangeBars** - the height \(in ticks\) of each bar.

```csharp
var rangeBarHistoricalData = this.Symbol.GetHistory(new HistoryRequestParameters()
{
    Symbol = this.Symbol,
    FromTime = DateTime.Now.AddHours(-3),
    ToTime = DateTime.Now,
    HistoryType = this.Symbol.HistoryType,
    Aggregation = new HistoryAggregationRangeBars(10),
});
```

### Renko aggregation

The [**HistoryAggregationRenko** ](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.HistoryAggregationRenko.html)class is used to build the [Renko ](https://help.quantower.com/analytics-panels/chart/chart-types/renko)chart.

```csharp
new HistoryAggregationRenko(Period period, int brickSize, RenkoStyle renkoStyle, int extension = 100, int inversion = 100, bool showWicks = false, bool buildCurrentBar = true)
```

* **period** - base period of time. Instance of [Period ](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.Period.html)structure.
* **brickSize** - required size of renko brick
* **renkoStyle** - enum, calculation methods \(Classic, HighLow, AdvancedClassic, AdvancedHighLow\)

```csharp
var renkoHistoricalData = this.Symbol.GetHistory(new HistoryRequestParameters()
{
    Symbol = this.Symbol,
    FromTime = DateTime.Now.AddDays(-1),
    ToTime = DateTime.Now,
    HistoryType = this.Symbol.HistoryType,
    Aggregation = new HistoryAggregationRenko(Period.MIN1, 10, RenkoStyle.AdvancedClassic, 100, 100, true, true),
});
```

### Line break aggregation

The [**HistoryAggregationLineBreak**](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.HistoryAggregationLineBreak.html) ****class is used to build the ****[Line break](https://help.quantower.com/analytics-panels/chart/chart-types/line-break) chart.

```csharp
new HistoryAggregationLineBreak(Period period, int lineBreak); 
```

* **period** - base period of time. Instance of [Period ](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.Period.html)structure.
* **lineBreak** - line break value.

```csharp
var lineBreakHistoricalData = this.Symbol.GetHistory(new HistoryRequestParameters()
{
    Symbol = this.Symbol,
    FromTime = DateTime.Now.AddDays(-1),
    ToTime = DateTime.Now,
    HistoryType = this.Symbol.HistoryType,
    Aggregation = new HistoryAggregationLineBreak(Period.MIN15, 3),
});
```

### Kagi aggregation

The [**HistoryAggregationKagi** ](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.HistoryAggregationKagi.html)class is used to build the [Kagi](https://help.quantower.com/analytics-panels/chart/chart-types/kagi) chart.

```csharp
new HistoryAggregationKagi(Period period, int reversal);
```

* **period** -  base period of time. Instance of [Period ](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.Period.html)structure.
* **reversal** - the amount of price movement that required for the Kagi line to reverse direction.

```csharp
var kagiHistoricalData = this.Symbol.GetHistory(new HistoryRequestParameters()
{
    Symbol = this.Symbol,
    FromTime = DateTime.Now.AddDays(-1),
    ToTime = DateTime.Now,
    HistoryType = this.Symbol.HistoryType,
    Aggregation = new HistoryAggregationKagi(Period.MIN15, 10),
});
```

### Points & Figures aggregation

The [**HistoryAggregationPointsAndFigures**](https://help.quantower.com/analytics-panels/chart/chart-types/points-and-figures) ****class is used to build the [Points & Figures](https://help.quantower.com/analytics-panels/chart/chart-types/points-and-figures) chart.

```csharp
new HistoryAggregationPointsAndFigures(Period period, int boxSize, int reversal, PointsAndFiguresStyle style);
```

* **period** - base period of time. Instance of [Period ](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.Period.html)structure.
* **boxSize** -  price range \(the number of ticks\) for X-Columns or O-Columns
* **reversal** - a parameter that indicates the number of Box Sizes that the price should go in the opposite direction to begin a new column.
* **style** - enum, calculation methods \(Classic, HighLow\)

```csharp
var pointFiguresHistoricalData = this.Symbol.GetHistory(new HistoryRequestParameters()
{
    Symbol = this.Symbol,
    FromTime = DateTime.Now.AddDays(-1),
    ToTime = DateTime.Now,
    HistoryType = this.Symbol.HistoryType,
    Aggregation = new HistoryAggregationPointsAndFigures(Period.TICK1, 100, 50, PointsAndFiguresStyle.HighLow),
});
```

### Volume Bars aggregation 

The **HistoryAggregationVolume** class is used to build the [Volume bars ](https://help.quantower.com/analytics-panels/chart/chart-types/volume-bars)chart.

```csharp
new HistoryAggregationVolume(int volumeValue);
```

* **volumeValue** - base volume value of bar

```csharp
var volumeBarsHistoricalData = this.Symbol.GetHistory(new HistoryRequestParameters()
{
    Symbol = this.Symbol,
    FromTime = DateTime.Now.AddHours(-4),
    ToTime = DateTime.Now,
    Period = Period.TICK1,
    HistoryType = this.Symbol.HistoryType,
    Aggregation = new HistoryAggregationVolume(1000),
});
```

## Practice

In this part of the article, we will create a simple strategy script in which we will try to apply the knowledge. Let's describe our actions step by step:

1. Create **HistoricalData** instance by loading 6 hours of **Renko** history. 
2. Create **Fast SMA** and **Slow SMA** indicators and then attach them to our HistoricalData.
3. Display **metrics**:
   1. Fast SMA value
   2. Slow SMA value
   3. Current brick high price
   4. Current brick low price
4. Log **high** and **low** prices of each new brick.

![](../.gitbook/assets/renkostrategy%20%282%29.png)

### Input parameters

First, let’s define input parameters. In this section, we want to be able to change the aggregation parameters and indicator base settigns.

```csharp
[InputParameter("Symbol", 10)]
public Symbol Symbol;

[InputParameter("Renko period", 20)]
public Period RenkoPeriod = Period.MIN1;

[InputParameter("Brick size", 30)]
public int BrickSize = 10;

[InputParameter("Renko style", 40, variants: new object[]
{
    "Classic", RenkoStyle.Classic,
    "High/Low", RenkoStyle.HighLow,
    "Adv. Classic", RenkoStyle.AdvancedClassic,
    "Adv. High/Low", RenkoStyle.AdvancedHighLow,
})]
public RenkoStyle RenkoStyle = RenkoStyle.Classic;

[InputParameter("Fast SMA period", 50, 1, 9999, 1, 0)]
public int FastSmaPeriod = 10;

[InputParameter("Slow SMA period", 50, 1, 9999, 1, 0)]
public int SlowSmaPeriod = 30;

private HistoricalData renkoHistoricalData;
private Indicator fastSmaIndicator;
private Indicator slowSmaIndicator;
```

### OnRun method

In this section, we will carry out the first, second and fourth points. 

{% hint style="info" %}
Pay attention to line **24**. Here we create instance of [**HistoryAggregationRenko**](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.HistoryAggregationRenko.html) class and pass required parameters.

Pay attention ****to line **30**. Here we subscribe '**NewHistoryItem**' event. Another words, our 'RenkoHistoricalData\_NewHistoryItem' handler will trigger on each new brick item.
{% endhint %}

```csharp
protected override void OnRun()
{
    //
    // check is symbol is null
    //
    if (Symbol == null)
    {
        Log("Symbol is null", StrategyLoggingLevel.Error);
        Stop();
        return;
    }

    try
    {
        //
        // Download history (use Renko aggregation)
        //
        renkoHistoricalData = Symbol.GetHistory(new HistoryRequestParameters()
        {
            Symbol = Symbol,
            HistoryType = Symbol.HistoryType,
            FromTime = Core.Instance.TimeUtils.DateTimeUtcNow.AddHours(-6),
            ToTime = default,
            Aggregation = new HistoryAggregationRenko(RenkoPeriod, BrickSize, RenkoStyle)
        });

        //
        // Subscribe to 'NewHistoryItem' event 
        //
        renkoHistoricalData.NewHistoryItem += RenkoHistoricalData_NewHistoryItem;

        //
        // Create Fast/Slow SMA indicators
        //
        fastSmaIndicator = Core.Instance.Indicators.BuiltIn.SMA(FastSmaPeriod, PriceType.Close);
        slowSmaIndicator = Core.Instance.Indicators.BuiltIn.SMA(SlowSmaPeriod, PriceType.Close);

        //
        // Attach our indicators to downloaded HistoricalData
        //
        renkoHistoricalData.AddIndicator(fastSmaIndicator);
        renkoHistoricalData.AddIndicator(slowSmaIndicator);
    }
    catch (Exception ex)
    {
        Log(ex.Message, StrategyLoggingLevel.Error);
        Stop();
    }
}

private void RenkoHistoricalData_NewHistoryItem(object sender, HistoryEventArgs e)
{
    // get high price for new brick
    var highPrice = e.HistoryItem[PriceType.High];

    // get low price for new brick
    var lowPrice = e.HistoryItem[PriceType.Low];

    // print message
    Log($"New brick  --  High: {highPrice} | Low: {lowPrice}", StrategyLoggingLevel.Info);
}
```

### OnGetMetrics method

Here we create required metrics. 

{% hint style="info" %}
Pay attention to line 10. Here we use '**FormatPrice**' method to format indicator value to symbol tick size.
{% endhint %}

```csharp
protected override List<StrategyMetric> OnGetMetrics()
{
    var result = base.OnGetMetrics();

    if (fastSmaIndicator != null)
    {
        result.Add(new StrategyMetric()
        {
            Name = "Fast SMA value",
            FormattedValue = Symbol.FormatPrice(fastSmaIndicator.GetValue())
        });
    }

    if (slowSmaIndicator != null)
    {
        result.Add(new StrategyMetric()
        {
            Name = "Slow SMA value",
            FormattedValue = Symbol.FormatPrice(slowSmaIndicator.GetValue())
        });
    }

    if (renkoHistoricalData != null)
    {
        result.Add(new StrategyMetric()
        {
            Name = "Current brick high price",
            FormattedValue = Symbol.FormatPrice(renkoHistoricalData[0][PriceType.High])
        });
        result.Add(new StrategyMetric()
        {
            Name = "Current brick low price",
            FormattedValue = Symbol.FormatPrice(renkoHistoricalData[0][PriceType.Low])
        });
    }

    return result;
}
```

### OnStop method 

Never forget to remove unused objects and unsubscribe form unused events.

```csharp
protected override void OnStop()
{
    if (renkoHistoricalData != null)
    {
        //
        // remove 'fastSmaIndicator' instance
        //
        if (fastSmaIndicator != null)
            renkoHistoricalData.RemoveIndicator(fastSmaIndicator);

        //
        // remove 'slowSmaIndicator' instance
        //
        if (slowSmaIndicator != null)
            renkoHistoricalData.RemoveIndicator(slowSmaIndicator);
        
        //
        // unsubscribe from 'NewHistoryItem' event and dispose our HistoricalData instance
        //       
        renkoHistoricalData.NewHistoryItem -= RenkoHistoricalData_NewHistoryItem;
        renkoHistoricalData.Dispose();
    }
}
```

