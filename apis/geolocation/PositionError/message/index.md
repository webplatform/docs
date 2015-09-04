---
title: message
tags:
  0: API
  1: Object
  2: Properties
  4: Geolocation
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The error text of the current PositionError, describing the details of the error encountered. This attribute is primarily intended for debugging and developers should not use it directly in their application user interface.'
uri: apis/geolocation/PositionError/message

---
# message

## Summary

The error text of the current PositionError, describing the details of the error encountered. This attribute is primarily intended for debugging and developers should not use it directly in their application user interface.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/geolocation/PositionError](/apis/geolocation/PositionError)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = PositionError.message;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

## Examples

``` {.js}
alert(PositionError.message);
```

## Related specifications

Specification
:   Status
[W3C Geolocation Specification](http://dev.w3.org/geo/api/spec-source.html)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

