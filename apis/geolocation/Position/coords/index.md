---
title: coords
tags:
  0: API
  1: Object
  2: Properties
  4: Geolocation
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Contains a set of geographic coordinates together with their associated accuracy, as well as a set of other optional attributes such as altitude and speed.'
uri: apis/geolocation/Position/coords

---
# coords

## Summary

Contains a set of geographic coordinates together with their associated accuracy, as well as a set of other optional attributes such as altitude and speed.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/geolocation/Position](/apis/geolocation/Position)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = Position.coords;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value"></span></span>

Coordinates

## Examples

``` {.js}
var poscoords = position.coords;
//Coordinates properties are now available
alert(poscoords.altitude);
alert(poscoords.heading);
//etc.
```

## Related specifications

Specification
:   Status
[W3C Geolocation Specification](http://dev.w3.org/geo/api/spec-source.html)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

