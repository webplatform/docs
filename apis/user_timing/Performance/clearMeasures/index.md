---
title: clearMeasures
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/user_timing/Performance
    href: /apis/user_timing/Performance
standardization_status: 'W3C Recommendation'
summary: 'Removes all DOMHighResTimeStamp durations for the given measure name, or removes all measures and their associated DOMHighResTimeStamp durations.'
tags:
  0: API
  1: Object
  2: Methods
  4: User
  5: Timing
uri: 'apis/user timing/Performance/clearMeasures'

---
## <span>Summary</span>

Removes all DOMHighResTimeStamp durations for the given measure name, or removes all measures and their associated DOMHighResTimeStamp durations.

Method of [apis/user\_timing/Performance](/apis/user_timing/Performance)[apis/user\_timing/Performance](/apis/user_timing/Performance)

## <span>Syntax</span>

``` js
 object.clearMeasures(measureName);
```

## <span>Parameters</span>

### <span>measureName</span>

 Data-type
:   any

(Optional)

Name of the measures(s) to be cleared.

## <span>Return Value</span>

No return value

## <span>Examples</span>

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

## <span>Notes</span>

If a value for the *measureName* parameter is specified, only measures with that name are removed. If there are no measures with the specified name, this method does nothing.

## <span>Related specifications</span>

[W3C User Timing Specification](http://www.w3.org/TR/user-timing/)
:   W3C Recommendation
