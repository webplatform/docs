---
title: count
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
readiness: 'In Progress'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'The count method returns the number of records in an object store.'
uri: apis/indexeddb/IDBObjectStore/count

---
# count

## Summary

The count method returns the number of records in an object store.

*Method of [apis/indexeddb/IDBObjectStore](/apis/indexeddb/IDBObjectStore)*

## Syntax

``` {.js}
var recordCount = objectStore.count(key);
```

## Parameters

### key

 Data-typeÂ
:   DOM Node

*(Optional)*

A key value or a reference to a [**IDBKeyRange**](/apis/indexeddb/IDBKeyRange) object.

## Return Value

Returns an object of type Number.

[**IDBRequest**](/apis/indexeddb/IDBRequest)

The number of records matching the specified value or "0" if no matches are found.

**Needs Examples**: This section should include examples.

## Notes

The method throws and exception is

-   The transaction this IDBObjectStoreSync belongs to is not active.
-   The key parameter is not a valid key or a key range.
-   Occurs if a request is made on a source object that has been deleted or removed.

### Syntax

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

