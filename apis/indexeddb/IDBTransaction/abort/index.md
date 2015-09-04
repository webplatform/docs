---
title: abort
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
readiness: 'Ready to Use'
standardization_status: 'W3C Proposed Recommendation'
summary: 'The abort method is used to abort a transaction. Once called, the abort method follows the steps to abort a transaction'
code_samples:
  - 'http://axemclion.github.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=Abort%20Transaction&'
uri: apis/indexeddb/IDBTransaction/abort

---
# abort

## Summary

The abort method is used to abort a transaction. Once called, the abort method follows the steps to abort a transaction

*Method of [apis/indexeddb/IDBTransaction](/apis/indexeddb/IDBTransaction)*

## Syntax

``` {.js}
 transaction.abort();
```

## Return Value

No return value

## Examples

``` {.js}
var dbOpenRequest = window.indexedDB.open("BookShop1");
dbOpenRequest.onsuccess = function (event) {
    var db = dbOpenRequest.result;
    try {
        var transaction = db.transaction(["ObjectStore_BookList"], IDBTransaction.READ_WRITE);

        // Now that the transaction is created, lets abort it !!
        transaction.abort();
    } catch (e) {
        write("Could not open transaction");
    }
};
```

[View live example](http://axemclion.github.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=Abort%20Transaction&)

## Usage

     If the transaction is finished, a DOMException of type InvalidStateError is thrown. Otherwise, the steps to abort a transactions are run.

## Related specifications

Specification
:   Status
[W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

