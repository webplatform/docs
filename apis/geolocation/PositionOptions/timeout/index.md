---
title: timeout
tags:
  0: API
  1: Object
  2: Properties
  4: Geolocation
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Denotes the maximum length of time (expressed in milliseconds) that is allowed to pass from the call to getCurrentPosition() or watchPosition() until the corresponding successCallback is invoked.'
uri: apis/geolocation/PositionOptions/timeout

---
# timeout

## Summary

Denotes the maximum length of time (expressed in milliseconds) that is allowed to pass from the call to getCurrentPosition() or watchPosition() until the corresponding successCallback is invoked.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/geolocation/PositionOptions](/apis/geolocation/PositionOptions)</span></span>

## Syntax

``` {.js}
var result = PositionOptions.timeout;
PositionOptions.timeout = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned long</span></span>

## Examples

``` {.js}
//10000ms = 10sec
PositionOptions.timeout = 10000;
```

## Related specifications

Specification
:   Status
[W3C Geolocation Specification](http://dev.w3.org/geo/api/spec-source.html)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

