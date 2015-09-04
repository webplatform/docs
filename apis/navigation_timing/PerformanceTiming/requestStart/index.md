---
title: requestStart
tags:
  0: API
  1: Object
  2: Properties
  4: Navigation
  5: Timing
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Returns the time immediately before the user agent starts requesting the current document from the server, or from relevant application caches or from local resources. If the transport connection fails after a request is sent and the user agent reopens a connection and resends the request, returns the corresponding values of the new request.'
uri: 'apis/navigation timing/PerformanceTiming/requestStart'

---
# requestStart

## Summary

Returns the time immediately before the user agent starts requesting the current document from the server, or from relevant application caches or from local resources. If the transport connection fails after a request is sent and the user agent reopens a connection and resends the request, returns the corresponding values of the new request.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/navigation timing/PerformanceTiming](/apis/navigation_timing/PerformanceTiming)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = PerformanceTiming.requestStart;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned long</span></span>

## Examples

``` {.js}
var perftime = performance.timing;
document.write("requestStart: " + perftime.requestStart + "<br />");
```

## Notes

The PerformanceTiming interface does not include an attribute to represent the completion of sending the request, e.g., requestEnd.

-   Completion of sending the request from the user agent does not always indicate the corresponding completion time in the network transport, which brings most of the benefit of having such an attribute.
-   Some user agents have high cost to determine the actual completion time of sending the request due to the HTTP layer encapsulation.

## Related specifications

Specification
:   Status
[Navigation Timing 2](http://www.w3.org/TR/navigation-timing-2/)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

