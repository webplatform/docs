---
title: requestStart
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/resource_timing/PerformanceResourceTiming
    href: /apis/resource_timing/PerformanceResourceTiming
  return:
    predicate: 'Returns an object of type '
    value: ''
    href: /apis/resource_timing/PerformanceResourceTiming
standardization_status: 'W3C Working Draft'
summary: 'Returns the time immediately before the user agent starts requesting the resource from the server, or from relevant application caches or from local resources.'
tags:
  0: API
  1: Object
  2: Properties
  4: Resource
  5: Timing
uri: 'apis/resource timing/PerformanceResourceTiming/requestStart'

---
## <span>Summary</span>

Returns the time immediately before the user agent starts requesting the resource from the server, or from relevant application caches or from local resources.

Property of [apis/resource\_timing/PerformanceResourceTiming](/apis/resource_timing/PerformanceResourceTiming)[apis/resource\_timing/PerformanceResourceTiming](/apis/resource_timing/PerformanceResourceTiming)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = element.requestStart;
```

## <span>Return Value</span>

Returns an object of type<span></span>

DOMHighResTimeStamp

## <span>Examples</span>

This example assumes an HTML page containing a resource such as \<img src="<https://www.webplatform.org/logo/logo-with-text.png>" /\>

``` js
var resources = window.performance.getEntriesByType('resource');
alert("requestStart: " + resources[0].requestStart);
```

## <span>Notes</span>

The value reported by the **requestStart** property represents the number of milliseconds between the recorded time and midnight January 1, 1970 (UTC).

## <span>Related specifications</span>

[W3C Resource Timing Specification](http://www.w3.org/TR/resource-timing/)
:   W3C Working Draft
