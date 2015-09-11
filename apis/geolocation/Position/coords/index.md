---
title: coords
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
  0: API
  1: Object
  2: Properties
  4: Geolocation
uri: apis/geolocation/Position/coords

---
## <span>Summary</span>

Contains a set of geographic coordinates together with their associated accuracy, as well as a set of other optional attributes such as altitude and speed.

Property of [apis/geolocation/Position](/apis/geolocation/Position)[apis/geolocation/Position](/apis/geolocation/Position)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = Position.coords;
```

## <span>Return Value</span>

Returns an object of type<span></span>

Coordinates

## <span>Examples</span>

``` js
var poscoords = position.coords;
//Coordinates properties are now available
alert(poscoords.altitude);
alert(poscoords.heading);
//etc.
```

## <span>Related specifications</span>

[W3C Geolocation Specification](http://dev.w3.org/geo/api/spec-source.html)
:   W3C Editor's Draft
