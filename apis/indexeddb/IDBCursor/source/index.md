---
title: 'source'
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/indexeddb/IDBCursor
    href: /apis/indexeddb/IDBCursor
summary: 'On getting, returns the IDBObjectStore or IDBIndex that the cursor is iterating. This function never returns null or throws an exception, even if the cursor is currently being iterated, has iterated past its end, or its transaction is not active.'
tags:
  - API_Object_Properties
  - API
  - IndexedDB
  - Needs_Examples
uri: apis/indexeddb/IDBCursor/source

---
## Summary

On getting, returns the IDBObjectStore or IDBIndex that the cursor is iterating. This function never returns null or throws an exception, even if the cursor is currently being iterated, has iterated past its end, or its transaction is not active.

Property of [apis/indexeddb/IDBCursor](/apis/indexeddb/IDBCursor)[apis/indexeddb/IDBCursor](/apis/indexeddb/IDBCursor)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.source;
```

