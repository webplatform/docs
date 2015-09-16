---
title: alititudeAccuracy
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
summary: 'Denotes the accuracy level of the altitude coordinate, specified in meters. If the implementation cannot provide altitude information, the value of this attribute must be null.'
tags:
  0: API
  1: Object
  2: Properties
  4: Geolocation
uri: apis/geolocation/Coordinates/alititudeAccuracy

---
## Summary

Denotes the accuracy level of the altitude coordinate, specified in meters. If the implementation cannot provide altitude information, the value of this attribute must be null.

Property of [apis/geolocation/Coordinates](/apis/geolocation/Coordinates)[apis/geolocation/Coordinates](/apis/geolocation/Coordinates)

## Syntax

**Note**: This property is read-only.

``` js
var result = Coordinates.alititudeAccuracy;
```

## Return Value

Returns an object of type NumberNumber

## Examples

``` js
//Assuming the variable altitude_accuracy_threshold has been set
if (position.coords.altitudeAccuracy < altitude_accuracy_threshold) {
   // The altitude position is relatively accurate.
   } else {
   // The altitude position is potentially inaccurate.
   }
```

## Related specifications

[W3C Geolocation Specification](http://dev.w3.org/geo/api/spec-source.html)
:   W3C Editor's Draft
