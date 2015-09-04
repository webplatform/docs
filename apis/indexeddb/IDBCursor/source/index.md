---
title: source
tags:
  0: API
  1: Object
  2: Properties
  4: IndexedDB
readiness: 'In Progress'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'On getting, returns the IDBObjectStore or IDBIndex that the cursor is iterating. This function never returns null or throws an exception, even if the cursor is currently being iterated, has iterated past its end, or its transaction is not active.'
uri: apis/indexeddb/IDBCursor/source

---
# source

## Summary

On getting, returns the IDBObjectStore or IDBIndex that the cursor is iterating. This function never returns null or throws an exception, even if the cursor is currently being iterated, has iterated past its end, or its transaction is not active.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/indexeddb/IDBCursor](/apis/indexeddb/IDBCursor)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.source;
```

**Needs Examples**: This section should include examples.

