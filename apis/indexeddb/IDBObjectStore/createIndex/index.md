---
title: createIndex
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
readiness: 'Ready to Use'
standardization_status: 'W3C Proposed Recommendation'
summary: 'This method creates and returns a new index with the given name and parameters in the connected database.'
code_samples:
  - 'http://nparashuram.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=Create%20Index&'
uri: apis/indexeddb/IDBObjectStore/createIndex

---
# createIndex

## Summary

This method creates and returns a new index with the given name and parameters in the connected database.

*Method of [apis/indexeddb/IDBObjectStore](/apis/indexeddb/IDBObjectStore)*

## Syntax

``` {.js}
var index = objectStore.createIndex(name, keyPath, optionalParameters);
```

## Parameters

### name

 Data-typeÂ
:   String

 Name of the index.

### keyPath

 Data-typeÂ
:   String

 Name of the field to be indexed.

### optionalParameters

 Data-typeÂ
:   String

*(Optional)*

The options object whose attributes are optional parameters to this function. 'unique' specifies whether the index's unique flag is set. 'multiEntry' specifies whether the index's multiEntry flag is set.

## Return Value

Returns an object of type DOM Node.

**IDBIndex**

An object representing the new index.

## Examples

``` {.js}
// The transaction is already created

var objectStore = transaction.objectStore("ObjectStore_BookList");
var index = objectStore.createIndex("priceIndex", "price", {
    "unique": false,
    "multiEntry": true
});
```

[View live example](http://nparashuram.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=Create%20Index&)

## Notes

The method throws an exception if

-   This method was not called from a "versionchange" transaction callback. Also occurs if a request is made on a source object that has been deleted or removed.
-   An index with the same name, compared in a case-sensitive manner, already exists in the connected database.

## Related specifications

Specification
:   Status
[W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

