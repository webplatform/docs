---
title: 'timeout'
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
summary: 'Denotes the maximum length of time (expressed in milliseconds) that is allowed to pass from the call to getCurrentPosition() or watchPosition() until the corresponding successCallback is invoked.'
tags:
  0: API
  1: Object
  2: Properties
  4: Geolocation
uri: apis/geolocation/PositionOptions/timeout

---
## Summary

Denotes the maximum length of time (expressed in milliseconds) that is allowed to pass from the call to getCurrentPosition() or watchPosition() until the corresponding successCallback is invoked.

Property of [apis/geolocation/PositionOptions](/apis/geolocation/PositionOptions)[apis/geolocation/PositionOptions](/apis/geolocation/PositionOptions)

## Syntax

``` js
var result = PositionOptions.timeout;
PositionOptions.timeout = value;
```

## Return Value

Returns an object of type unsigned longunsigned long

## Examples

``` js
//10000ms = 10sec
PositionOptions.timeout = 10000;
```

## Related specifications

[W3C Geolocation Specification](http://dev.w3.org/geo/api/spec-source.html)
:   W3C Editor's Draft
