---
title: unloadEventStart
tags:
  0: API
  1: Object
  2: Properties
  4: Navigation
  5: Timing
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Returns the time immediately before the user agent starts the unload event of the previous document. If there is no previous document or the previous document has a different origin than the current document, returns zero.'
uri: 'apis/navigation timing/PerformanceTiming/unloadEventStart'

---
# unloadEventStart

## Summary

Returns the time immediately before the user agent starts the unload event of the previous document. If there is no previous document or the previous document has a different origin than the current document, returns zero.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/navigation timing/PerformanceTiming](/apis/navigation_timing/PerformanceTiming)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = PerformanceTiming.unloadEventStart;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned long</span></span>

## Examples

``` {.js}
var perftime = performance.timing;
document.write("unloadEventStart: " + perftime.unloadEventStart + "<br />");
```

## Notes

The value reported represents the number of milliseconds between the recorded time and midnight January 1, 1970 (UTC).

## Related specifications

Specification
:   Status
[Navigation Timing 2](http://www.w3.org/TR/navigation-timing-2/)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

