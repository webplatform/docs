---
title: accuracy
tags:
  0: API
  1: Object
  2: Properties
  4: Geolocation
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Denotes the accuracy level of the latitude and longitude coordinates. It is specified in meters and must be supported by all implementations. The value of this attribute must be a non-negative real number.'
uri: apis/geolocation/Coordinates/accuracy

---
# accuracy

## Summary

Denotes the accuracy level of the latitude and longitude coordinates. It is specified in meters and must be supported by all implementations. The value of this attribute must be a non-negative real number.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/geolocation/Coordinates](/apis/geolocation/Coordinates)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = Coordinates.accuracy;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

## Examples

``` {.js}
//Assuming the variable accuracy_threshold has been set
if (position.coords.accuracy < accuracy_threshold) {
   // The position is relatively accurate.
   } else {
   // The position is potentially inaccurate.
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

