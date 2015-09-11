---
title: multiEntry
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/indexeddb/IDBIndex
    href: /apis/indexeddb/IDBIndex
  return:
    predicate: 'Returns an object of type '
    value: Boolean
    href: /apis/indexeddb/IDBIndex
summary: 'Affects how the index behaves when the result of evaluating the index''s key path yields an array. If true, there is one record in the index for each item in an array of keys. If false, then there is one record for each key that is an array.'
tags:
  0: API
  1: Object
  2: Properties
  4: IndexedDB
uri: apis/indexeddb/IDBIndex/multiEntry

---
## <span>Summary</span>

Affects how the index behaves when the result of evaluating the index's key path yields an array. If true, there is one record in the index for each item in an array of keys. If false, then there is one record for each key that is an array.

Property of [apis/indexeddb/IDBIndex](/apis/indexeddb/IDBIndex)[apis/indexeddb/IDBIndex](/apis/indexeddb/IDBIndex)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = element.multiEntry;
```

## <span>Return Value</span>

Returns an object of type BooleanBoolean

**Needs Examples**: This section should include examples.

