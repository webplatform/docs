---
title: transaction
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/indexeddb/IDBDatabase
    href: /apis/indexeddb/IDBDatabase
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /apis/indexeddb/IDBDatabase
summary: 'Execute the steps for creating a transaction in a sychronous fashion.'
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
uri: apis/indexeddb/IDBDatabase/transaction

---
## Summary

Execute the steps for creating a transaction in a sychronous fashion.

Method of [apis/indexeddb/IDBDatabase](/apis/indexeddb/IDBDatabase)[apis/indexeddb/IDBDatabase](/apis/indexeddb/IDBDatabase)

## Syntax

``` js
var object = object.transaction(storeNames, mode);
```

## Parameters

### storeNames

 Data-type
:   Blob

 If specified, defines the names of the object stores included in the transaction. Use a **DOMString** to specify a single object store or an array of **DOMString** values to specify multiple object stores.

### mode

 Data-type
:   Blob

 Value Meaning

 readonly

Changes are not allowed in this transaction.

 readwrite

Changes are allowed in this transaction.

 versionchange

Objects in the database can be create

## Return Value

Returns an object of type DOM NodeDOM Node

**Needs Examples**: This section should include examples.

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
<strong>name</strong>: InvalidAccessError
</dt>
<dt>
<strong>code</strong>: DOMException.INVALID_ACCESS_ERR (15)
</dt>
</dl></td>
<td align="left">The value of the <strong>storeNames</strong> parameter is blank or otherwise invalid.</td>
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
<td align="left">The database has been closed or a transaction has been requested for an object that has been deleted or is otherwise unavailable.</td>
</tr>
<tr class="even">
<td align="left"><dl>
<p></p>
<dt>
<strong>name</strong>: NotFoundError
</dt>
<dt>
<strong>code</strong>: DOMException.NOT_FOUND_ERR (8)
</dt>
</dl></td>
<td align="left">A specified object store could not be found in the current database (case-sensitive).</td>
</tr>
<tr class="odd">
<td align="left"><dl>
<p></p>
<dt>
<strong>name</strong>: TypeError
</dt>
</dl></td>
<td align="left">The value of the <strong>mode</strong> parameter is not supported.</td>
</tr>
</tbody>
</table>

  **Note**  As of Internet Explorer 10, the **code** property is deprecated in favor of the **name** property, which is preferred for standards compliance and future compatibility.

### Syntax

### Standards information

-   [Indexed Database API](http://go.microsoft.com/fwlink/p/?LinkId=224519)
