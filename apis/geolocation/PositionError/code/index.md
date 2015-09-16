---
title: 'code'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/geolocation/PositionError
    href: /apis/geolocation/PositionError
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /apis/geolocation/PositionError
standardization_status: 'W3C Editor''s Draft'
summary: 'The error code of the current PositionError.'
tags:
  0: API
  1: Object
  2: Properties
  4: Geolocation
uri: apis/geolocation/PositionError/code

---
## Summary

The error code of the current PositionError.

Property of [apis/geolocation/PositionError](/apis/geolocation/PositionError)[apis/geolocation/PositionError](/apis/geolocation/PositionError)

## Syntax

**Note**: This property is read-only.

``` js
var result = PositionError.code;
```

## Return Value

Returns an object of type NumberNumber

Must be one of the following constant values:

-   PERMISSION\_DENIED (numeric value 1): The location acquisition process failed because the document does not have permission to use the Geolocation API.
-   POSITION\_UNAVAILABLE (numeric value 2): The position of the device could not be determined. For instance, one or more of the location providers used in the location acquisition process reported an internal error that caused the process to fail entirely.
-   TIMEOUT (numeric value 3): The length of time specified by the *timeout* property has elapsed before the implementation could successfully acquire a new **Position** object.

## Examples

``` js
alert(PositionError.code);
```

## Related specifications

[W3C Geolocation Specification](http://dev.w3.org/geo/api/spec-source.html)
:   W3C Editor's Draft
