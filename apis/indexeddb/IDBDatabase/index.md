---
title: IDBDatabase
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Proposed Recommendation'
summary: 'Represents a database connection for the purpose of conducting a transaction.'
tags:
  0: API
  1: Objects
  3: IndexedDB
uri: apis/indexeddb/IDBDatabase

---
## Summary

Represents a database connection for the purpose of conducting a transaction.

## Properties

API Name
:   Summary

[name](/apis/indexeddb/IDBDatabase/name)
:   Name of the connected database.

[objectStoreNames](/apis/indexeddb/IDBDatabase/objectStoreNames)
:   Returns a list of names of the object stores currently in the connected database.

[version](/apis/indexeddb/IDBDatabase/version)
:   Returns the version of the database when this IDBDatabaseSync instance was created.

## Methods

API Name
:   Summary

[close](/apis/indexeddb/IDBDatabase/close)
:   This method synchronously performs the steps for closing a database connection and returns once the database has been closed.

[createObjectStore](/apis/indexeddb/IDBDatabase/createObjectStore)
:   The createObjectStore method enables you to create object stores inside an indexedDB database. The creation of an object store is only possible inside a "versionchange" transaction.

[deleteObjectStore](/apis/indexeddb/IDBDatabase/deleteObjectStore)
:   Destroys an object store with the given name as well as all indexes that are referencing that object store.

[setVersion](/apis/indexeddb/IDBDatabase/setVersion)
:   Deletion candidate. Not in spec: <http://www.w3.org/TR/IndexedDB/>

[transaction](/apis/indexeddb/IDBDatabase/transaction)
:   Execute the steps for creating a transaction in a sychronous fashion.

## Events

*No events.*

## Related specifications

[W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation
