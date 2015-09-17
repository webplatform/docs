---
title: 'requestStart'
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
  - API_Object_Properties
  - API
  - Resource_Timing
uri: 'apis/resource timing/PerformanceResourceTiming/requestStart'

---
## Summary

Returns the time immediately before the user agent starts requesting the resource from the server, or from relevant application caches or from local resources.

Property of [apis/resource\_timing/PerformanceResourceTiming](/apis/resource_timing/PerformanceResourceTiming)[apis/resource\_timing/PerformanceResourceTiming](/apis/resource_timing/PerformanceResourceTiming)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.requestStart;
```

## Return Value

Returns an object of type

DOMHighResTimeStamp

## Examples

This example assumes an HTML page containing a resource such as \<img src="<https://www.webplatform.org/logo/logo-with-text.png>" /\>

``` js
var resources = window.performance.getEntriesByType('resource');
alert("requestStart: " + resources[0].requestStart);
```

## Notes

The value reported by the **requestStart** property represents the number of milliseconds between the recorded time and midnight January 1, 1970 (UTC).

## Related specifications

[W3C Resource Timing Specification](http://www.w3.org/TR/resource-timing/)
:   W3C Working Draft
