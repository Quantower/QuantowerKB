# TPO Profile Chart

**Time Price Opportunity** or **TPO Chart**, shows the price distribution during the specified time, thus forming a profile. This allows you to understand at which levels or ranges the price has spent the most time, as well as to determine the main support and resistance levels.

![TPO Profile Chart \(Market Profile\) general view in Quantower platform](../.gitbook/assets/tpo-profile-chart-general-view.png)

To open new TPO panel, go to _**Main menu**_ \(Logo icon\) and select _**TPO Chart**_ in the Analytics section.

![Open TPO Chart panel via Main menu](../.gitbook/assets/tpo_start.png)

### Key Elements of TPO Profile Chart

**Point of Control \(POC\)** — price level of the greatest market activity or trading volume. At this level, the price spent most time over the profile range.

**Value Area** — price range in which approximately 68% - 70% of the market activity or trading volume took place.

**Singles** or **single prints** of the profile are placed in the middle of a profile structure, not at the upper or lower edge. They occur on impulse movements and are used as support/resistance zones, which the price can test in the near future. The singles line indicates where the singles begin to form \(in cases when there are several single prints\).

**TPO letters** — basic element of the TPO chart, where each letter corresponds to a specific time \("**Build From**"\).

## Main Controls of TPO Chart

There are three main controls on the top toolbar of TPO chart panel:

* **Aggregation**
* **Style**
* **Volume Analysis**

### Aggregation of TPO Profile Chart

The base element of the TPO chart is letters that are used to build the market profile structure. Each letter initially represents a half-hour period. Quantower offers to specify in the aggregation settings any values on the basis of which the profile will be built. For example, a daily profile of 30-minute bars is considered as a “standard”. But you can set a lower value of “**Build From**” and the profile will be more granular. Conversely, set the value higher and the shape of the profile will be smoother.

![](../.gitbook/assets/custom-period.gif)

![TPO Profile can be build with any custom period and base](../.gitbook/assets/screenshot_11.png)

* **Build From \(Minute, Hour, Day\)** — this parameter determines the length of time for building each letter \(for A, B, C etc.\).
* **Profile Aggregation** — defines the range for each TPO profile. The standard range is 1 day, but there are several base ranges for building each profile — **Minute, Hour, Day**. For example, a 1 day range will start at the beginning of the trading day and finish at the end of the current trading day \(defined in the trading hours or by custom session\).
* **History Range** — determines the depth of history for building TPO profiles. At a high depth of history, volume profiles can be built for a long time, because they use tick data.
* **Custom Step \(Ticks\)** — this parameter defines the height and number of letters in the profile. _If enabled_, the letter height will correspond to the number of ticks which is set in the parameter. _If disabled_, the height and number of letters will be selected automatically using a smart algorithm. As a result, the chart will look the most optimal for analysis.



