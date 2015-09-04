---
title: cmp
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
readiness: 'Ready to Use'
standardization_status: 'W3C Proposed Recommendation'
summary: 'This method compares two specified keys. Returns 1 if the first key is greater than the second, -1 if the first is less than the second, and 0 if the first is equal to the second.'
uri: apis/indexeddb/IDBFactory/cmp

---
# cmp

## Summary

This method compares two specified keys. Returns 1 if the first key is greater than the second, -1 if the first is less than the second, and 0 if the first is equal to the second.

*Method of [apis/indexeddb/IDBFactory](/apis/indexeddb/IDBFactory)*

## Syntax

``` {.js}
var result = window.indexeddb.cmp(first, second);
```

## Parameters

### first

 Data-typeÂ
:   DOM Node

 The first key to compare

### second

 Data-typeÂ
:   String

 The second key to compare

## Return Value

Returns an object of type Number.

The method returns 1 if the first key is greater than the second, -1 if the first is less than the second, and 0 if the first is equal to the second. Throws a DOMException (Data Error) is one of the supplied keys was not a valid key.

## Examples

``` {.js}
var value1 = "Alpha";
var value2 = "Beta";
var result = window.indexedDB.cmp( value1, value2 );
console.log( "Comparison results: " + result );
```

## Related specifications

Specification
:   Status
[W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

