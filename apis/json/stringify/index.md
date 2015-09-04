---
title: stringify
tags:
  - API
  - Object
  - Methods
  - JavaScript
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Export a JavaScript object to a JSON string.'
uri: apis/json/stringify

---
# JSON.stringify

## Summary

Export a JavaScript object to a JSON string.

*Method of [apis/json](/apis/json)*

## Syntax

``` {.js}
var  = JSON.stringify(JavaScript object);
```

## Parameters

### JavaScript object

 Data-typeÂ
:   String

 The JavaScript object to convert to a string.

## Return Value

Returns an object of type String.

A string representation of the JavaScript object.

## Examples

``` {.js}
// Returns string '{"type":"Mage","stats":[10,3,5]}'
JSON.stringify({
  type: 'Mage',
  stats: [10, 3, 5]
});
```

## Related specifications

Specification
:   Status
[JSON-LD 1.0](http://www.w3.org/TR/json-ld/)
:   W3C Recommendation

