---
title: timing
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
summary: 'Represents the timing information related to the browsing contexts since the last non-redirect navigation. This attribute is defined by the PerformanceTiming interface.'
tags:
  0: API
  1: Object
  2: Properties
  4: Navigation
  5: Timing
uri: 'apis/navigation timing/Performance/timing'

---
## <span>Summary</span>

Represents the timing information related to the browsing contexts since the last non-redirect navigation. This attribute is defined by the PerformanceTiming interface.

Property of [apis/navigation\_timing/Performance](/apis/navigation_timing/Performance)[apis/navigation\_timing/Performance](/apis/navigation_timing/Performance)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = Performance.timing;
```

## <span>Return Value</span>

Returns an object of type ObjectObject

## <span>Examples</span>

``` js
var perftim = performance.timing;
alert(perftim); // "[object PerformanceTiming]"
```

## <span>Notes</span>

Use the **performance** property of the **window** object to get the host for this object.

## <span>Related specifications</span>

[W3C Navigation Timing Specification](http://www.w3.org/TR/navigation-timing/)
:   W3C Recommendation
