---
title: 'name'
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
    value: String
    href: /apis/user_timing/PerformanceMark
standardization_status: 'W3C Recommendation'
summary: 'Returns the mark''s name.'
tags:
  - API_Object_Properties
  - API
  - User_Timing
uri: 'apis/user timing/PerformanceMark/name'

---
## Summary

Returns the mark's name.

Property of [apis/user\_timing/PerformanceMark](/apis/user_timing/PerformanceMark)[apis/user\_timing/PerformanceMark](/apis/user_timing/PerformanceMark)

## Syntax

``` js
var result = element.name;
element.name = value;
```

## Return Value

Returns an object of type StringString

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
