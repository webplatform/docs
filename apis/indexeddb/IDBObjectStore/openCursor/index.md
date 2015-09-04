---
title: openCursor
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
readiness: 'In Progress'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'Creates a cursor.'
uri: apis/indexeddb/IDBObjectStore/openCursor

---
# openCursor

## Summary

Creates a cursor.

*Method of [apis/indexeddb/IDBObjectStore](/apis/indexeddb/IDBObjectStore)*

## Syntax

``` {.js}
var object = object.openCursor(range, direction);
```

## Parameters

### range

 Data-type�
:   Blob

 A key range limiting the cursor to a specific set of values.

### direction

 Data-type�
:   Blob

 Indicates the direction of traversal and whether duplicate values are included.

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
**name**: DataError

</dt>
</dl>
</dt>
<dd>
The values **range** parameter are not valid for the data source.

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
The object store has been deleted or is otherwise unavailable.

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

