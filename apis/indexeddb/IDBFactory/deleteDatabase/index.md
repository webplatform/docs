---
title: deleteDatabase
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
readiness: 'Ready to Use'
standardization_status: 'W3C Proposed Recommendation'
summary: 'Deletes a database with the specified name.'
code_samples:
  - 'http://nparashuram.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=#deleteDB&'
uri: apis/indexeddb/IDBFactory/deleteDatabase

---
# deleteDatabase

## Summary

Deletes a database with the specified name.

*Method of [apis/indexeddb/IDBFactory](/apis/indexeddb/IDBFactory)*

## Syntax

``` {.js}
var dbOpenRequest = window.indexeddb.deleteDatabase(name);
```

## Parameters

### name

 Data-typeÂ
:   String

 The name of the database to delete.

## Return Value

Returns an object of type DOM Node.

An **IDBOpenRequest** request object that fires events to indicate the result of the request.

## Examples

Delete a database

``` {.js}
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

Specification
:   Status
[W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

