---
title: 'count'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/indexeddb/IDBObjectStore
    href: /apis/indexeddb/IDBObjectStore
  return_type:
    predicate: 'Returns an object of type  '
    value: Number
    href: /apis/indexeddb/IDBObjectStore
summary: 'The count method returns the number of records in an object store.'
tags:
  - API_Object_Methods
  - API
  - IndexedDB
  - Needs_Examples
uri: apis/indexeddb/IDBObjectStore/count

---
## Summary

The count method returns the number of records in an object store.

Method of [apis/indexeddb/IDBObjectStore](/apis/indexeddb/IDBObjectStore)[apis/indexeddb/IDBObjectStore](/apis/indexeddb/IDBObjectStore)

## Syntax

``` js
var recordCount = objectStore.count(key);
```

## Parameters

### key

 Data-type
:   DOM Node

(Optional)

A key value or a reference to a [**IDBKeyRange**](/apis/indexeddb/IDBKeyRange) object.

## Return Value

Returns an object of type NumberNumber

[**IDBRequest**](/apis/indexeddb/IDBRequest)

The number of records matching the specified value or "0" if no matches are found.

## Notes

The method throws and exception is

-   The transaction this IDBObjectStoreSync belongs to is not active.
-   The key parameter is not a valid key or a key range.
-   Occurs if a request is made on a source object that has been deleted or removed.

### Syntax
