---
title: measure
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/user_timing/Performance
    href: /apis/user_timing/Performance
standardization_status: 'W3C Recommendation'
summary: 'Stores the DOMHighResTimeStamp duration between two marks along with the associated name (a &quot;measure&quot;).'
tags:
  0: API
  1: Object
  2: Methods
  4: User
  5: Timing
uri: 'apis/user timing/Performance/measure'

---
## <span>Summary</span>

Stores the DOMHighResTimeStamp duration between two marks along with the associated name (a &quot;measure&quot;).

Method of [apis/user\_timing/Performance](/apis/user_timing/Performance)[apis/user\_timing/Performance](/apis/user_timing/Performance)

## <span>Syntax</span>

``` js
 object.measure(name, startMark, endMark);
```

## <span>Parameters</span>

### <span>name</span>

 Data-type
:   any

 Name associated with the performance measure.

### <span>startMark</span>

 Data-type
:   any

(Optional)

Name of the start performance mark.

### <span>endMark</span>

 Data-type
:   any

(Optional)

Name of the end performance mark.

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

-   If neither the startMark nor the endMark argument is specified, measure() will store the duration as a DOMHighResTimeStamp from navigationStart to the current time.
-   If the startMark argument is specified, but the endMark argument is not specified, measure() will store the duration as a DOMHighResTimeStamp from the most recent occurrence of the start mark to the current time.
-   If both the startMark and endMark arguments are specified, measure() will store the duration as a DOMHighResTimeStamp from the most recent occurrence of the start mark to the most recent occurrence of the end mark.

## <span>Related specifications</span>

[W3C User Timing Specification](http://www.w3.org/TR/user-timing/)
:   W3C Recommendation
