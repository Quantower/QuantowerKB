---
description: Instantiate a custom indicator with input parameters.
---

# Custom indicators access

## General

Quantower API provides a huge collection of built-in indicators. But sometimes we need to use our own indicator that we developed before or downloaded from the Internet. 

In this article, we will create an instance of the custom indicator and pass the input parameters in different ways.

Below you can see the custom indicator code. Let's imagine that it is a very useful script and that we want to use its calculation results in our code. But we are not satisfied with the default input parameters, so we want to change them.

```csharp
public class CustomIndicator : Indicator
{
    [InputParameter("Level", 10, 0.1, 9999, 0.1, 1)]
    public double LevelValue = 10;

    [InputParameter("Slow period", 20, 1, 9999, 1, 0)]
    public int SlowPeriod = 30;

    [InputParameter("Price type", variants: new object[]
    {
        "Close", PriceType.Close,
        "Open", PriceType.Open,
        "High", PriceType.High,
        "Low", PriceType.Low,
    })]
    public PriceType PriceType = PriceType.Close;

    [InputParameter("Period")]
    public Period Period = Period.MIN1;

    //
    // Parameterless constructor
    //
    public CustomIndicator()
    {
        this.Name = "Custom indicator";
        this.AddLineSeries("Line", Color.DodgerBlue, 2, LineStyle.Solid);

        this.SeparateWindow = true;
    }

    protected override void OnUpdate(UpdateArgs args)
    {
        // something usefull
    }
}
```

## Use class constructor \(Beginner\)

The easiest way to create and pass parameters is to use the class constructor. At this moment, our custom indicator has сonstructor that takes no parameters \(parameterless constructor\). Each indicator must have such a constructor.  
  
Let's add a new constructor for the **"CustomIndicator"** class in which we will override the default input parameters.

```csharp
public class CustomIndicator : Indicator
{
    // ...

    //
    // Parameterless constructor
    //
    public CustomIndicator()
    {
        this.Name = "Custom indicator";
        this.AddLineSeries("Line", Color.DodgerBlue, 2, LineStyle.Solid);

        this.SeparateWindow = true;
    }

    //
    // New constructor with parameters
    //
    public CustomIndicator(double levelValue, int slowPeriod, PriceType priceType, Period period)
         : this() // Don't forget to invoke parameterless constructor
    {
        this.LevelValue = levelValue;
        this.SlowPeriod = slowPeriod;
        this.PriceType = priceType;
        this.Period = period;
    }
    
    // ...
}
```

Now, in other indicators, we can use this constructor instead of default. For example in the **“OnInit”** method.

```csharp
class BestIndicator : Indicator
{       
    private Indicator customIndicator;
    
    protected override void OnInit()
    {
        this.customIndicator = new CustomIndicator(10, 500, PriceType.High, Period.DAY1);
        this.AddIndicator(this.customIndicator);
    }
      
    protected override void OnUpdate()
    {
        var indicatorValue = this.customIndicator.GetValue();
        
        // something usefull
    }
}
```

## **Use indicator settings collection \(Advance\)**

This method can be used if you are unable to add the required constructor. For example, you imported a dll-library with an indicator. Each indicator has a "Settings" property that contains all input parameters converted into objects of “[SettignItem](https://api.quantower.com/docs/TradingPlatform.BusinessLayer.SettingItemAction.html)” type.

To modify any of the parameters, you need to invoke the **"UpdateItemValue"** method and pass the name of the required parameter and the new value.

```csharp
class BestIndicator : Indicator
{       
    private Indicator customIndicator;
    
    //    
    protected override void OnInit()
    {
        var customIndicator = new CustomIndicator();
        var settings = customIndicator.Settings;

        try
        {
            settings.UpdateItemValue("Level", 12.5);
            settings.UpdateItemValue("Slow period", 55);
            settings.UpdateItemValue("Price type", new SelectItem("Open", PriceType.Open));
            settings.UpdateItemValue("Period", Period.MONTH1);
    
            this.AddIndicator(this.customIndicator);
        }
        catch (Exception ex)
        {
            // log exception
        }
    
        indicator.Settings = settings;
    }

    // 
    protected override void OnUpdate()
    {
        var indicatorValue = customIndicator.GetValue();
        
        // something usefull
    }
}

```

