---
title: type
tags:
  0: API
  1: Object
  2: Properties
  4: Navigation
  5: Timing
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Returns the type of the last non-redirect navigation in the current browsing context. See Notes.'
uri: 'apis/navigation timing/PerformanceNavigation/type'

---
# type

## Summary

Returns the type of the last non-redirect navigation in the current browsing context. See Notes.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/navigation timing/PerformanceNavigation](/apis/navigation_timing/PerformanceNavigation)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = PerformanceNavigation.type;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned short</span></span>

## Examples

``` {.js}
var perfnavtyp = performance.navigation.type;
alert(perfnavtyp); // see Notes
```

## Notes

This attribute must have one of the following navigation type values.

-   TYPE\_NAVIGATE (0): Navigation started by clicking on a link, or entering the URL in the user agent's address bar, or form submission, or initializing through a script operation other than the ones used by TYPE\_RELOAD and TYPE\_BACK\_FORWARD as listed below.
-   TYPE\_RELOAD (1): Navigation through the reload operation or the location.reload() method.
-   TYPE\_BACK\_FORWARD (2): Navigation through a history traversal operation.
-   TYPE\_RESERVED (255): Any navigation types not defined by values above.

## Related specifications

Specification
:   Status
[W3C Navigation Timing Specification 2](http://www.w3.org/TR/navigation-timing-2/)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

