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
## <span>Summary</span>

Parse a JSON string to a JavaScript object.

Method of [apis/json](/apis/json)[apis/json](/apis/json)

## <span>Syntax</span>

``` js
var  = JSON.parse(json string);
```

## <span>Parameters</span>

### <span>json string</span>

 Data-type
:   String

 A JSON string.

## <span>Return Value</span>

Returns an object of type<span></span>

A JavaScript object representing the JSON string.

## <span>Examples</span>

``` html
var json = '{"result":true,"count":1}',
    obj = JSON && JSON.parse(json)
```

## <span>Notes</span>

This method will throw an error if the argument is not a valid JSON string. You should wrap the parse call in a try/catch block.

## <span>Related specifications</span>

[JSON-LD 1.0](http://www.w3.org/TR/json-ld/)
:   W3C Recommendation
