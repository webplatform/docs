---
title: 'duration'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/user_timing/PerformanceMark
    href: /apis/user_timing/PerformanceMark
  return:
    predicate: 'Returns an object of type '
    value: ''
    href: /apis/user_timing/PerformanceMark
standardization_status: 'W3C Recommendation'
summary: 'Returns a DOMHighResTimeStamp value. For marks, the value is always 0 (zero).'
tags:
  0: API
  1: Object
  2: Properties
  4: User
  5: Timing
uri: 'apis/user timing/PerformanceMark/duration'

---
## Summary

Returns a DOMHighResTimeStamp value. For marks, the value is always 0 (zero).

Property of [apis/user\_timing/PerformanceMark](/apis/user_timing/PerformanceMark)[apis/user\_timing/PerformanceMark](/apis/user_timing/PerformanceMark)

## Syntax

``` js
var result = element.duration;
element.duration = value;
```

## Return Value

Returns an object of type

DOMHighResTimeStamp

## Examples

``` js
// set begin mark
performance.mark("startMark");
// execute a function to be measured
someFunction();
// set end mark
performance.mark("stopMark");

// save the timing information
performance.measure("functionTime", "startMark", "stopMark");
// display the first mark's data
var marks = performance.getEntriesByType("mark");
alert("Mark name: " + marks[0].name + "\n" +
      "Mark type: " + marks[0].entryType + "\n" +
      "Mark start: " + marks[0].startTime + "\n" +
      "Mark duration: " + marks[0].duration);

// clear the measure "functionTime"
performance.clearMeasures("functionTime");
// clear all marks
performance.clearMarks();
```

## Related specifications

[W3C User Timing Specification](http://www.w3.org/TR/user-timing/)
:   W3C Recommendation
