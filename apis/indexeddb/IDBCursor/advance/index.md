---
title: advance
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
readiness: 'Ready to Use'
standardization_status: 'W3C Proposed Recommendation'
summary: 'Advances the cursor by the specified number of records.'
code_samples:
  - 'http://axemclion.github.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=Advance%20cursor&'
uri: apis/indexeddb/IDBCursor/advance

---
# advance

## Summary

Advances the cursor by the specified number of records.

*Method of [apis/indexeddb/IDBCursor](/apis/indexeddb/IDBCursor)*

## Syntax

``` {.js}
 cursor.advance(count);
```

## Parameters

### count

 Data-typeÂ
:   Number

 A positive, non-zero integer value indicating the number of records to advance.

## Return Value

No return value

## Examples

``` {.js}
var dbOpenRequest = window.indexedDB.open("BookShop1");
dbOpenRequest.onsuccess = function(event){
    var transaction = dbOpenRequest.result.transaction(["ObjectStore_BookList"], IDBTransaction.READ_WRITE);
    var objectStore = transaction.objectStore("ObjectStore_BookList");
    // Function to call when a new cursor is required
    var cursor = null;
    var request = objectStore.openCursor(IDBKeyRange.bound(0, new Date().getTime(), true, false), 1);
    request.onsuccess = function(event){
        cursor = request.result;
        write("Cursor opened", cursor);

        if (cursor) {
            write("Value in cursor now is ", cursor.key, cursor.value);
            cursor.advance(2); // jump 2 entries
        }

    };
};
```

[View live example](http://axemclion.github.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=Advance%20cursor&)

## Usage

     Throws an exception if

-   The value passed into the count parameter was zero or a negative number.
-   The transaction this IDBCursor belongs to is not active.
-   The cursor is currently being iterated, or has iterated past its end.

## Notes

Calling this method more than once before new cursor data has been loaded is not allowed and results in a DOMException of type InvalidStateError being thrown. For example, calling advance() twice from the same onsuccess handler results in a DOMException of type InvalidStateError being thrown on the second call.

### Syntax

## Related specifications

Specification
:   Status
[W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

