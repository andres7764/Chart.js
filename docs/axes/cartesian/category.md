# Category Cartesian Axis

The category scale will be familiar to those who have used v1.0. Labels are drawn from one of the label arrays included in the chart data. If only `data.labels` is defined, this will be used. If `data.xLabels` is defined and the axis is horizontal, this will be used. Similarly, if `data.yLabels` is defined and the axis is vertical, this property will be used. Using both `xLabels` and `yLabels` together can create a chart that uses strings for both the X and Y axes.

## Tick Configuration Options

The category scale provides the following options for configuring tick marks.

### min
**Type:** String
The minimum item to display. Must be a value in the `labels` array.

In the example below, the x axis would only display "March" through "June".

```javascript
let chart = new Chart(ctx, {
    type: 'line',
    data: {
        datasets: [{
            data: [10, 20, 30, 40, 50, 60]
        }],
        labels: ['January', 'February', 'March', 'April', 'May', 'June'],
    },
    options: {
        scales: {
            xAxes: [{
                ticks: {
                    min: 'March'
                }
            }]
        }
    }
});
```

### max
**Type:** String
The maximum item to display. Must be a value in the `labels` array.