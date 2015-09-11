---
title: open
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://axemclion.github.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=#db'
  - 'http://axemclion.github.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=#dbVersion&'
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
summary: 'The open method is used to open an IndexedDB database.'
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
uri: apis/indexeddb/IDBFactory/open

---
## <span>Summary</span>

The open method is used to open an IndexedDB database.

Method of [apis/indexeddb/IDBFactory](/apis/indexeddb/IDBFactory)[apis/indexeddb/IDBFactory](/apis/indexeddb/IDBFactory)

## <span>Syntax</span>

``` js
var dbOpenRequest = indexeddb.open(name, version);
```

## <span>Parameters</span>

### <span>name</span>

 Data-type
:   String

 The name of the database to be opened.

### <span>version</span>

 Data-type
:   Number

(Optional)

The version (unsigned long long) for the database

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

An **IDBOpenRequest** request object that fires events to indicate the result of the request.

## <span>Examples</span>

Open a database without a version number

``` js
var dbOpenRequest = window.indexedDB.open("DatabaseName");
  dbOpenRequest.onsuccess = function(event){
var db = dbOpenRequest.result; // This is the database object
};


dbOpenRequest.onerror = function(e){
   // Called when an error occurs
  };
  dbOpenRequest.onblocked = function(e){
    // Called if another transaction is open on the database
  };
```

[View live example](http://axemclion.github.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=#db)

Open a database with a version number that is higher than the existing version number

``` js
// The database is already opened with version 1.
var dbOpenRequest = window.indexedDB.open("DatabaseName", 2);
  dbOpenRequest.onsuccess = function(event){
var db = dbOpenRequest.result; // This is the database object on which various operations can be performed
};

dbOpenRequest.onupgradeneeded = function(e){
   //This occurs when the version specified in the open call is higher that the version of the database. This is the version change transaction.
  };
dbOpenRequest.onerror = function(e){
   // Called when an error occurs
  };
  dbOpenRequest.onblocked = function(e){
    // Called if another transaction is open on the database
  };
```

[View live example](http://axemclion.github.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=#dbVersion&)

## <span>Usage</span>

     var openRequest = window.indexedDB.open("databaseName", 1);

## <span>Notes</span>

The open method either creates a database if it does not exist, or opens one, with the specified version number. If no version number is specified, the database is opened with the current version number. If a database is to be created and a version number is not specified, the database is opened with a version 1.

## <span>Related specifications</span>

[W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation
