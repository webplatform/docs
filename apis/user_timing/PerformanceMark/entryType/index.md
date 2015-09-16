---
title: 'entryType'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
notes:
  - 'Needs example'
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
summary: 'Returns the DOMString &quot;mark&quot;.'
tags:
  0: API
  1: Object
  2: Properties
  4: User
  5: Timing
uri: 'apis/user timing/PerformanceMark/entryType'

---
## Summary

Returns the DOMString &quot;mark&quot;.

Property of [apis/user\_timing/PerformanceMark](/apis/user_timing/PerformanceMark)[apis/user\_timing/PerformanceMark](/apis/user_timing/PerformanceMark)

## Syntax

``` js
var result = element.entryType;
element.entryType = value;
```

## Return Value

Returns an object of type

DOMString

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
