---
title: delete
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://nparashuram.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=Delete%20Data&'
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
summary: 'Removes a record from the specified Object Store.'
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
uri: apis/indexeddb/IDBObjectStore/delete

---
## <span>Summary</span>

Removes a record from the specified Object Store.

Method of [apis/indexeddb/IDBObjectStore](/apis/indexeddb/IDBObjectStore)[apis/indexeddb/IDBObjectStore](/apis/indexeddb/IDBObjectStore)

## <span>Syntax</span>

``` js
var idbRequest = objectStore.delete(key);
```

## <span>Parameters</span>

### <span>key</span>

 Data-type
:   String

 Key identifying the record to be deleted

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

Returns an IDBRequest Object

## <span>Examples</span>

``` js
store = db.createObjectStore("store1", { autoIncrement: true });
store.put("a"); // Will get key 1
store.delete(1);
store.put("b"); // Will get key 2
store.clear();
store.put("c"); // Will get key 3
store.delete(IDBKeyRange.lowerBound(0));
```

[View live example](http://nparashuram.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=Delete%20Data&)

## <span>Notes</span>

### <span>Remarks</span>

This method can throw the following [**DOMException**](/dom/DOMException) exceptions:

<table>
<col width="50%" />
<col width="50%" />
<tbody>
<tr class="odd">
<td align="left"><strong>Exception properties</strong></td>
<td align="left"><strong>Description</strong></td>
</tr>
<tr class="even">
<td align="left"><dl>
<p></p>
<dt>
<strong>name</strong>: ReadOnlyError
</dt>
</dl></td>
<td align="left">The associated transaction is read-only.</td>
</tr>
<tr class="odd">
<td align="left"><dl>
<p></p>
<dt>
<strong>name</strong>: TransactionInactiveError
</dt>
</dl></td>
<td align="left">The associated transaction is not active.</td>
</tr>
</tbody>
</table>

## <span>Related specifications</span>

[W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation
