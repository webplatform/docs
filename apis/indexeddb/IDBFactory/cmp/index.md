---
title: 'cmp'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/indexeddb/IDBFactory
    href: /apis/indexeddb/IDBFactory
  return_type:
    predicate: 'Returns an object of type  '
    value: Number
    href: /apis/indexeddb/IDBFactory
standardization_status: 'W3C Proposed Recommendation'
summary: 'This method compares two specified keys. Returns 1 if the first key is greater than the second, -1 if the first is less than the second, and 0 if the first is equal to the second.'
tags:
  - API_Object_Methods
  - API
  - IndexedDB
uri: apis/indexeddb/IDBFactory/cmp

---
## Summary

This method compares two specified keys. Returns 1 if the first key is greater than the second, -1 if the first is less than the second, and 0 if the first is equal to the second.

Method of [apis/indexeddb/IDBFactory](/apis/indexeddb/IDBFactory)[apis/indexeddb/IDBFactory](/apis/indexeddb/IDBFactory)

## Syntax

``` js
var result = window.indexeddb.cmp(first, second);
```

## Parameters

### first

 Data-type
:   DOM Node

 The first key to compare

### second

 Data-type
:   String

 The second key to compare

## Return Value

Returns an object of type NumberNumber

The method returns 1 if the first key is greater than the second, -1 if the first is less than the second, and 0 if the first is equal to the second. Throws a DOMException (Data Error) is one of the supplied keys was not a valid key.

## Examples

``` js
var value1 = "Alpha";
var value2 = "Beta";
var result = window.indexedDB.cmp( value1, value2 );
console.log( "Comparison results: " + result );
```

## Related specifications

[W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation
