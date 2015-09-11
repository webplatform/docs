---
title: count
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
  0: API
  1: Object
  2: Methods
  4: IndexedDB
uri: apis/indexeddb/IDBObjectStore/count

---
## <span>Summary</span>

The count method returns the number of records in an object store.

Method of [apis/indexeddb/IDBObjectStore](/apis/indexeddb/IDBObjectStore)[apis/indexeddb/IDBObjectStore](/apis/indexeddb/IDBObjectStore)

## <span>Syntax</span>

``` js
var recordCount = objectStore.count(key);
```

## <span>Parameters</span>

### <span>key</span>

 Data-type
:   DOM Node

(Optional)

A key value or a reference to a [**IDBKeyRange**](/apis/indexeddb/IDBKeyRange) object.

## <span>Return Value</span>

Returns an object of type NumberNumber

[**IDBRequest**](/apis/indexeddb/IDBRequest)

The number of records matching the specified value or "0" if no matches are found.

**Needs Examples**: This section should include examples.

## <span>Notes</span>

The method throws and exception is

-   The transaction this IDBObjectStoreSync belongs to is not active.
-   The key parameter is not a valid key or a key range.
-   Occurs if a request is made on a source object that has been deleted or removed.

### <span>Syntax</span>