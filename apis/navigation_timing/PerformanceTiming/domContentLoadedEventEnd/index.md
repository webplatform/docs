---
title: 'domContentLoadedEventEnd'
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
summary: 'Returns the time immediately after the document''s DOMContentLoaded event completes.'
tags:
  - API_Object_Properties
  - API
  - Navigation_Timing
uri: 'apis/navigation timing/PerformanceTiming/domContentLoadedEventEnd'

---
## Summary

Returns the time immediately after the document's DOMContentLoaded event completes.

Property of [apis/navigation\_timing/PerformanceTiming](/apis/navigation_timing/PerformanceTiming)[apis/navigation\_timing/PerformanceTiming](/apis/navigation_timing/PerformanceTiming)

## Syntax

**Note**: This property is read-only.

``` js
var result = PerformanceTiming.domContentLoadedEventEnd;
```

## Return Value

Returns an object of type unsigned longunsigned long

## Examples

``` js
var perftime = performance.timing;
document.write("domContentLoadedEventEnd: " + perftime.domContentLoadedEventEnd + "<br />");
```

## Notes

The value represents the number of milliseconds between midnight January 1, 1970 (UTC) and the recorded ending time.

## Related specifications

[W3C Navigation Timing Specification 2](http://www.w3.org/TR/navigation-timing-2/)
:   W3C Working Draft
