---
title: 'IDBObjectStore'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Proposed Recommendation'
summary: 'Represents an object store in a database.'
tags:
  - API_Objects
  - API
  - IndexedDB
uri: apis/indexeddb/IDBObjectStore

---
## Summary

Represents an object store in a database.

## Properties

[autoIncrement](/apis/indexeddb/IDBObjectStore/autoIncrement)
:   Provides the auto increment flag for this object store.

[indexNames](/apis/indexeddb/IDBObjectStore/indexNames)
:   Provides a list of the names of indexes on objects in this object store.

[keyPath](/apis/indexeddb/IDBObjectStore/keyPath)
:   Provides the key path of this object store.

[name](/apis/indexeddb/IDBObjectStore/name)
:   Provides the name of this object store.

[transaction](/apis/indexeddb/IDBObjectStore/transaction)
:   Returns the transaction this object store belongs to.

## Methods

[add](/apis/indexeddb/IDBObjectStore/add)
:   Adds a record to the specified object store.

[clear](/apis/indexeddb/IDBObjectStore/clear)
:   Removes all records from the object store.

[count](/apis/indexeddb/IDBObjectStore/count)
:   The count method returns the number of records in an object store.

[createIndex](/apis/indexeddb/IDBObjectStore/createIndex)
:   This method creates and returns a new index with the given name and parameters in the connected database.

[delete](/apis/indexeddb/IDBObjectStore/delete)
:   Removes a record from the specified Object Store.

[deleteIndex](/apis/indexeddb/IDBObjectStore/deleteIndex)
:   This method destroys the index with the given name in the connected database. Note that this method must only be called from a "versionchange" transaction callback.

[get](/apis/indexeddb/IDBObjectStore/get)
:   Runs the steps for asynchronously executing a request and returns the IDBRequest created by these steps.

[index](/apis/indexeddb/IDBObjectStore/index)
:   Returns an IDBIndex representing an index that is part of the object store.

[openCursor](/apis/indexeddb/IDBObjectStore/openCursor)
:   Creates a cursor.

[put](/apis/indexeddb/IDBObjectStore/put)
:   Creates a structured clone of the value parameter.

## Events

*No events.*

## Related specifications

[W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation
