---
title: 'clear'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://axemclion.github.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=Clear%20ObjectStore&'
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
    value: 'DOM Node'
    href: /apis/indexeddb/IDBObjectStore
standardization_status: 'W3C Working Draft'
summary: 'Removes all records from the object store.'
tags:
  - API_Object_Methods
  - API
  - IndexedDB
uri: apis/indexeddb/IDBObjectStore/clear

---
## Summary

Removes all records from the object store.

Method of [apis/indexeddb/IDBObjectStore](/apis/indexeddb/IDBObjectStore)[apis/indexeddb/IDBObjectStore](/apis/indexeddb/IDBObjectStore)

## Syntax

``` js
var idbRequest = objectStore.clear();
```

## Return Value

Returns an object of type DOM NodeDOM Node

## Examples

``` js
store = db.createObjectStore("store1", { autoIncrement: true });
store.put("a"); // Will get key 1
store.delete(1);
store.put("b"); // Will get key 2
store.clear(); // Clears all records from the store
```

[View live example](http://axemclion.github.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=Clear%20ObjectStore&)

## Usage

     The method throws a DOMException if

-   The transaction this IDBObjectStore belongs to is not active.
-   The mode of the transaction this IDBObjectStore belongs to is "readonly".
-   Occurs if a request is made on a source object that has been deleted or removed.

### Syntax

### Standards information

-   [Indexed Database API](http://go.microsoft.com/fwlink/p/?LinkId=224519)
