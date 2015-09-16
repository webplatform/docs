---
title: setResourceTimingBufferSize
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/resource_timing/Performance
    href: /apis/resource_timing/Performance
standardization_status: 'W3C Working Draft'
summary: 'Sets the maximum number of PerformanceResourceTiming resources that may be stored in the buffer to the value of the maxSize parameter.'
tags:
  0: API
  1: Object
  2: Methods
  4: Resource
  5: Timing
uri: 'apis/resource timing/Performance/setResourceTimingBufferSize'

---
## Summary

Sets the maximum number of PerformanceResourceTiming resources that may be stored in the buffer to the value of the maxSize parameter.

Method of [apis/resource\_timing/Performance](/apis/resource_timing/Performance)[apis/resource\_timing/Performance](/apis/resource_timing/Performance)

## Syntax

``` js
 .setResourceTimingBufferSize(maxSize);
```

## Parameters

### maxSize

 Data-type
:   unsigned long

 The maximum number of PerformanceResourceTiming resources that will be stored in the buffer.

## Return Value

No return value

## Examples

This example uses clearResourceTimings and setResourceTimingBufferSize to set an initial buffer size. It then uses onresourcetimingbufferfull to detect when the buffer is full, and executes a function that uses clearResourceTimings to clear the buffer.

``` js
performance.clearResourceTimings();
setResourceTimingBufferSize(100);

function buffFull() {
  performance.clearResourceTimings();
  };

performance.onresourcetimingbufferfull = buffFull;
```

## Notes

The **setResourceTimingBufferSize** does not take effect until the **clearResourceTimings** method is called.

## Related specifications

[W3C Resource Timing Specification](http://www.w3.org/TR/resource-timing/)
:   W3C Working Draft
