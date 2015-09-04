---
title: deleteIndex
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
readiness: 'Ready to Use'
standardization_status: 'W3C Proposed Recommendation'
summary: 'This method destroys the index with the given name in the connected database. Note that this method must only be called from a "versionchange" transaction callback.'
code_samples:
  - 'http://nparashuram.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=Delete%20Index&'
uri: apis/indexeddb/IDBObjectStore/deleteIndex

---
# deleteIndex

## Summary

This method destroys the index with the given name in the connected database. Note that this method must only be called from a "versionchange" transaction callback.

*Method of [apis/indexeddb/IDBObjectStore](/apis/indexeddb/IDBObjectStore)*

## Syntax

``` {.js}
 objectStore.deleteIndex(indexName);
```

## Parameters

### indexName

 Data-typeÂ
:   String

 Name of the index to be deleted.

## Return Value

No return value

## Examples

``` {.js}
var objectStore = transaction.objectStore("ObjectStore_BookList");
objectStore.deleteIndex("priceIndex");
```

[View live example](http://nparashuram.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=Delete%20Index&)

## Notes

Throws an exception when

-   This method was not called from a "versionchange" transaction callback.
-   There is no index with the given name, compared in a case-sensitive manner, in the connected database.

## Related specifications

Specification
:   Status
[W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

