---
title: 'IDBOpenDBRequest'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: IDBRequest
    href: /apis/indexeddb/IDBRequest
standardization_status: 'W3C Proposed Recommendation'
summary: 'Provides access to the result of a request to open a database.'
tags:
  0: API
  1: Objects
  3: IndexedDB
uri: apis/indexeddb/IDBOpenDBRequest

---
## Summary

Provides access to the result of a request to open a database.

Inherits from [IDBRequest](/apis/indexeddb/IDBRequest)[IDBRequest](/apis/indexeddb/IDBRequest)

## Properties

API Name
:   Summary

[onUpgradeNeeded](/apis/indexeddb/IDBOpenDBRequest/onUpgradeNeeded)
:   The event handler for the upgrade needed event.

[onblocked](/apis/indexeddb/IDBOpenDBRequest/onblocked)
:   The event handler for the blocked event. This event is triggered when the upgradeneeded should be triggered because of a version change but the database is still in use (ie not closed) somewhere, even after the versionchange event was sent.

## Methods

*No methods.*

## Events

*No events.*

## Inherited from IDBRequest

### Properties

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

### Methods

*No methods.*

### Events

*No events.*

## Notes

### Remarks

The **IDBOpenDBRequest** object is returned by operations that affect database, such [**open**](/apis/indexeddb/IDBFactory/open) and [**deleteDatabase**](/apis/indexeddb/IDBFactory/deleteDatabase).

## Related specifications

[W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation
