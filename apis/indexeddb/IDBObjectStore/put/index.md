---
title: put
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
readiness: 'In Progress'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'Creates a structured clone of the value parameter.'
uri: apis/indexeddb/IDBObjectStore/put

---
# put

## Summary

Creates a structured clone of the value parameter.

*Method of [apis/indexeddb/IDBObjectStore](/apis/indexeddb/IDBObjectStore)*

## Syntax

``` {.js}
var object = object.put(value, key);
```

## Parameters

### value

 Data-type�
:   Blob

 An object literal containing the values to be stored in the object store.

### key

 Data-type�
:   Blob

 The key value of the new record.

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
**name**: DataCloneError

</dt>
<dt>
**code**: DOMException.DATA\_CLONE\_ERR (25)

</dt>
</dl>
</dt>
<dd>
The data could not be saved to the object store.

</dd>
<dt>
<dl>

<dt>
**name**: DataError

</dt>
</dl>
</dt>
<dd>
The specified **key** value is invalid or the value specified for an indexed attribute is invalid.

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

