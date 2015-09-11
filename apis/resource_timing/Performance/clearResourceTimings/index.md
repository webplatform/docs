---
title: clearResourceTimings
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/resource_timing/Performance
    href: /apis/resource_timing/Performance
standardization_status: 'W3C Working Draft'
summary: 'Clears the buffer used to store the current list of PerformanceResourceTiming resources.'
tags:
  0: API
  1: Object
  2: Methods
  4: Resource
  5: Timing
uri: 'apis/resource timing/Performance/clearResourceTimings'

---
## <span>Summary</span>

Clears the buffer used to store the current list of PerformanceResourceTiming resources.

Method of [apis/resource\_timing/Performance](/apis/resource_timing/Performance)[apis/resource\_timing/Performance](/apis/resource_timing/Performance)

## <span>Syntax</span>

``` js
 .clearResourceTimings();
```

## <span>Return Value</span>

No return value

## <span>Examples</span>

This example uses clearResourceTimings and setResourceTimingBufferSize to set an initial buffer size. It then uses onresourcetimingbufferfull to detect when the buffer is full, and executes a function that uses clearResourceTimings to clear the buffer.

``` js
performance.clearResourceTimings();
setResourceTimingBufferSize(100);

function buffFull() {
  performance.clearResourceTimings();
  };

performance.onresourcetimingbufferfull = buffFull;
```

## <span>Related specifications</span>

[W3C Resource Timing Specification](http://www.w3.org/TR/resource-timing/)
:   W3C Working Draft
