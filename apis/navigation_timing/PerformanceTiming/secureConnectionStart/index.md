---
title: secureConnectionStart
tags:
  0: API
  1: Object
  2: Properties
  4: Navigation
  5: Timing
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Returns the time immediately before the user agent starts the handshake process to secure the current connection, if the scheme of the current page is HTTPS. If HTTPS is not used, returns zero.'
uri: 'apis/navigation timing/PerformanceTiming/secureConnectionStart'

---
# secureConnectionStart

## Summary

Returns the time immediately before the user agent starts the handshake process to secure the current connection, if the scheme of the current page is HTTPS. If HTTPS is not used, returns zero.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/navigation timing/PerformanceTiming](/apis/navigation_timing/PerformanceTiming)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = PerformanceTiming.secureConnectionStart;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned long</span></span>

## Examples

``` {.js}
var perftime = performance.timing;
document.write("secureConnectionStart: " + perftime.secureConnectionStart + "<br />");
```

## Notes

This attribute is optional. User agents that don't have this attribute available must set it as undefined.

## Related specifications

Specification
:   Status
[Navigation Timing 2](http://www.w3.org/TR/navigation-timing-2/)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

