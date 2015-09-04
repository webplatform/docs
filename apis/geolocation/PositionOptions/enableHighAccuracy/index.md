---
title: enableHighAccuracy
tags:
  0: API
  1: Object
  2: Properties
  4: Geolocation
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'A request from the application to receive the best possible location results. The intended purpose of this attribute is to allow applications to inform the implementation that they do not require high accuracy geolocation fixes so the implementation can avoid using geolocation providers that consume a significant amount of power (e.g., GPS).'
uri: apis/geolocation/PositionOptions/enableHighAccuracy

---
# enableHighAccuracy

## Summary

A request from the application to receive the best possible location results. The intended purpose of this attribute is to allow applications to inform the implementation that they do not require high accuracy geolocation fixes so the implementation can avoid using geolocation providers that consume a significant amount of power (e.g., GPS).

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/geolocation/PositionOptions](/apis/geolocation/PositionOptions)</span></span>

## Syntax

``` {.js}
var result = PositionOptions.enableHighAccuracy;
PositionOptions.enableHighAccuracy = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

Default is *false*.

## Examples

``` {.js}
//Request the best possible geolocation fix
PositionOptions.enableHighAccuracy = true;
```

## Related specifications

Specification
:   Status
[W3C Geolocation Specification](http://dev.w3.org/geo/api/spec-source.html)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

