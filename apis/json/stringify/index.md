---
title: 'JSON.stringify'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/json
    href: /apis/json
  return_type:
    predicate: 'Returns an object of type  '
    value: String
    href: /apis/json
standardization_status: 'W3C Recommendation'
summary: 'Export a JavaScript object to a JSON string.'
tags:
  - API
  - Object
  - Methods
  - JavaScript
uri: apis/json/stringify

---
## Summary

Export a JavaScript object to a JSON string.

Method of [apis/json](/apis/json)[apis/json](/apis/json)

## Syntax

``` js
var  = JSON.stringify(JavaScript object);
```

## Parameters

### JavaScript object

 Data-type
:   String

 The JavaScript object to convert to a string.

## Return Value

Returns an object of type StringString

A string representation of the JavaScript object.

## Examples

``` js
// Returns string '{"type":"Mage","stats":[10,3,5]}'
JSON.stringify({
  type: 'Mage',
  stats: [10, 3, 5]
});
```

## Related specifications

[JSON-LD 1.0](http://www.w3.org/TR/json-ld/)
:   W3C Recommendation
