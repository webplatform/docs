---
title: 'coords'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/geolocation/Position
    href: /apis/geolocation/Position
  return:
    predicate: 'Returns an object of type '
    value: ''
    href: /apis/geolocation/Position
standardization_status: 'W3C Editor''s Draft'
summary: 'Contains a set of geographic coordinates together with their associated accuracy, as well as a set of other optional attributes such as altitude and speed.'
tags:
  - API_Object_Properties
  - API
  - Geolocation
uri: apis/geolocation/Position/coords

---
## Summary

Contains a set of geographic coordinates together with their associated accuracy, as well as a set of other optional attributes such as altitude and speed.

Property of [apis/geolocation/Position](/apis/geolocation/Position)[apis/geolocation/Position](/apis/geolocation/Position)

## Syntax

**Note**: This property is read-only.

``` js
var result = Position.coords;
```

## Return Value

Returns an object of type

Coordinates

## Examples

``` js
var poscoords = position.coords;
//Coordinates properties are now available
alert(poscoords.altitude);
alert(poscoords.heading);
//etc.
```

## Related specifications

[W3C Geolocation Specification](http://dev.w3.org/geo/api/spec-source.html)
:   W3C Editor's Draft
