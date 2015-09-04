---
title: multiEntry
tags:
  0: API
  1: Object
  2: Properties
  4: IndexedDB
readiness: 'In Progress'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'Affects how the index behaves when the result of evaluating the index''s key path yields an array. If true, there is one record in the index for each item in an array of keys. If false, then there is one record for each key that is an array.'
uri: apis/indexeddb/IDBIndex/multiEntry

---
# multiEntry

## Summary

Affects how the index behaves when the result of evaluating the index's key path yields an array. If true, there is one record in the index for each item in an array of keys. If false, then there is one record for each key that is an array.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/indexeddb/IDBIndex](/apis/indexeddb/IDBIndex)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.multiEntry;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

**Needs Examples**: This section should include examples.

