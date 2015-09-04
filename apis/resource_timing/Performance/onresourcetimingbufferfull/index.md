---
title: onresourcetimingbufferfull
tags:
  0: API
  1: Object
  2: Properties
  4: Resource
  5: Timing
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'This callback is triggered when the buffer used to store the list of PerformanceResourceTiming is full.'
uri: 'apis/resource timing/Performance/onresourcetimingbufferfull'

---
# onresourcetimingbufferfull

## Summary

This callback is triggered when the buffer used to store the list of PerformanceResourceTiming is full.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/resource\_timing/Performance](/apis/resource_timing/Performance)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.onresourcetimingbufferfull;
```

## Examples

This example uses clearResourceTimings and setResourceTimingBufferSize to set an initial buffer size. It then uses onresourcetimingbufferfull to detect when the buffer is full, and executes a function that uses clearResourceTimings to clear the buffer.

``` {.js}
performance.clearResourceTimings();
setResourceTimingBufferSize(100);

function buffFull() {
  performance.clearResourceTimings();
  };

performance.onresourcetimingbufferfull = buffFull;
```

## Related specifications

Specification
:   Status
[W3C Resource Timing Specification](http://www.w3.org/TR/resource-timing/)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

