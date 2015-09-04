---
title: redirectCount
tags:
  0: API
  1: Object
  2: Properties
  4: Navigation
  5: Timing
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Returns the number of redirects since the last non-redirect navigation under the current browsing context. If there is no redirect or there is any redirect that is not from the same origin as the destination document, returns zero.'
uri: 'apis/navigation timing/PerformanceNavigation/redirectCount'

---
# redirectCount

## Summary

Returns the number of redirects since the last non-redirect navigation under the current browsing context. If there is no redirect or there is any redirect that is not from the same origin as the destination document, returns zero.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/navigation\_timing/PerformanceNavigation](/apis/navigation_timing/PerformanceNavigation)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = PerformanceNavigation.redirectCount;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned short</span></span>

## Examples

``` {.js}
var perfnavred = performance.navigation.redirectCount;
alert(perfnavred);
```

## Related specifications

Specification
:   Status
[W3C Navigation Timing Specification 2](http://www.w3.org/TR/navigation-timing-2/)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

