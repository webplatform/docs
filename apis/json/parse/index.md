---
title: JSON.parse
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/json
    href: /apis/json
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /apis/json
standardization_status: 'W3C Recommendation'
summary: 'Parse a JSON string to a JavaScript object.'
tags:
  - API
  - Object
  - Methods
  - JavaScript
uri: apis/json/parse

---
## Summary

Parse a JSON string to a JavaScript object.

Method of [apis/json](/apis/json)[apis/json](/apis/json)

## Syntax

``` js
var  = JSON.parse(json string);
```

## Parameters

### json string

 Data-type
:   String

 A JSON string.

## Return Value

Returns an object of type

A JavaScript object representing the JSON string.

## Examples

``` html
var json = '{"result":true,"count":1}',
    obj = JSON && JSON.parse(json)
```

## Notes

This method will throw an error if the argument is not a valid JSON string. You should wrap the parse call in a try/catch block.

## Related specifications

[JSON-LD 1.0](http://www.w3.org/TR/json-ld/)
:   W3C Recommendation
