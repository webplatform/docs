---
title: enableHighAccuracy
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
    value: Boolean
    href: /apis/geolocation/PositionOptions
standardization_status: 'W3C Editor''s Draft'
summary: 'A request from the application to receive the best possible location results. The intended purpose of this attribute is to allow applications to inform the implementation that they do not require high accuracy geolocation fixes so the implementation can avoid using geolocation providers that consume a significant amount of power (e.g., GPS).'
tags:
  0: API
  1: Object
  2: Properties
  4: Geolocation
uri: apis/geolocation/PositionOptions/enableHighAccuracy

---
## <span>Summary</span>

A request from the application to receive the best possible location results. The intended purpose of this attribute is to allow applications to inform the implementation that they do not require high accuracy geolocation fixes so the implementation can avoid using geolocation providers that consume a significant amount of power (e.g., GPS).

Property of [apis/geolocation/PositionOptions](/apis/geolocation/PositionOptions)[apis/geolocation/PositionOptions](/apis/geolocation/PositionOptions)

## <span>Syntax</span>

``` js
var result = PositionOptions.enableHighAccuracy;
PositionOptions.enableHighAccuracy = value;
```

## <span>Return Value</span>

Returns an object of type BooleanBoolean

Default is *false*.

## <span>Examples</span>

``` js
//Request the best possible geolocation fix
PositionOptions.enableHighAccuracy = true;
```

## <span>Related specifications</span>

[W3C Geolocation Specification](http://dev.w3.org/geo/api/spec-source.html)
:   W3C Editor's Draft
