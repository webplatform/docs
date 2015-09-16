---
title: 'domainLookupEnd'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: 'apis/navigation timing/PerformanceTiming'
    href: /apis/navigation_timing/PerformanceTiming
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned long'
    href: /apis/navigation_timing/PerformanceTiming
standardization_status: 'W3C Working Draft'
summary: 'Returns the time immediately after the user agent finishes the domain name lookup for the current document.'
tags:
  0: API
  1: Object
  2: Properties
  4: Navigation
  5: Timing
uri: 'apis/navigation timing/PerformanceTiming/domainLookupEnd'

---
## Summary

Returns the time immediately after the user agent finishes the domain name lookup for the current document.

Property of [apis/navigation timing/PerformanceTiming](/apis/navigation_timing/PerformanceTiming)[apis/navigation timing/PerformanceTiming](/apis/navigation_timing/PerformanceTiming)

## Syntax

**Note**: This property is read-only.

``` js
var result = PerformanceTiming.domainLookupEnd;
```

## Return Value

Returns an object of type unsigned longunsigned long

## Examples

``` js
var perftime = performance.timing;
document.write("domainLookupEnd: " + perftime.domainLookupEnd + "<br />");
```

## Related specifications

[W3C Navigation Timing Specification 2](http://www.w3.org/TR/navigation-timing-2/)
:   W3C Working Draft
