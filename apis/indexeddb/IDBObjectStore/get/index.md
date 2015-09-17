---
title: 'get'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/indexeddb/IDBObjectStore
    href: /apis/indexeddb/IDBObjectStore
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /apis/indexeddb/IDBObjectStore
summary: 'Runs the steps for asynchronously executing a request and returns the IDBRequest created by these steps.'
tags:
  - API_Object_Methods
  - API
  - IndexedDB
  - Needs_Examples
uri: apis/indexeddb/IDBObjectStore/get

---
## Summary

Runs the steps for asynchronously executing a request and returns the IDBRequest created by these steps.

Method of [apis/indexeddb/IDBObjectStore](/apis/indexeddb/IDBObjectStore)[apis/indexeddb/IDBObjectStore](/apis/indexeddb/IDBObjectStore)

## Syntax

``` js
var object = object.get(key);
```

## Parameters

### key

 Data-type
:   Blob

 The key value of the record to be retrieved.

## Return Value

Returns an object of type DOM NodeDOM Node

## Notes

### Remarks

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
<strong>name</strong>: DataError
</dt>
</dl></td>
<td align="left">The <strong>key</strong> parameter value is not valid.</td>
</tr>
<tr class="odd">
<td align="left"><dl>
<p></p>
<dt>
<strong>name</strong>: InvalidStateError
</dt>
<dt>
<strong>code</strong>: DOMException.INVALID_STATE_ERR (11)
</dt>
</dl></td>
<td align="left">The object store has been deleted or is otherwise unavailable.</td>
</tr>
<tr class="even">
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

  **Note**  As of Internet Explorer 10, the **code** property is deprecated in favor of the **name** property, which is preferred for standards compliance and future compatibility.

### Syntax

### Standards information

-   [Indexed Database API](http://go.microsoft.com/fwlink/p/?LinkId=224519)
