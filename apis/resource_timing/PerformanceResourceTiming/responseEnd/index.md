---
title: responseEnd
tags:
  0: API
  1: Object
  2: Properties
  4: Resource
  5: Timing
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Returns the time immediately after the user agent finishes receiving the last byte of the resource from from relevant application caches or from local resources.'
uri: 'apis/resource timing/PerformanceResourceTiming/responseEnd'

---
# responseEnd

## Summary

Returns the time immediately after the user agent finishes receiving the last byte of the resource from from relevant application caches or from local resources.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/resource\_timing/PerformanceResourceTiming](/apis/resource_timing/PerformanceResourceTiming)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.responseEnd;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value"></span></span>

DOMHighResTimeStamp

## Examples

This example assumes an HTML page containing a resource such as \<img src="[https://www.webplatform.org/logo/logo-with-text.png](https://www.webplatform.org/logo/logo-with-text.png)" /\>

``` {.js}
var resources = window.performance.getEntriesByType('resource');
alert("responseEnd: " + resources[0].responseEnd);
```

## Notes

The value reported by the **responseEnd** property represents the number of milliseconds between the recorded time and midnight January 1, 1970 (UTC).

## Related specifications

Specification
:   Status
[W3C Resource Timing Specification](http://www.w3.org/TR/resource-timing/)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

