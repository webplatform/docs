---
title: bound
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/indexeddb/IDBKeyRange
    href: /apis/indexeddb/IDBKeyRange
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /apis/indexeddb/IDBKeyRange
standardization_status: 'W3C Proposed Recommendation'
summary: 'Creates and returns a new key range with lower set to lower, lowerOpen set to lowerOpen, upper set to upper and upperOpen set to upperOpen.'
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
uri: apis/indexeddb/IDBKeyRange/bound

---
## <span>Summary</span>

Creates and returns a new key range with lower set to lower, lowerOpen set to lowerOpen, upper set to upper and upperOpen set to upperOpen.

Method of [apis/indexeddb/IDBKeyRange](/apis/indexeddb/IDBKeyRange)[apis/indexeddb/IDBKeyRange](/apis/indexeddb/IDBKeyRange)

## <span>Syntax</span>

``` js
var range = IDBKeyRange.bound(lower, upper, lowerOpen, upperOpen);
```

## <span>Parameters</span>

### <span>lower</span>

 Data-type
:   String

 The lower value of the key range.

### <span>upper</span>

 Data-type
:   String

 The upper value of the key range.

### <span>lowerOpen</span>

 Data-type
:   Boolean

 Indicates whether the key range includes the lower value.

### <span>upperOpen</span>

 Data-type
:   Boolean

 Indicates whether the key range includes the upper value.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

A range that can be used for specifying the range of cursors.

## <span>Examples</span>

``` js
var range = new IDBKeyRange.bound(2, 4);
var cursor = store.openCursor(range);
// each value is a contact and each key is the id for that
// contact whose id is between 2 and 4, both inclusive
```

## <span>Usage</span>

     Raises a DOMException when either the lower or upper parameters were not passed a valid key or the lower key is greater than the upper key or the lower key and upper key match and either of the bounds are open.

## <span>Related specifications</span>

[W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation
