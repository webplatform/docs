---
title: 'timestamp'
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
summary: 'Represents the time when the Position object was acquired, represented as a DOMTimeStamp.'
tags:
  - API_Object_Properties
  - API
  - Geolocation
uri: apis/geolocation/Position/timestamp

---
## Summary

Represents the time when the Position object was acquired, represented as a DOMTimeStamp.

Property of [apis/geolocation/Position](/apis/geolocation/Position)[apis/geolocation/Position](/apis/geolocation/Position)

## Syntax

**Note**: This property is read-only.

``` js
var result = Position.timestamp;
```

## Return Value

Returns an object of type

DOMTimeStamp

## Examples

``` js
//Assuming the variable fresh_threshold has been set
if (position.timestamp < fresh_threshold) {
   // The position is relatively recent.
   } else {
   // The position is potentially outdated.
   }
```

## Related specifications

[W3C Geolocation Specification](http://dev.w3.org/geo/api/spec-source.html)
:   W3C Editor's Draft
