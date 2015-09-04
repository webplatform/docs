---
title: responseEnd
tags:
  0: API
  1: Object
  2: Properties
  4: Navigation
  5: Timing
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Returns the time immediately after the user agent receives the last byte of the current document from the server, relevant application caches or from local resources, or immediately before the transport connection is closed, whichever comes first.'
uri: 'apis/navigation timing/PerformanceTiming/responseEnd'

---
# responseEnd

## Summary

Returns the time immediately after the user agent receives the last byte of the current document from the server, relevant application caches or from local resources, or immediately before the transport connection is closed, whichever comes first.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/navigation timing/PerformanceTiming](/apis/navigation_timing/PerformanceTiming)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = PerformanceTiming.responseEnd;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned long</span></span>

## Examples

``` {.js}
var perftime = performance.timing;
document.write("responseEnd: " + perftime.responseEnd + "<br />");
```

## Related specifications

Specification
:   Status
[Navigation Timing 2](http://www.w3.org/TR/navigation-timing-2/)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

