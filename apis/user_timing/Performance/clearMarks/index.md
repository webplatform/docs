---
title: clearMarks
tags:
  0: API
  1: Object
  2: Methods
  4: User
  5: Timing
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Removes all DOMHighResTimeStamp time values for the given mark name, or removes all marks and their associated DOMHighResTimeStamp time values.'
uri: 'apis/user timing/Performance/clearMarks'

---
# clearMarks

## Summary

Removes all DOMHighResTimeStamp time values for the given mark name, or removes all marks and their associated DOMHighResTimeStamp time values.

*Method of [apis/user\_timing/Performance](/apis/user_timing/Performance)*

## Syntax

``` {.js}
 object.clearMarks(markName);
```

## Parameters

### markName

 Data-typeÂ
:   any

*(Optional)*

Name of the mark(s) to be cleared.

## Return Value

No return value

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
// display the measured time
var measures = performance.getEntriesByType("measure");
alert("functionTime: " + measures[0].duration);

// clear the measure "functionTime"
performance.clearMeasures("functionTime");
// clear all marks
performance.clearMarks();
```

## Notes

If a value for the *markName* parameter is specified, only marks with that name are removed. If there are no marks with the specified name, this method does nothing.

## Related specifications

Specification
:   Status
[W3C User Timing Specification](http://www.w3.org/TR/user-timing/)
:   W3C Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

