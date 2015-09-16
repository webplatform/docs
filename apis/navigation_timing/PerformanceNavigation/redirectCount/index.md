---
title: 'redirectCount'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/navigation_timing/PerformanceNavigation
    href: /apis/navigation_timing/PerformanceNavigation
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned short'
    href: /apis/navigation_timing/PerformanceNavigation
standardization_status: 'W3C Working Draft'
summary: 'Returns the number of redirects since the last non-redirect navigation under the current browsing context. If there is no redirect or there is any redirect that is not from the same origin as the destination document, returns zero.'
tags:
  0: API
  1: Object
  2: Properties
  4: Navigation
  5: Timing
uri: 'apis/navigation timing/PerformanceNavigation/redirectCount'

---
## Summary

Returns the number of redirects since the last non-redirect navigation under the current browsing context. If there is no redirect or there is any redirect that is not from the same origin as the destination document, returns zero.

Property of [apis/navigation\_timing/PerformanceNavigation](/apis/navigation_timing/PerformanceNavigation)[apis/navigation\_timing/PerformanceNavigation](/apis/navigation_timing/PerformanceNavigation)

## Syntax

**Note**: This property is read-only.

``` js
var result = PerformanceNavigation.redirectCount;
```

## Return Value

Returns an object of type unsigned shortunsigned short

## Examples

``` js
var perfnavred = performance.navigation.redirectCount;
alert(perfnavred);
```

## Related specifications

[W3C Navigation Timing Specification 2](http://www.w3.org/TR/navigation-timing-2/)
:   W3C Working Draft
