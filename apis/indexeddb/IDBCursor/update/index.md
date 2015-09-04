---
title: update
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
readiness: 'In Progress'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'Creates a structured clone of the value parameter.'
uri: apis/indexeddb/IDBCursor/update
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/indexedDB/methods/openKeyCursor

---
# update

## Summary

Creates a structured clone of the value parameter.

*Method of [apis/indexeddb/IDBCursor](/apis/indexeddb/IDBCursor)*

## Syntax

``` {.js}
var object = object.update(value);
```

## Parameters

### value

 Data-type�
:   Blob

## Return Value

Returns an object of type DOM Node.

[**IDBRequest**](/apis/indexeddb/IDBRequest)

An object representing the update request.

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
**name**: DataError

</dt>
</dl>
</dt>
<dd>
When an object store uses inline keys, this exception indicates that the key value of the update object does not match the key value of a corresponding record in the object store.

</dd>
<dt>
<dl>

<dt>
**name**: DataCloneError

</dt>
<dt>
**code**: DOMException.DATA\_CLONE\_ERR (25)

</dt>
</dl>
</dt>
<dd>
The data could not be copied.

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
The update is not allowed for one of the following reasons:

-   the cursor was created using [**openKeyCursor**](/w/index.php?title=apis/indexedDB/methods/openKeyCursor&action=edit&redlink=1).
-   the cursor is iterating to a new record.
-   the cursor has moved past the last record.

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
  **Note**  As of Internet Explorer 10, the **code** property is deprecated in favor of the **name** property, which is preferred for standards compliance and future compatibility.

### Syntax

### Standards information

-   [Indexed Database API](http://go.microsoft.com/fwlink/p/?LinkId=224519)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

