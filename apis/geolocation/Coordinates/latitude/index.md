---
title: latitude
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
summary: 'Geographic latitude specified in decimal degrees.'
tags:
  0: API
  1: Object
  2: Properties
  4: Geolocation
uri: apis/geolocation/Coordinates/latitude

---
## <span>Summary</span>

Geographic latitude specified in decimal degrees.

Property of [apis/geolocation/Coordinates](/apis/geolocation/Coordinates)[apis/geolocation/Coordinates](/apis/geolocation/Coordinates)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = Coordinates.latitude;
```

## <span>Return Value</span>

Returns an object of type NumberNumber

## <span>Examples</span>

``` js
alert('Current coordinates are latitude: ' + position.coords.latitude + ' and longitude: ' + position.coords.longitude);
```

## <span>Related specifications</span>

[W3C Geolocation Specification](http://dev.w3.org/geo/api/spec-source.html)
:   W3C Editor's Draft
