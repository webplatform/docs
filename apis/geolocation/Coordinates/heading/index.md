---
title: heading
tags:
  0: API
  1: Object
  2: Properties
  4: Geolocation
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Denotes the direction of travel of the hosting device specified in degrees, where 0° ≤ heading < 360°, counting clockwise relative to the true north. If the implementation cannot provide heading information, the value of this attribute must be null. If the hosting device is stationary (i.e., the value of the speed attribute is 0), then the value of this attribute must be NaN.'
uri: apis/geolocation/Coordinates/heading

---
# heading

## Summary

Denotes the direction of travel of the hosting device specified in degrees, where 0° ≤ heading \< 360°, counting clockwise relative to the true north. If the implementation cannot provide heading information, the value of this attribute must be null. If the hosting device is stationary (i.e., the value of the speed attribute is 0), then the value of this attribute must be NaN.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/geolocation/Coordinates](/apis/geolocation/Coordinates)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = Coordinates.heading;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

## Examples

``` {.js}
if (position.coords.heading > 87 && position.coords.heading < 93) {
   // moving within 5 degrees of due east
   } else {
   // not moving east
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

