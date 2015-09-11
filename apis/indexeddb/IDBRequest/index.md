---
title: IDBRequest
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Proposed Recommendation'
summary: 'Provides access to the result of a request on the database.'
tags:
  0: API
  1: Objects
  3: IndexedDB
uri: apis/indexeddb/IDBRequest

---
## <span>Summary</span>

Provides access to the result of a request on the database.

## <span>Properties</span>

API Name
:   Summary

[error](/apis/indexeddb/IDBRequest/error)
:   The error codes returned under certain conditions.

[onerror](/apis/indexeddb/IDBRequest/onerror)
:   The event handler for the error event.

[onsuccess](/apis/indexeddb/IDBRequest/onsuccess)
:   The event handler for the success event.

[readyState](/apis/indexeddb/IDBRequest/readyState)
:   The state of the request. Every request starts in the pending state. The state changes to done when the request completes successfully or when an error occurs.

[result](/apis/indexeddb/IDBRequest/result)
:   Returns the result of the request. If the the request failed and the result is not available, the DOMException InvalidStateError exception is thrown.

[source](/apis/indexeddb/IDBRequest/source)
:   The source of the request, such as an Index or a ObjectStore. If no source exists (such as when calling indexedDB.open()), it returns null.

[transaction](/apis/indexeddb/IDBRequest/transaction)
:   The transaction for the request. This property can be null for certain requests, such as for request returned from IDBFactory.open (You're just connecting to a database, so there is no transaction to return).

## <span>Methods</span>

*No methods.*

## <span>Events</span>

*No events.*

## <span>Related specifications</span>

[W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation
