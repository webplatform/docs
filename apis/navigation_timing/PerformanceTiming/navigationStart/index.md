---
title: navigationStart
tags:
  0: API
  1: Object
  2: Properties
  4: Navigation
  5: Timing
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Returns the time immediately after the user agent finishes prompting to unload the previous document. If there is no previous document, returns the same value as fetchStart.'
uri: 'apis/navigation timing/PerformanceTiming/navigationStart'

---
# navigationStart

## Summary

Returns the time immediately after the user agent finishes prompting to unload the previous document. If there is no previous document, returns the same value as fetchStart.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/navigation timing/PerformanceTiming](/apis/navigation_timing/PerformanceTiming)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = PerformanceTiming.navigationStart;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned long</span></span>

## Examples

``` {.js}
var perftime = performance.timing;
document.write("navigationStart: " + perftime.navigationStart + "<br />");
```

## Notes

The value reported represents the number of milliseconds between the recorded time and midnight January 1, 1970 (UTC).

## Related specifications

Specification
:   Status
[W3C Navigation Timing Specification 2](http://www.w3.org/TR/navigation-timing-2/)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

