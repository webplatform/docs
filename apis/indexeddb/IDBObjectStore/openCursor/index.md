---
title: 'openCursor'
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
summary: 'Creates a cursor.'
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
uri: apis/indexeddb/IDBObjectStore/openCursor

---
## Summary

Creates a cursor.

Method of [apis/indexeddb/IDBObjectStore](/apis/indexeddb/IDBObjectStore)[apis/indexeddb/IDBObjectStore](/apis/indexeddb/IDBObjectStore)

## Syntax

``` js
var object = object.openCursor(range, direction);
```

## Parameters

### range

 Data-type
:   Blob

 A key range limiting the cursor to a specific set of values.

### direction

 Data-type
:   Blob

 Indicates the direction of traversal and whether duplicate values are included.

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
<strong>name</strong>: DataError
</dt>
</dl></td>
<td align="left">The values <strong>range</strong> parameter are not valid for the data source.</td>
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
