---
title: 'navigation'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/navigation_timing/Performance
    href: /apis/navigation_timing/Performance
  return:
    predicate: 'Returns an object of type '
    value: Object
    href: /apis/navigation_timing/Performance
standardization_status: 'W3C Recommendation'
summary: 'Represents the navigation information related to the browsing context. This attribute is defined by the PerformanceNavigation interface.'
tags:
  0: API
  1: Object
  2: Properties
  4: Navigation
  5: Timing
uri: 'apis/navigation timing/Performance/navigation'

---
## Summary

Represents the navigation information related to the browsing context. This attribute is defined by the PerformanceNavigation interface.

Property of [apis/navigation\_timing/Performance](/apis/navigation_timing/Performance)[apis/navigation\_timing/Performance](/apis/navigation_timing/Performance)

## Syntax

**Note**: This property is read-only.

``` js
var result = Performance.navigation;
```

## Return Value

Returns an object of type ObjectObject

## Examples

``` js
var perfnav = performance.navigation;
alert(perfnav); // "[object PerformanceNavigation]"
```

## Notes

Use the **performance** property of the **window** object to get the host for this object.

## Related specifications

[W3c Navigation Timing Specification](http://www.w3.org/TR/navigation-timing/)
:   W3C Recommendation
