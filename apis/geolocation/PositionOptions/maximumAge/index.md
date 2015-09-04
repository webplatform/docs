---
title: maximumAge
tags:
  0: API
  1: Object
  2: Properties
  4: Geolocation
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Indicates that the application is willing to accept a cached position whose age is no greater than the specified time (in milliseconds).'
uri: apis/geolocation/PositionOptions/maximumAge

---
# maximumAge

## Summary

Indicates that the application is willing to accept a cached position whose age is no greater than the specified time (in milliseconds).

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/geolocation/PositionOptions](/apis/geolocation/PositionOptions)</span></span>

## Syntax

``` {.js}
var result = PositionOptions.maximumAge;
PositionOptions.maximumAge = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned long</span></span>

## Examples

``` {.js}
//10000ms = 10sec
if (PositionOptions.maximumAge < 10000) {
   // The position is relatively recent.
   } else {
   // The position is potentially outdated.
   }
```

## Related specifications

Specification
:   Status
[W3C Geolocation Specification](http://dev.w3.org/geo/api/spec-source.html)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

