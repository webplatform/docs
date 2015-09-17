---
title: 'createObjectStore'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://nparashuram.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=#createObjectStore&'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/indexeddb/IDBDatabase
    href: /apis/indexeddb/IDBDatabase
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /apis/indexeddb/IDBDatabase
standardization_status: 'W3C Proposed Recommendation'
summary: 'The createObjectStore method enables you to create object stores inside an indexedDB database. The creation of an object store is only possible inside a &quot;versionchange&quot; transaction.'
tags:
  - API_Object_Methods
  - API
  - IndexedDB
uri: apis/indexeddb/IDBDatabase/createObjectStore

---
## Summary

The createObjectStore method enables you to create object stores inside an indexedDB database. The creation of an object store is only possible inside a &quot;versionchange&quot; transaction.

Method of [apis/indexeddb/IDBDatabase](/apis/indexeddb/IDBDatabase)[apis/indexeddb/IDBDatabase](/apis/indexeddb/IDBDatabase)

## Syntax

``` js
var IDBObjectStore = IDBDatabase.createObjectStore(name, optionalParameters);
```

## Parameters

### name

 Data-type
:   String

 The name of the object store to be created.

### optionalParameters

 Data-type
:   DOM Node

(Optional)

An object literal containing one or more of the following attributes:

-   **keyPath**: specifies the key path of the new object store. If the attribute is null, no key path is specified. In this case the key isn't an attribute of the object stored in the value
-   **autoIncrement**: specifies whether the object store should have a key generator. If a key generator is present, the key will be automatically incremented when objects get inserted.

## Return Value

Returns an object of type DOM NodeDOM Node

[**IDBObjectStore**](/apis/indexeddb/IDBObjectStore)

An object representing the new object store.

## Examples

``` js
// the db object was opened in the upgradeNeeded method
try {
  var objectStore = db.createObjectStore("ObjectStore_BookList", {
    "keyPath": "id",
    "autoIncrement": true
  });
  write("Object Store created", objectStore);
} catch (e) {
  write("Error occured", e);
}​
```

[View live example](http://nparashuram.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=#createObjectStore&)

## Notes

The method throws an exception if

-   This method was not called from a "versionchange" transaction. Also occurs if a request is made on a source object that has been deleted or removed.
-   If an object store with the same name, compared in a case-sensitive manner, already exists in the connected database.
-   If autoIncrement is set to true, and keyPath either is the empty string, or an Array containing the empty string.

## Related specifications

[W3C Proposed Recommendation](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation
