---
title: IDBCursor
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Proposed Recommendation'
summary: 'Iterates over object stores and indices.'
tags:
  0: API
  1: Objects
  3: IndexedDB
uri: apis/indexeddb/IDBCursor

---
## <span>Summary</span>

Iterates over object stores and indices.

## <span>Properties</span>

API Name
:   Summary

[direction](/apis/indexeddb/IDBCursor/direction)
:   Indicates the direction of travel within a cursor.

[key](/apis/indexeddb/IDBCursor/key)
:   The key value for the record currently displayed by the cursor.

[primaryKey](/apis/indexeddb/IDBCursor/primaryKey)
:   Returns the cursor's current effective key.

[source](/apis/indexeddb/IDBCursor/source)
:   On getting, returns the IDBObjectStore or IDBIndex that the cursor is iterating. This function never returns null or throws an exception, even if the cursor is currently being iterated, has iterated past its end, or its transaction is not active.

## <span>Methods</span>

API Name
:   Summary

[advance](/apis/indexeddb/IDBCursor/advance)
:   Advances the cursor by the specified number of records.

[continue](/apis/indexeddb/IDBCursor/continue)
:   Moves to the next record, or to the record specified by a key.

[delete](/apis/indexeddb/IDBCursor/delete)
:   Returns an IDBRequest object and, in a separate thread, deletes the record at the cursor's position, without changing the cursor's position. Once the record is deleted, the cursor's value is set to null.

[update](/apis/indexeddb/IDBCursor/update)
:   Creates a structured clone of the value parameter.

## <span>Events</span>

*No events.*

## <span>Related specifications</span>

[W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation
