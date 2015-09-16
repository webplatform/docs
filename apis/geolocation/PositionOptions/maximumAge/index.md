---
title: maximumAge
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/geolocation/PositionOptions
    href: /apis/geolocation/PositionOptions
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned long'
    href: /apis/geolocation/PositionOptions
standardization_status: 'W3C Editor''s Draft'
summary: 'Indicates that the application is willing to accept a cached position whose age is no greater than the specified time (in milliseconds).'
tags:
  0: API
  1: Object
  2: Properties
  4: Geolocation
uri: apis/geolocation/PositionOptions/maximumAge

---
## Summary

Indicates that the application is willing to accept a cached position whose age is no greater than the specified time (in milliseconds).

Property of [apis/geolocation/PositionOptions](/apis/geolocation/PositionOptions)[apis/geolocation/PositionOptions](/apis/geolocation/PositionOptions)

## Syntax

``` js
var result = PositionOptions.maximumAge;
PositionOptions.maximumAge = value;
```

## Return Value

Returns an object of type unsigned longunsigned long

## Examples

``` js
//10000ms = 10sec
if (PositionOptions.maximumAge < 10000) {
   // The position is relatively recent.
   } else {
   // The position is potentially outdated.
   }
```

## Related specifications

[W3C Geolocation Specification](http://dev.w3.org/geo/api/spec-source.html)
:   W3C Editor's Draft
