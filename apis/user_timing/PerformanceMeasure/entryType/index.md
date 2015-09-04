---
title: entryType
tags:
  0: API
  1: Object
  2: Properties
  4: User
  5: Timing
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Returns the DOMString "measure".'
uri: 'apis/user timing/PerformanceMeasure/entryType'

---
# entryType

## Summary

Returns the DOMString "measure".

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/user timing/PerformanceMeasure](/apis/user_timing/PerformanceMeasure)</span></span>

## Syntax

``` {.js}
var result = element.entryType;
element.entryType = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value"></span></span>

DOMString

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
// display the measure's data
var measures = performance.getEntriesByType("measure");
alert("Measure name: " + measures[0].name + "\n" +
      "Measure type: " + measures[0].entryType + "\n" +
      "Measure start: " + measures[0].startTime + "\n" +
      "Measure duration: " + measures[0].duration);

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

