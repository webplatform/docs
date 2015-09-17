---
title: 'domLoading'
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
summary: 'Returns the time immediately before the user agent sets the current document readiness to &quot;loading&quot;.'
tags:
  - API_Object_Properties
  - API
  - Navigation_Timing
uri: 'apis/navigation timing/PerformanceTiming/domLoading'

---
## Summary

Returns the time immediately before the user agent sets the current document readiness to &quot;loading&quot;.

Property of [apis/navigation\_timing/PerformanceTiming](/apis/navigation_timing/PerformanceTiming)[apis/navigation\_timing/PerformanceTiming](/apis/navigation_timing/PerformanceTiming)

## Syntax

**Note**: This property is read-only.

``` js
var result = PerformanceTiming.domLoading;
```

## Return Value

Returns an object of type unsigned longunsigned long

## Examples

``` js
var perftime = performance.timing;
document.write("domLoading: " + perftime.domLoading + "<br />");
```

## Notes

The value of the **domLoading** property is controlled by the **document** object associated with the **window** object. The value of the **domLoading** property is updated when the **readyState** property is set to `loading`. If the document cannot be loaded, the value of the **domLoading** property is available after the **onload** event has finished executing. The value reported represents the number of milliseconds between the recorded time and midnight January 1, 1970 (UTC).

## Related specifications

[W3C Navigation Timing Specification 2](http://www.w3.org/TR/navigation-timing-2/)
:   W3C Working Draft
