---
title: deleteIndex
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://nparashuram.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=Delete%20Index&'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/indexeddb/IDBObjectStore
    href: /apis/indexeddb/IDBObjectStore
standardization_status: 'W3C Proposed Recommendation'
summary: 'This method destroys the index with the given name in the connected database. Note that this method must only be called from a &quot;versionchange&quot; transaction callback.'
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
uri: apis/indexeddb/IDBObjectStore/deleteIndex

---
## <span>Summary</span>

This method destroys the index with the given name in the connected database. Note that this method must only be called from a &quot;versionchange&quot; transaction callback.

Method of [apis/indexeddb/IDBObjectStore](/apis/indexeddb/IDBObjectStore)[apis/indexeddb/IDBObjectStore](/apis/indexeddb/IDBObjectStore)

## <span>Syntax</span>

``` js
 objectStore.deleteIndex(indexName);
```

## <span>Parameters</span>

### <span>indexName</span>

 Data-type
:   String

 Name of the index to be deleted.

## <span>Return Value</span>

No return value

## <span>Examples</span>

``` js
var objectStore = transaction.objectStore("ObjectStore_BookList");
objectStore.deleteIndex("priceIndex");
```

[View live example](http://nparashuram.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=Delete%20Index&)

## <span>Notes</span>

Throws an exception when

-   This method was not called from a "versionchange" transaction callback.
-   There is no index with the given name, compared in a case-sensitive manner, in the connected database.

## <span>Related specifications</span>

[W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation
