---
title: deleteObjectStore
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
readiness: 'In Progress'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'Destroys an object store with the given name as well as all indexes that are referencing that object store.'
uri: apis/indexeddb/IDBDatabase/deleteObjectStore

---
# deleteObjectStore

## Summary

Destroys an object store with the given name as well as all indexes that are referencing that object store.

*Method of [apis/indexeddb/IDBDatabase](/apis/indexeddb/IDBDatabase)*

## Syntax

``` {.js}
var object = object.deleteObjectStore(name);
```

## Parameters

### name

 Data-typeÂ
:   Blob

 Name of the object store to be removed.

## Return Value

Returns an object of type DOM Node.

This method can throw the following [**DOMException**](/dom/DOMException) exceptions:

**Note**Â Â As of Internet ExplorerÂ 10, the **code** property is deprecated in lieu of the **name** property, which is preferred for standards compliance and future compatibility.

<dl data-table="wikitable">
<dt>
Exception properties

</dt>
<dd>
Description

</dd>
<dt>
name: InvalidStateError

code: DOMException.INVALID\_STATE\_ERR (11)

</dt>
<dd>
The method was not called within the context of a VERSION\_CHANGE transaction or the request was made for an object that has been moved or deleted.

</dd>
<dt>
name: NotFoundError

code: DOMException.NOT\_FOUND\_ERR (8)

</dt>
<dd>
An object store could not be found with the specified name (case-sensitive).

</dd>
</dl>
Â

**Needs Examples**: This section should include examples.

### Syntax

### Standards information

-   [Indexed Database API](http://go.microsoft.com/fwlink/p/?LinkId=224519)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

