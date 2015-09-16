---
title: 'index'
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
summary: 'Returns an IDBIndex representing an index that is part of the object store.'
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
uri: apis/indexeddb/IDBObjectStore/index

---
## Summary

Returns an IDBIndex representing an index that is part of the object store.

Method of [apis/indexeddb/IDBObjectStore](/apis/indexeddb/IDBObjectStore)[apis/indexeddb/IDBObjectStore](/apis/indexeddb/IDBObjectStore)

## Syntax

``` js
var object = object.index(name);
```

## Parameters

### name

 Data-type
:   Blob

 Name of the index to be retrieved.

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
<strong>name</strong>: NotFoundError
</dt>
<dt>
<strong>code</strong>: DOMException.NOT_FOUND_ERR (8)
</dt>
</dl></td>
<td align="left">The specified index was not found in the database (case-sensitive).</td>
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
<td align="left">The data source has been deleted or removed.</td>
</tr>
</tbody>
</table>

  **Note**  As of Internet Explorer 10, the **code** property is deprecated in favor of the **name** property, which is preferred for standards compliance and future compatibility.

### Syntax

### Standards information

-   [Indexed Database API](http://go.microsoft.com/fwlink/p/?LinkId=224519)
