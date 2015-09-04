---
title: mark
tags:
  0: API
  1: Object
  2: Methods
  4: User
  5: Timing
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Stores a timestamp with the associated name (a "mark").'
uri: 'apis/user timing/Performance/mark'

---
# mark

## Summary

Stores a timestamp with the associated name (a "mark").

*Method of [apis/user\_timing/Performance](/apis/user_timing/Performance)*

## Syntax

``` {.js}
 object.mark(markName);
```

## Parameters

### markName

 Data-typeÂ
:   any

 Name associated with the performance mark.

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

Names for custom performance marks cannot duplicate the names of built-in performance marks.

When mark names are reused, the previous timing values are replaced by the later timing values.

## Related specifications

Specification
:   Status
[W3C User Timing Specification](http://www.w3.org/TR/user-timing/)
:   W3C Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

