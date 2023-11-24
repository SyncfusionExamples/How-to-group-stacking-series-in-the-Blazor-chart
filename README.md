# How-to-group-stacking-series-in-the-Blazor-chart

This article Explains how to group the stacking group in the Blazor Chart.

**Grouping stacking series**

Stacking series are rendered in such a way that all the series are stacked. This is not desired when there are many stacking series in the chart. In such cases, the Blazor chart provides options to group the stacking series by using [StackingGroup](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.ChartSeries.html#Syncfusion_Blazor_Charts_ChartSeries_StackingGroup) property.

For example, consider four stacking column series grouped into two; Group1 and Group2 by using the [StackingGroup](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.ChartSeries.html#Syncfusion_Blazor_Charts_ChartSeries_StackingGroup) property. Then, chart is rendered in two stacking columns at a point; one for Group1 and the other for Group2.

The Following code example illustrates this.

**C#**

```cshtml

@using Syncfusion.Blazor.Charts

<SfChart>

    <ChartPrimaryXAxis ValueType="Syncfusion.Blazor.Charts.ValueType.Category"></ChartPrimaryXAxis>

    <ChartSeriesCollection>
        <ChartSeries DataSource="@DataSource" StackingGroup="Group1" XName="X" YName="YValue" Type="ChartSeriesType.StackingColumn">
        </ChartSeries>
        <ChartSeries DataSource="@DataSource" StackingGroup="Group1" XName="X" YName="YValue1" Type="ChartSeriesType.StackingColumn">
        </ChartSeries>
        <ChartSeries DataSource="@DataSource" StackingGroup="Group2" XName="X" YName="YValue2" Type="ChartSeriesType.StackingColumn">
        </ChartSeries>
        <ChartSeries DataSource="@DataSource" StackingGroup="Group2" XName="X" YName="YValue3" Type="ChartSeriesType.StackingColumn">
        </ChartSeries>
    </ChartSeriesCollection>

</SfChart>

@code {

    public class ChartData
    {
        public string X { get; set; }
        public double YValue { get; set; }
        public double YValue1 { get; set; }
        public double YValue2 { get; set; }
        public double YValue3 { get; set; }
    }

    public List<ChartData> DataSource = new List<ChartData>
    {
        new ChartData { X= "USA", YValue= 46, YValue1=56, YValue2=26,YValue3=50},
        new ChartData { X= "GBR", YValue= 27, YValue1=17, YValue2=37,YValue3=20},
        new ChartData { X= "CHN", YValue= 26, YValue1=36, YValue2=56,YValue3=26},
        new ChartData { X= "UK", YValue= 56,  YValue1=16, YValue2=36,YValue3=16},
        new ChartData { X= "AUS", YValue= 12, YValue1=46, YValue2=26,YValue3=20},
        new ChartData { X= "IND", YValue= 26, YValue1=16, YValue2=76,YValue3=25},
        new ChartData { X= "DEN", YValue= 26, YValue1=12, YValue2=42,YValue3=20},
        new ChartData { X= "MEX", YValue= 34, YValue1=32, YValue2=82,YValue3=35},
    };
}

```

The following screenshot illustrate the output of the above code snippet.

**Output:**

Figure 1:- Before Grouping

![](/before-grouping.png)

Figure 2:- After Grouping

![](/stacking-group.png)

**Conclusion**

I hope you enjoyed learning how to group the Stacking series in Blazor Chart Component.

You can refer to our [Blazor Chart feature tour](https://www.syncfusion.com/blazor-components/blazor-charts) page to know about its other groundbreaking feature representations and [documentation](https://blazor.syncfusion.com/documentation/chart/getting-started), and how to quickly get started for configuration specifications. You can also explore our [Blazor Chart example](https://blazor.syncfusion.com/demos/chart/line?theme=bootstrap5) to understand how to create and manipulate data.

For current customers, you can check out our components from the [License and Downloads](https://www.syncfusion.com/sales/teamlicense) page. If you are new to Syncfusion, you can try our 30-day [free trial](https://www.syncfusion.com/downloads/blazor) to check out our other controls.

If you have any queries or require clarifications, please let us know in the comments section below. You can also contact us through our [support forums](https://www.syncfusion.com/forums), [support portal](https://support.syncfusion.com/create), or [feedback portal](https://www.syncfusion.com/feedback/blazor-components?control=charts). We are always happy to assist you!

