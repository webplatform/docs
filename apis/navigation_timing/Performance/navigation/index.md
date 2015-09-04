---
title: navigation
tags:
  0: API
  1: Object
  2: Properties
  4: Navigation
  5: Timing
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Represents the navigation information related to the browsing context. This attribute is defined by the PerformanceNavigation interface.'
uri: 'apis/navigation timing/Performance/navigation'

---
# navigation

## Summary

Represents the navigation information related to the browsing context. This attribute is defined by the PerformanceNavigation interface.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/navigation\_timing/Performance](/apis/navigation_timing/Performance)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = Performance.navigation;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Object</span></span>

## Examples

``` {.js}
var perfnav = performance.navigation;
alert(perfnav); // "[object PerformanceNavigation]"
```

## Notes

Use the **performance** property of the **window** object to get the host for this object.

## Related specifications

Specification
:   Status
[W3c Navigation Timing Specification](http://www.w3.org/TR/navigation-timing/)
:   W3C Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

