---
title: 'IDBIndex'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Proposed Recommendation'
summary: 'A metadata index to a referenced object store.'
tags:
  - API_Objects
  - API
  - IndexedDB
uri: apis/indexeddb/IDBIndex

---
## Summary

A metadata index to a referenced object store.

## Properties

[keyPath](/apis/indexeddb/IDBIndex/keyPath)
:   The key path of this index. If null, this index is not auto-populated.

[multiEntry](/apis/indexeddb/IDBIndex/multiEntry)
:   Affects how the index behaves when the result of evaluating the index's key path yields an array. If true, there is one record in the index for each item in an array of keys. If false, then there is one record for each key that is an array.

[name](/apis/indexeddb/IDBIndex/name)
:   The name of this index.

[objectStore](/apis/indexeddb/IDBIndex/objectStore)
:   Returns a reference to the IDBObjectStore instance for the referenced object store in this IDBIndex's transaction.

[unique](/apis/indexeddb/IDBIndex/unique)
:   Provides the unique flag of this index.

## Methods

[count](/apis/indexeddb/IDBIndex/count)
:   Runs the steps for asynchronously executing a request and returns the IDBRequest created by these steps.

[get](/apis/indexeddb/IDBIndex/get)
:   Runs the steps for asynchronously executing a request and returns the IDBRequest created by these steps.

[openCursor](/apis/indexeddb/IDBIndex/openCursor)
:   Creates a cursor.

[openKeyCursor](/apis/indexeddb/IDBIndex/openKeyCursor)
:   Creates a cursor.

## Events

*No events.*

## Related specifications

[W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation
