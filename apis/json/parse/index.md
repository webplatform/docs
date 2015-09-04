---
title: parse
tags:
  - API
  - Object
  - Methods
  - JavaScript
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Parse a JSON string to a JavaScript object.'
uri: apis/json/parse

---
# JSON.parse

## Summary

Parse a JSON string to a JavaScript object.

*Method of [apis/json](/apis/json)*

## Syntax

``` {.js}
var  = JSON.parse(json string);
```

## Parameters

### json string

 Data-typeÂ
:   String

 A JSON string.

## Return Value

Returns an object of type .

A JavaScript object representing the JSON string.

## Examples

    var json = '{"result":true,"count":1}',
        obj = JSON && JSON.parse(json)

## Notes

This method will throw an error if the argument is not a valid JSON string. You should wrap the parse call in a try/catch block.

## Related specifications

Specification
:   Status
[JSON-LD 1.0](http://www.w3.org/TR/json-ld/)
:   W3C Recommendation

