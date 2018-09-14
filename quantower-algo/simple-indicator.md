# Simple Indicator

In this topic we will show you how simple is writing indicators in Quantower. We will use Quantower Algo extension for Visual Studio, but main principles are valid for all development environments. If you don't have Visual Studio or Quantower Algo extension installed you can [read our topic](https://help.quantower.com/quantower-algo/installing-visual-studio) which will help you with this.

## So, what is indicator in general?

Indicator is mathematical calculations based on a symbol's price and/or volume. The result is used for displaying on the chart and to help trader make a correct decision. From technical point view Indicator in Quantower is set of lines with buffers. Each element of buffer is assigned to historical bar or tick on the chart. All you need  is to make required calculation for each bar and put the result into this buffer. 

An indicator is mathematical calculations based on a symbol's price and/or volume. The result is used for displaying on the chart and to help trader make a correct decision. From technical point view Indicator in Quantower is a set of lines with buffers. Each element of the buffer is assigned to a historical bar or tick on the chart. All you need is to make a required calculation for each bar and put the result into this buffer.

Sounds not very difficult, doesn't it? Let's start! As for example we will write a code that will implement algorithm of Simple Moving Average indicator.

Use "_**File -&gt; New project**_" in the main menu of Visual Studio to open "**New project**" window. Find "**Quantower Algo**" group and select "**Indicator**" template:

At first, you need to create a new project for the indicator. Quantower Algo provides you predefined templates for an empty indicator as well as a few examples of real indicators with source code.

![New Project window](../.gitbook/assets/new-project.png)

A minimum required source code will be generated automatically and contains the main Indicator functions:

![Default source code for blank indicator](../.gitbook/assets/default-code.png)

It is time to go deep into the code. In a **constructor** method you can specify name of indicator, short name for displaying on the charts and whether you indicator require separate window on the chart. The most important here is specifying the amount of lines and their default style: Line/Dot/Histogram, color, width. In our example we need only one line, but you can add any amount you need:

```csharp
/// <summary>
/// Indicator's constructor. Contains general information: name, description, LineSeries etc. 
/// </summary>
public SimpleIndicator()
    : base()
{
    // Defines indicator's name and description.
    Name = "SimpleIndicator";
    Description = "My indicator's annotation";

    // Defines line on demand with particular parameters.
    AddLineSeries("line1", Color.CadetBlue, 1, LineStyle.Solid);

    // By default indicator will be applied on main window of the chart
    SeparateWindow = false;
}
```

In a constructor method, you can specify a name of indicator, short name for displaying on the charts and whether you indicator requires a separate window on the chart. The most important here is specifying the number of lines and their default style: Line/Dot/Histogram, color, width. In our example, we need only one line, but you can add any amount you need.

**OnUpdate** method will be called each time on history changing - here we need to add our calculations. Most of indicators are using prices or volumes in their algorithms. Quantower API provides you a few ways to retrieve this data - you can access Open, High, Low, Close and others data from current bar or for previous bars if it required. 

Common method [**GetPrice**](http://api.quantower.com/docs/TradingPlatform.BusinessLayer.Indicator.html#TradingPlatform_BusinessLayer_Indicator_GetPrice_TradingPlatform_BusinessLayer_PriceType_System_Int32_), allows to retrieve all type of the data

```csharp
// To get Low price of the current bar
double low = GetPrice(PriceType.Low);
// To get Volume price for the fifth bar before the current
double volume = GetPrice(PriceType.Volume, 5);    
```

And simplified ways to retrieve the data:

```csharp
// To get Close price of the current bar
double close = Close();
// To get High price of the current bar
double high = High();
// To get Open price for the fifth bar before the current
double open = Open(5);   
```

You can find more information about **Indicator** class in our [API documentation](http://api.quantower.com).

Now we know how to get prices. We can add required calculations using standard C\# possibilities. And, as we told before, we need to put results into indicator buffer. We can use [**SetValue**](http://api.quantower.com/docs/TradingPlatform.BusinessLayer.Indicator.html#TradingPlatform_BusinessLayer_Indicator_SetValue_System_Double_System_Int32_System_Int32_) method:

```csharp
// Put value into current bar for first line of indicator
SetValue(1.43);
// Put value into current bar for second line of indicator
SetValue(1.43, 1);
// Put value into fifth bar before the current bar for second line of indicator
SetValue(1.43, 1, 5);
```

Now we know everything required to finish our first indicator. It is ready to use in trading platform. We need to compile it - Press Build button on the toolbar. Quantower Algo will automatically copy your indicator to assigned Quantower you can add this indicator on the chart.

