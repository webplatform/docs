---
title: upperBound
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
summary: 'Creates and returns a new key range with lower set to undefined, lowerOpen set to true, upper set to upper and and upperOpen set to open.'
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
uri: apis/indexeddb/IDBKeyRange/upperBound

---
## <span>Summary</span>

Creates and returns a new key range with lower set to undefined, lowerOpen set to true, upper set to upper and and upperOpen set to open.

Method of [apis/indexeddb/IDBKeyRange](/apis/indexeddb/IDBKeyRange)[apis/indexeddb/IDBKeyRange](/apis/indexeddb/IDBKeyRange)

## <span>Syntax</span>

``` js
var object = object.upperBound(bound, open);
```

## <span>Parameters</span>

### <span>bound</span>

 Data-type
:   Blob

 The upper value of the key range.

### <span>open</span>

 Data-type
:   Boolean

 Indicates whether the key range includes the **bound** value.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

**Needs Examples**: This section should include examples.

### <span>Syntax</span>

### <span>Standards information</span>

-   [Indexed Database API](http://go.microsoft.com/fwlink/p/?LinkId=224519)
