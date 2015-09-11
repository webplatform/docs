---
title: add
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://axemclion.github.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=#saveData&'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/indexeddb/IDBObjectStore
    href: /apis/indexeddb/IDBObjectStore
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /apis/indexeddb/IDBObjectStore
standardization_status: 'W3C Proposed Recommendation'
summary: 'Adds a record to the specified object store.'
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
uri: apis/indexeddb/IDBObjectStore/add

---
## <span>Summary</span>

Adds a record to the specified object store.

Method of [apis/indexeddb/IDBObjectStore](/apis/indexeddb/IDBObjectStore)[apis/indexeddb/IDBObjectStore](/apis/indexeddb/IDBObjectStore)

## <span>Syntax</span>

``` js
var idbRequest = objectStore.add(value, key);
```

## <span>Parameters</span>

### <span>value</span>

 Data-type
:   String

 The value must be valid for the Structured Cloning Algorithm.

### <span>key</span>

 Data-type
:   String

(Optional)

A key must be provided if the Object Store does not have a key path, or a key generator is not specified.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

## <span>Examples</span>

``` js
var dbOpenRequest = window.indexedDB.open("BookShop1");
dbOpenRequest.onsuccess = function(event){
    var db = dbOpenRequest.result;
    var transaction = db.transaction(["ObjectStore_BookList"], IDBTransaction.READ_WRITE);

    // The object store has a keyPath as "id". Hence no key is specified, but the value has id as a property
    var objectStore = transaction.objectStore("ObjectStore_BookList");

    // Sample data to add to the Object store
    var key = 10;
    var value = {
        "bookName": "Book-" + Math.random(),
        "author": "AuthorName",
        "id": key
    };

    var request = objectStore.add(value);
    request.onsuccess = function(event){
        console.log("Saved id ", request.result);
    };
    request.onerror = function(e){
        console.log("Error adding data")
    };

};
```

[View live example](http://axemclion.github.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=#saveData&)

## <span>Usage</span>

     An error is thrown if one of the following is true

-   The object store uses in-line keys and the key parameter was provided.
-   The object store uses out-of-line keys and has no key generator and the key parameter was not provided.
-   The object store uses in-line keys and the result of evaluating the object store's key path yields a value and that value is not a valid key.
-   The object store uses in-line keys but no key generator and the result of evaluating the object store's key path does not yield a value.
-   The key parameter was provided but does not contain a valid key.

## <span>Notes</span>

### <span>Remarks</span>

This method can throw the following [**DOMException**](/dom/DOMException)

## <span>Related specifications</span>

[W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation
