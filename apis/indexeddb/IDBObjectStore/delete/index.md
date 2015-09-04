---
title: delete
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
readiness: 'Ready to Use'
standardization_status: 'W3C Proposed Recommendation'
summary: 'Removes a record from the specified Object Store.'
code_samples:
  - 'http://nparashuram.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=Delete%20Data&'
uri: apis/indexeddb/IDBObjectStore/delete

---
# delete

## Summary

Removes a record from the specified Object Store.

*Method of [apis/indexeddb/IDBObjectStore](/apis/indexeddb/IDBObjectStore)*

## Syntax

``` {.js}
var idbRequest = objectStore.delete(key);
```

## Parameters

### key

 Data-typeÂ
:   String

 Key identifying the record to be deleted

## Return Value

Returns an object of type DOM Node.

Returns an IDBRequest Object

## Examples

``` {.js}
store = db.createObjectStore("store1", { autoIncrement: true });
store.put("a"); // Will get key 1
store.delete(1);
store.put("b"); // Will get key 2
store.clear();
store.put("c"); // Will get key 3
store.delete(IDBKeyRange.lowerBound(0));
```

[View live example](http://nparashuram.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=Delete%20Data&)

## Notes

### Remarks

This method can throw the following [**DOMException**](/dom/DOMException) exceptions:

<dl data-table="wikitable">
<dt>
**Exception properties**

</dt>
<dd>
**Description**

</dd>
<dt>
<dl>

<dt>
**name**: ReadOnlyError

</dt>
</dl>
</dt>
<dd>
The associated transaction is read-only.

</dd>
<dt>
<dl>

<dt>
**name**: TransactionInactiveError

</dt>
</dl>
</dt>
<dd>
The associated transaction is not active.

</dd>
</dl>

## Related specifications

Specification
:   Status
[W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

