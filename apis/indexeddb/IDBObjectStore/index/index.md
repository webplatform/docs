---
title: index
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
readiness: 'In Progress'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'Returns an IDBIndex representing an index that is part of the object store.'
uri: apis/indexeddb/IDBObjectStore/index

---
# index

## Summary

Returns an IDBIndex representing an index that is part of the object store.

*Method of [apis/indexeddb/IDBObjectStore](/apis/indexeddb/IDBObjectStore)*

## Syntax

``` {.js}
var object = object.index(name);
```

## Parameters

### name

 Data-type�
:   Blob

 Name of the index to be retrieved.

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
**name**: NotFoundError

</dt>
<dt>
**code**: DOMException.NOT\_FOUND\_ERR (8)

</dt>
</dl>
</dt>
<dd>
The specified index was not found in the database (case-sensitive).

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
The data source has been deleted or removed.

</dd>
</dl>
  **Note**  As of Internet Explorer 10, the **code** property is deprecated in favor of the **name** property, which is preferred for standards compliance and future compatibility.

### Syntax

### Standards information

-   [Indexed Database API](http://go.microsoft.com/fwlink/p/?LinkId=224519)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

