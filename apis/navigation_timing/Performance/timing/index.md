---
title: timing
tags:
  0: API
  1: Object
  2: Properties
  4: Navigation
  5: Timing
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Represents the timing information related to the browsing contexts since the last non-redirect navigation. This attribute is defined by the PerformanceTiming interface.'
uri: 'apis/navigation timing/Performance/timing'

---
# timing

## Summary

Represents the timing information related to the browsing contexts since the last non-redirect navigation. This attribute is defined by the PerformanceTiming interface.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/navigation\_timing/Performance](/apis/navigation_timing/Performance)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = Performance.timing;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Object</span></span>

## Examples

``` {.js}
var perftim = performance.timing;
alert(perftim); // "[object PerformanceTiming]"
```

## Notes

Use the **performance** property of the **window** object to get the host for this object.

## Related specifications

Specification
:   Status
[W3C Navigation Timing Specification](http://www.w3.org/TR/navigation-timing/)
:   W3C Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

