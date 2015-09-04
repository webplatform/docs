---
title: altitude
tags:
  0: API
  1: Object
  2: Properties
  4: Geolocation
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Denotes the height of the position, specified in meters above the ellipsoid. If the implementation cannot provide altitude information, the value of this attribute must be null.'
uri: apis/geolocation/Coordinates/altitude

---
# altitude

## Summary

Denotes the height of the position, specified in meters above the ellipsoid. If the implementation cannot provide altitude information, the value of this attribute must be null.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/geolocation/Coordinates](/apis/geolocation/Coordinates)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = Coordinates.altitude;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

## Examples

``` {.js}
if (position.coords.altitude <= 2) {
   // at ground level
   } else {
   // above ground level
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

