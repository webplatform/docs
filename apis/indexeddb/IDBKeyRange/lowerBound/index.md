---
title: 'lowerBound'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/indexeddb/IDBKeyRange
    href: /apis/indexeddb/IDBKeyRange
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /apis/indexeddb/IDBKeyRange
summary: 'Creates and returns a new key range with lower set to lower, lowerOpen set to open, upper set to undefined and and upperOpen set to true.'
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
uri: apis/indexeddb/IDBKeyRange/lowerBound

---
## Summary

Creates and returns a new key range with lower set to lower, lowerOpen set to open, upper set to undefined and and upperOpen set to true.

Method of [apis/indexeddb/IDBKeyRange](/apis/indexeddb/IDBKeyRange)[apis/indexeddb/IDBKeyRange](/apis/indexeddb/IDBKeyRange)

## Syntax

``` js
var object = object.lowerBound(bound, open);
```

## Parameters

### bound

 Data-type
:   Blob

 The lower value of the key range.

### open

 Data-type
:   Boolean

 Indicates whether the key range includes the **bound** value.

## Return Value

Returns an object of type DOM NodeDOM Node

**Needs Examples**: This section should include examples.

### Syntax

### Standards information

-   [Indexed Database API](http://go.microsoft.com/fwlink/p/?LinkId=224519)
