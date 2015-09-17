---
title: 'deleteDatabase'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://nparashuram.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=#deleteDB&'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/indexeddb/IDBFactory
    href: /apis/indexeddb/IDBFactory
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /apis/indexeddb/IDBFactory
standardization_status: 'W3C Proposed Recommendation'
summary: 'Deletes a database with the specified name.'
tags:
  - API_Object_Methods
  - API
  - IndexedDB
uri: apis/indexeddb/IDBFactory/deleteDatabase

---
## Summary

Deletes a database with the specified name.

Method of [apis/indexeddb/IDBFactory](/apis/indexeddb/IDBFactory)[apis/indexeddb/IDBFactory](/apis/indexeddb/IDBFactory)

## Syntax

``` js
var dbOpenRequest = window.indexeddb.deleteDatabase(name);
```

## Parameters

### name

 Data-type
:   String

 The name of the database to delete.

## Return Value

Returns an object of type DOM NodeDOM Node

An **IDBOpenRequest** request object that fires events to indicate the result of the request.

## Examples

Delete a database

``` js
var dbDeleteRequest = window.indexedDB.deleteDatabase("BookShop1");
  dbDeleteRequest.onsuccess = function(e){
    write("Database successfully deleted");

  };

  dbDeleteRequest.onerror = function(e){
    write("Error deleting DB");
  };
  dbDeleteRequest.onblocked = function(e){
    write("Deleting DB Blocked");
  };
```

[View live example](http://nparashuram.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=#deleteDB&)

## Related specifications

[W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation
