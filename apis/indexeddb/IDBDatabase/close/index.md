---
title: 'close'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://axemclion.github.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=Close%20Database&'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/indexeddb/IDBDatabase
    href: /apis/indexeddb/IDBDatabase
standardization_status: 'W3C Proposed Recommendation'
summary: 'This method synchronously performs the steps for closing a database connection and returns once the database has been closed.'
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
uri: apis/indexeddb/IDBDatabase/close

---
## Summary

This method synchronously performs the steps for closing a database connection and returns once the database has been closed.

Method of [apis/indexeddb/IDBDatabase](/apis/indexeddb/IDBDatabase)[apis/indexeddb/IDBDatabase](/apis/indexeddb/IDBDatabase)

## Syntax

``` js
 database.close();
```

## Return Value

No return value

## Examples

``` js
var dbOpenRequest = window.indexedDB.open("BookShop1");
dbOpenRequest.onsuccess = function(event){
    var db = dbOpenRequest.result;
    // The database is now opened
    db.close(); // Close the database connection
};
```

[View live example](http://axemclion.github.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=Close%20Database&)

## Usage

     This is a synchronous method that returns after the connection to the database is closed.

## Related specifications

[W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation
