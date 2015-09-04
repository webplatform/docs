---
title: code
tags:
  0: API
  1: Object
  2: Properties
  4: Geolocation
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The error code of the current PositionError.'
uri: apis/geolocation/PositionError/code

---
# code

## Summary

The error code of the current PositionError.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/geolocation/PositionError](/apis/geolocation/PositionError)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = PositionError.code;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

Must be one of the following constant values:

-   PERMISSION\_DENIED (numeric value 1): The location acquisition process failed because the document does not have permission to use the Geolocation API.
-   POSITION\_UNAVAILABLE (numeric value 2): The position of the device could not be determined. For instance, one or more of the location providers used in the location acquisition process reported an internal error that caused the process to fail entirely.
-   TIMEOUT (numeric value 3): The length of time specified by the *timeout* property has elapsed before the implementation could successfully acquire a new **Position** object.

## Examples

``` {.js}
alert(PositionError.code);
```

## Related specifications

Specification
:   Status
[W3C Geolocation Specification](http://dev.w3.org/geo/api/spec-source.html)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

