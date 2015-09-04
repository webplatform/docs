---
title: timestamp
tags:
  0: API
  1: Object
  2: Properties
  4: Geolocation
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Represents the time when the Position object was acquired, represented as a DOMTimeStamp.'
uri: apis/geolocation/Position/timestamp

---
# timestamp

## Summary

Represents the time when the Position object was acquired, represented as a DOMTimeStamp.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/geolocation/Position](/apis/geolocation/Position)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = Position.timestamp;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value"></span></span>

DOMTimeStamp

## Examples

``` {.js}
//Assuming the variable fresh_threshold has been set
if (position.timestamp < fresh_threshold) {
   // The position is relatively recent.
   } else {
   // The position is potentially outdated.
   }
```

## Related specifications

Specification
:   Status
[W3C Geolocation Specification](http://dev.w3.org/geo/api/spec-source.html)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

