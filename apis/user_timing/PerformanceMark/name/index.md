---
title: name
tags:
  0: API
  1: Object
  2: Properties
  4: User
  5: Timing
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Returns the mark''s name.'
uri: 'apis/user timing/PerformanceMark/name'

---
# name

## Summary

Returns the mark's name.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/user\_timing/PerformanceMark](/apis/user_timing/PerformanceMark)</span></span>

## Syntax

``` {.js}
var result = element.name;
element.name = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

## Examples

``` {.js}
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

Specification
:   Status
[W3C User Timing Specification](http://www.w3.org/TR/user-timing/)
:   W3C Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

