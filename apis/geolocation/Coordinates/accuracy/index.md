---
title: 'accuracy'
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
summary: 'Denotes the accuracy level of the latitude and longitude coordinates. It is specified in meters and must be supported by all implementations. The value of this attribute must be a non-negative real number.'
tags:
  0: API
  1: Object
  2: Properties
  4: Geolocation
uri: apis/geolocation/Coordinates/accuracy

---
## Summary

Denotes the accuracy level of the latitude and longitude coordinates. It is specified in meters and must be supported by all implementations. The value of this attribute must be a non-negative real number.

Property of [apis/geolocation/Coordinates](/apis/geolocation/Coordinates)[apis/geolocation/Coordinates](/apis/geolocation/Coordinates)

## Syntax

**Note**: This property is read-only.

``` js
var result = Coordinates.accuracy;
```

## Return Value

Returns an object of type NumberNumber

## Examples

``` js
//Assuming the variable accuracy_threshold has been set
if (position.coords.accuracy < accuracy_threshold) {
   // The position is relatively accurate.
   } else {
   // The position is potentially inaccurate.
   }
```

## Related specifications

[W3C Geolocation Specification](http://dev.w3.org/geo/api/spec-source.html)
:   W3C Editor's Draft
