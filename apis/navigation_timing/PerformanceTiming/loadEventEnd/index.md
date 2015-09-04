---
title: loadEventEnd
tags:
  0: API
  1: Object
  2: Properties
  4: Navigation
  5: Timing
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Returns the time when the load event of the current document is completed, or returns zero when the load event is not fired or is not completed.'
uri: 'apis/navigation timing/PerformanceTiming/loadEventEnd'

---
# loadEventEnd

## Summary

Returns the time when the load event of the current document is completed, or returns zero when the load event is not fired or is not completed.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/navigation\_timing/PerformanceTiming](/apis/navigation_timing/PerformanceTiming)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = PerformanceTiming.loadEventEnd;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned long</span></span>

## Examples

``` {.js}
var perftime = performance.timing;
document.write("loadEventEnd: " + perftime.loadEventEnd + "<br />");
```

## Notes

The value reported represents the number of milliseconds between the recorded time and midnight January 1, 1970 (UTC).

## Related specifications

Specification
:   Status
[W3C Navigation Timing 2](http://www.w3.org/TR/navigation-timing-2/)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

