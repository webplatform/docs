---
title: 'continue'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://axemclion.github.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=Continue%20with%20cursor&'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/indexeddb/IDBCursor
    href: /apis/indexeddb/IDBCursor
  return_type:
    predicate: 'Returns an object of type  '
    value: Boolean
    href: /apis/indexeddb/IDBCursor
standardization_status: 'W3C Proposed Recommendation'
summary: 'Moves to the next record, or to the record specified by a key.'
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
uri: apis/indexeddb/IDBCursor/continue

---
## Summary

Moves to the next record, or to the record specified by a key.

Method of [apis/indexeddb/IDBCursor](/apis/indexeddb/IDBCursor)[apis/indexeddb/IDBCursor](/apis/indexeddb/IDBCursor)

## Syntax

``` js
var hasMoved = cursor.continue(key);
```

## Parameters

### key

 Data-type
:   String

(Optional)

The next key to position this cursor at.

If the key parameter is specified and fulfills any of these conditions this method must throw a DOMException of type DataError:

-   The parameter is not a valid key.
-   The parameter is less than or equal to this cursor's position and this cursor's direction is "next" or "nextunique".
-   The parameter is greater than or equal to this cursor's position and this cursor's direction is "prev" or "prevunique".

## Return Value

Returns an object of type BooleanBoolean

If the steps for synchronously executing a request returns a cursor, then this function returns true. Otherwise this function returns false.

## Examples

``` js
var tx = db.transaction('Contact');
var store = tx.objectStore('Contact');
var cursor = store.openCursor();
while(cursor.continue()) {
    var value = cursor.value;
    // act on each object or key
}
```

[View live example](http://axemclion.github.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=Continue%20with%20cursor&)

## Usage

     The continue method throws an exception if

-   The transaction this IDBCursor belongs to is not active.
-   The cursor is currently being iterated, or has iterated past its end.
-   The key parameter was specified but did not contain a valid key.

## Related specifications

[W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation
