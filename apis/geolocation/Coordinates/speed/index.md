---
title: 'speed'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/geolocation/Coordinates
    href: /apis/geolocation/Coordinates
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /apis/geolocation/Coordinates
standardization_status: 'W3C Editor''s Draft'
summary: 'Denotes the magnitude of the horizontal component of the hosting device''s current velocity specified in meters per second. If the implementation cannot provide speed information, the value of this attribute must be null. Otherwise, the value of this attribute must be a non-negative real number.'
tags:
  - API_Object_Properties
  - API
  - Geolocation
uri: apis/geolocation/Coordinates/speed

---
## Summary

Denotes the magnitude of the horizontal component of the hosting device's current velocity specified in meters per second. If the implementation cannot provide speed information, the value of this attribute must be null. Otherwise, the value of this attribute must be a non-negative real number.

Property of [apis/geolocation/Coordinates](/apis/geolocation/Coordinates)[apis/geolocation/Coordinates](/apis/geolocation/Coordinates)

## Syntax

**Note**: This property is read-only.

``` js
var result = Coordinates.speed;
```

## Return Value

Returns an object of type NumberNumber

## Examples

``` js
if (position.coords.speed > 0) {
   // moving
   } else {
   // not moving
   }
```

## Related specifications

[W3C Geolocation Specification](http://dev.w3.org/geo/api/spec-source.html)
:   W3C Editor's Draft
