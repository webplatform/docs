---
title: responseEnd
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
summary: 'Returns the time immediately after the user agent receives the last byte of the current document from the server, relevant application caches or from local resources, or immediately before the transport connection is closed, whichever comes first.'
tags:
  0: API
  1: Object
  2: Properties
  4: Navigation
  5: Timing
uri: 'apis/navigation timing/PerformanceTiming/responseEnd'

---
## <span>Summary</span>

Returns the time immediately after the user agent receives the last byte of the current document from the server, relevant application caches or from local resources, or immediately before the transport connection is closed, whichever comes first.

Property of [apis/navigation timing/PerformanceTiming](/apis/navigation_timing/PerformanceTiming)[apis/navigation timing/PerformanceTiming](/apis/navigation_timing/PerformanceTiming)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = PerformanceTiming.responseEnd;
```

## <span>Return Value</span>

Returns an object of type unsigned longunsigned long

## <span>Examples</span>

``` js
var perftime = performance.timing;
document.write("responseEnd: " + perftime.responseEnd + "<br />");
```

## <span>Related specifications</span>

[Navigation Timing 2](http://www.w3.org/TR/navigation-timing-2/)
:   W3C Working Draft
