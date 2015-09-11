---
title: IDBTransaction
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Proposed Recommendation'
summary: 'Provides for the scope and type of access to a database, and represents a transaction on the database.'
tags:
  0: API
  1: Objects
  3: IndexedDB
uri: apis/indexeddb/IDBTransaction

---
## <span>Summary</span>

Provides for the scope and type of access to a database, and represents a transaction on the database.

## <span>Properties</span>

API Name
:   Summary

[db](/apis/indexeddb/IDBTransaction/db)
:   The database connection of which this transaction is a part.

[error](/apis/indexeddb/IDBTransaction/error)
:   Null if the transaction is not finished, is finished and successfully committed, or was aborted with the abort() function. Returns the same DOMError as the request object which caused the transaction to be aborted due to a failed request, or a DOMError for the transaction failure not due to a failed request (such as QuotaExceededError or UnknownError).

[mode](/apis/indexeddb/IDBTransaction/mode)
:   The mode for isolating access to data in the object stores that are in the scope of the transaction. For possible values, see Return Value, below. The default value is readonly.

[onabort](/apis/indexeddb/IDBTransaction/onabort)
:   The event handler for the onabort event.

[oncomplete](/apis/indexeddb/IDBTransaction/oncomplete)
:   The event handler for the oncomplete event.

[onerror](/apis/indexeddb/IDBTransaction/onerror)
:   The event handler for the error event.

## <span>Methods</span>

API Name
:   Summary

[abort](/apis/indexeddb/IDBTransaction/abort)
:   The abort method is used to abort a transaction. Once called, the abort method follows the [steps to abort](http://www.w3.org/TR/IndexedDB/#dfn-steps-for-aborting-a-transaction) a transaction

[objectStore](/apis/indexeddb/IDBTransaction/objectStore)
:   Returns an object store that has already been added to the scope of this transaction.

## <span>Events</span>

*No events.*

## <span>Related specifications</span>

[W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation
