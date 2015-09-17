---
title: 'clearMarks'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/user_timing/Performance
    href: /apis/user_timing/Performance
standardization_status: 'W3C Recommendation'
summary: 'Removes all DOMHighResTimeStamp time values for the given mark name, or removes all marks and their associated DOMHighResTimeStamp time values.'
tags:
  - API_Object_Methods
  - API
  - User_Timing
uri: 'apis/user timing/Performance/clearMarks'

---
## Summary

Removes all DOMHighResTimeStamp time values for the given mark name, or removes all marks and their associated DOMHighResTimeStamp time values.

Method of [apis/user\_timing/Performance](/apis/user_timing/Performance)[apis/user\_timing/Performance](/apis/user_timing/Performance)

## Syntax

``` js
 object.clearMarks(markName);
```

## Parameters

### markName

 Data-type
:   any

(Optional)

Name of the mark(s) to be cleared.

## Return Value

No return value

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

[W3C User Timing Specification](http://www.w3.org/TR/user-timing/)
:   W3C Recommendation
