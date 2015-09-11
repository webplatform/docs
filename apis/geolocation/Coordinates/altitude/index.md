---
title: altitude
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
summary: 'Denotes the height of the position, specified in meters above the ellipsoid. If the implementation cannot provide altitude information, the value of this attribute must be null.'
tags:
  0: API
  1: Object
  2: Properties
  4: Geolocation
uri: apis/geolocation/Coordinates/altitude

---
## <span>Summary</span>

Denotes the height of the position, specified in meters above the ellipsoid. If the implementation cannot provide altitude information, the value of this attribute must be null.

Property of [apis/geolocation/Coordinates](/apis/geolocation/Coordinates)[apis/geolocation/Coordinates](/apis/geolocation/Coordinates)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = Coordinates.altitude;
```

## <span>Return Value</span>

Returns an object of type NumberNumber

## <span>Examples</span>

``` js
if (position.coords.altitude <= 2) {
   // at ground level
   } else {
   // above ground level
   }
```

## <span>Related specifications</span>

[W3C Geolocation Specification](http://dev.w3.org/geo/api/spec-source.html)
:   W3C Editor's Draft
