---
title: 'domContentLoadedEventStart'
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
summary: 'Returns the time immediately before the user agent fires the DOMContentLoaded event at the Document.'
tags:
  - API_Object_Properties
  - API
  - Navigation_Timing
uri: 'apis/navigation timing/PerformanceTiming/domContentLoadedEventStart'

---
## Summary

Returns the time immediately before the user agent fires the DOMContentLoaded event at the Document.

Property of [apis/navigation\_timing/PerformanceTiming](/apis/navigation_timing/PerformanceTiming)[apis/navigation\_timing/PerformanceTiming](/apis/navigation_timing/PerformanceTiming)

## Syntax

**Note**: This property is read-only.

``` js
var result = PerformanceTiming.domContentLoadedEventStart;
```

## Return Value

Returns an object of type unsigned longunsigned long

## Examples

``` js
var perftime = performance.timing;
document.write("domContentLoadedEventStart: " + perftime.domContentLoadedEventStart + "<br />");
```

## Notes

The value reported represents the number of milliseconds between the recorded time and midnight January 1, 1970 (UTC).

## Related specifications

[W3C Navigation Timing Specification 2](http://www.w3.org/TR/navigation-timing-2/)
:   W3C Working Draft
