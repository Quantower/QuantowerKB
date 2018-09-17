# Indicator with custom painting \(GDI\)

In this topic we will show you how to use a really great possibility of scripts in Quantower - a custom painting on the Chart. You can draw anything you need via GDI+ - a graphical subsystem of Windows. In C\# all features from GDI+ are encapsulated in class Graphics. It is a set of functions allows to create graphical primitives, splines, using Brushes and Pens, Images, etc. More information you can find on Microsoft documentation site.

Let's start. To get access to Graphics object of the chart you need to override OnPaint method and use Hdc value from its parameters:

```csharp
public override void OnPaintChart(PaintChartEventArgs args)
{
    // Use args.Hdc to create Graphics which give us acces to chart canvas
    Graphics gr = Graphics.FromHdc(args.Hdc);                        
    
    // Add your custom drawings here...
}
```

That's all - now you have full access to canvas and can draw anything you need. For drawings in C\# you need to call special methods and provide parameters for them, coordinates, color, width:

```csharp
public override void OnPaintChart(PaintChartEventArgs args)
{
    Graphics gr = Graphics.FromHdc(args.Hdc);
            
    // Draw a line using predefined Red pen
    gr.DrawLine(Pens.Red, 100,100,200,200);

    // Draw a rectangle using predefined Blue pen
    gr.DrawRectangle(Pens.Blue, 250, 100, 100, 100);

    // Fill a rectangle using predefined yellow brush
    gr.FillRectangle(Brushes.Yellow, 400, 100, 100, 100);            

    // Create a custom pen and use it for drawing
    Pen myPen = new Pen(Color.Green, 3);
    gr.DrawRectangle(myPen, 50, 50, 500, 200);
}
```

If we build this indicator - we can see results on the chart window:

![Drawing directly on the chart](../.gitbook/assets/primitives.png)

  
Lets try to draw a text - it is very similar, we need to specify text, font and coordinates:

```csharp
public override void OnPaintChart(PaintChartEventArgs args)
{
    Graphics gr = Graphics.FromHdc(args.Hdc);

    // Draw the text with specified font and color
    gr.DrawString("An examle if drawing text...", new Font("Arial", 20), Brushes.Red, 100, 100);    
}
```

Build this and check your chart:

![Drawing a text](../.gitbook/assets/text.png)

Ok, it is interesting, but quite useless. Let's do something more serious - for example, display top 5 levels of market depth on the the chart. This is source code:

```csharp
public override void OnPaintChart(PaintChartEventArgs args)
{
    Graphics gr = Graphics.FromHdc(args.Hdc);

    // Create a font
    Font font = new Font("Arial", 10);

    // Request a current sorting bids
    List<Level2Item> sortedBids = this.Symbol.Bids.GetSortedList();

    // Draw bids
    for (int i = 0; i < sortedBids.Count; i++)
        gr.DrawString(sortedBids[i].Quote.Price.ToString(), font, Brushes.LightGray, 20, 23 * i + 30);

    // Request a current sorting asks
    List<Level2Item> sortedAsks = this.Symbol.Asks.GetSortedList();

    // Draw asks
    for (int i = 0; i < sortedAsks.Count; i++)
        gr.DrawString(sortedAsks[i].Quote.Price.ToString(), font, Brushes.LightGray, 100, 23 * i + 30);     
}
```

And this how our chart looks now. You can compare results with Quantower Market Depth panel:

![Display bids and asks on the chart](../.gitbook/assets/level2.png)

It is a great possibility of chart features extending, isn't it? You can add your own Info Window, Track Cursor or even Volume Analysis visualization. There are no limitations from our API, only your fantasy.  


