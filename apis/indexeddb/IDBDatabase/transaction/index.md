---
title: transaction
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
readiness: 'In Progress'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'Execute the steps for creating a transaction in a sychronous fashion.'
uri: apis/indexeddb/IDBDatabase/transaction

---
# transaction

## Summary

Execute the steps for creating a transaction in a sychronous fashion.

*Method of [apis/indexeddb/IDBDatabase](/apis/indexeddb/IDBDatabase)*

## Syntax

``` {.js}
var object = object.transaction(storeNames, mode);
```

## Parameters

### storeNames

 Data-type�
:   Blob

 If specified, defines the names of the object stores included in the transaction. Use a **DOMString** to specify a single object store or an array of **DOMString** values to specify multiple object stores.

### mode

 Data-type�
:   Blob

 Value Meaning

 readonly

Changes are not allowed in this transaction.

 readwrite

Changes are allowed in this transaction.

 versionchange

Objects in the database can be create

## Return Value

Returns an object of type DOM Node.

**Needs Examples**: This section should include examples.

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
**name**: InvalidAccessError

</dt>
<dt>
**code**: DOMException.INVALID\_ACCESS\_ERR (15)

</dt>
</dl>
</dt>
<dd>
The value of the **storeNames** parameter is blank or otherwise invalid.

</dd>
<dt>
<dl>

<dt>
**name**: InvalidStateError

</dt>
<dt>
**code**: DOMException.INVALID\_STATE\_ERR (11)

</dt>
</dl>
</dt>
<dd>
The database has been closed or a transaction has been requested for an object that has been deleted or is otherwise unavailable.

</dd>
<dt>
<dl>

<dt>
**name**: NotFoundError

</dt>
<dt>
**code**: DOMException.NOT\_FOUND\_ERR (8)

</dt>
</dl>
</dt>
<dd>
A specified object store could not be found in the current database (case-sensitive).

</dd>
<dt>
<dl>

<dt>
**name**: TypeError

</dt>
</dl>
</dt>
<dd>
The value of the **mode** parameter is not supported.

</dd>
</dl>
  **Note**  As of Internet Explorer 10, the **code** property is deprecated in favor of the **name** property, which is preferred for standards compliance and future compatibility.

### Syntax

### Standards information

-   [Indexed Database API](http://go.microsoft.com/fwlink/p/?LinkId=224519)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

