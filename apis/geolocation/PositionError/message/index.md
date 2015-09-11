---
title: message
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
    value: String
    href: /apis/geolocation/PositionError
standardization_status: 'W3C Editor''s Draft'
summary: 'The error text of the current PositionError, describing the details of the error encountered. This attribute is primarily intended for debugging and developers should not use it directly in their application user interface.'
tags:
  0: API
  1: Object
  2: Properties
  4: Geolocation
uri: apis/geolocation/PositionError/message

---
## <span>Summary</span>

The error text of the current PositionError, describing the details of the error encountered. This attribute is primarily intended for debugging and developers should not use it directly in their application user interface.

Property of [apis/geolocation/PositionError](/apis/geolocation/PositionError)[apis/geolocation/PositionError](/apis/geolocation/PositionError)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = PositionError.message;
```

## <span>Return Value</span>

Returns an object of type StringString

## <span>Examples</span>

``` js
alert(PositionError.message);
```

## <span>Related specifications</span>

[W3C Geolocation Specification](http://dev.w3.org/geo/api/spec-source.html)
:   W3C Editor's Draft
