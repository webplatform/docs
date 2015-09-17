---
title: 'abort'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://axemclion.github.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=Abort%20Transaction&'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/indexeddb/IDBTransaction
    href: /apis/indexeddb/IDBTransaction
standardization_status: 'W3C Proposed Recommendation'
summary: 'The abort method is used to abort a transaction. Once called, the abort method follows the steps to abort a transaction'
tags:
  - API_Object_Methods
  - API
  - IndexedDB
uri: apis/indexeddb/IDBTransaction/abort

---
## Summary

The abort method is used to abort a transaction. Once called, the abort method follows the steps to abort a transaction

Method of [apis/indexeddb/IDBTransaction](/apis/indexeddb/IDBTransaction)[apis/indexeddb/IDBTransaction](/apis/indexeddb/IDBTransaction)

## Syntax

``` js
 transaction.abort();
```

## Return Value

No return value

## Examples

``` js
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

[W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation
