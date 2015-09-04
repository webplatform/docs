---
title: domLoading
tags:
  0: API
  1: Object
  2: Properties
  4: Navigation
  5: Timing
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Returns the time immediately before the user agent sets the current document readiness to "loading".'
uri: 'apis/navigation timing/PerformanceTiming/domLoading'

---
# domLoading

## Summary

Returns the time immediately before the user agent sets the current document readiness to "loading".

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/navigation\_timing/PerformanceTiming](/apis/navigation_timing/PerformanceTiming)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = PerformanceTiming.domLoading;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned long</span></span>

## Examples

``` {.js}
var perftime = performance.timing;
document.write("domLoading: " + perftime.domLoading + "<br />");
```

## Notes

The value of the **domLoading** property is controlled by the **document** object associated with the **window** object. The value of the **domLoading** property is updated when the **readyState** property is set to `loading`. If the document cannot be loaded, the value of the **domLoading** property is available after the **onload** event has finished executing. The value reported represents the number of milliseconds between the recorded time and midnight January 1, 1970 (UTC).

## Related specifications

Specification
:   Status
[W3C Navigation Timing Specification 2](http://www.w3.org/TR/navigation-timing-2/)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

