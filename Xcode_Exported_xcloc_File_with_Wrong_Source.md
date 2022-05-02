# Xcode Exported xcloc File with Wrong Source
## Issue
For swift code:
```swift
private func getSubTitle() -> String {
    let points = barChartData.dataSets.dataPoints.filter { $0.value != 0 }
    let firstPoint = points.first!
    let lastPoint = points.last!
    let interval = Int(lastPoint.date!.timeIntervalSince(firstPoint.date!))
    
    let hour = 60 * 60
    let minute = 60
    
    if interval >= hour {
        let hourInt = interval / hour
        var remain = interval - hour * hourInt
        let minuteInt = remain / minute
        remain = remain - minute * minuteInt
        
        return String.localizedStringWithFormat(NSLocalizedString("%02dh%02m%02s", comment: ""), hourInt, minuteInt, remain)
    } else if interval >= minute {
        let minuteInt = interval / minute
        let remain = interval - minute * minuteInt
        return String.localizedStringWithFormat(NSLocalizedString("%02dm%02ds", comment: ""), minuteInt, remain)
    }
    
    return String.localizedStringWithFormat(NSLocalizedString("%02ds", comment: ""), interval)
}
```

There is NSLocalizedString("%02dh%02m%02s", comment: "") to translate. When exporting by Xcode, the result was 

```xml
<trans-unit id="%02dh%02m%02s" xml:space="preserve">
    <source>%1$dh%2$m%3$s</source>
    <target></target>
    <note>No comment provided by engineer.</note>
</trans-unit>
```

The source was changed and not correct. 

Xcode   13.3.1 (13E500a)

## Workaround
Ignore the source and translate base on the id. That means using "%02dh%02m%02s" in target instead of "%1$dh%2$m%3$s" to translate.