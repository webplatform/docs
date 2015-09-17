---
title: 'unloadEventEnd'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/navigation_timing/PerformanceTiming
    href: /apis/navigation_timing/PerformanceTiming
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned long'
    href: /apis/navigation_timing/PerformanceTiming
standardization_status: 'W3C Working Draft'
summary: 'Returns the time immediately after the user agent finishes the unload event of the previous document. If there is no previous document or the previous document has a different origin than the current document or the unload is not yet completed, returns zero.'
tags:
  - API_Object_Properties
  - API
  - Navigation_Timing
uri: 'apis/navigation timing/PerformanceTiming/unloadEventEnd'

---
## Summary

Returns the time immediately after the user agent finishes the unload event of the previous document. If there is no previous document or the previous document has a different origin than the current document or the unload is not yet completed, returns zero.

Property of [apis/navigation\_timing/PerformanceTiming](/apis/navigation_timing/PerformanceTiming)[apis/navigation\_timing/PerformanceTiming](/apis/navigation_timing/PerformanceTiming)

## Syntax

**Note**: This property is read-only.

``` js
var result = PerformanceTiming.unloadEventEnd;
```

## Return Value

Returns an object of type unsigned longunsigned long

## Examples

``` js
var perftime = performance.timing;
document.write("unloadEventEnd: " + perftime.unloadEventEnd + "<br />");
```

## Notes

The value reported represents the number of milliseconds between the recorded time and midnight January 1, 1970 (UTC).

## Related specifications

[Navigation Timing 2](http://www.w3.org/TR/navigation-timing-2/)
:   W3C Working Draft
