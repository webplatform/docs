---
title: 'update'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/indexeddb/IDBCursor
    href: /apis/indexeddb/IDBCursor
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /apis/indexeddb/IDBCursor
summary: 'Creates a structured clone of the value parameter.'
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/indexedDB/methods/openKeyCursor
uri: apis/indexeddb/IDBCursor/update

---
## Summary

Creates a structured clone of the value parameter.

Method of [apis/indexeddb/IDBCursor](/apis/indexeddb/IDBCursor)[apis/indexeddb/IDBCursor](/apis/indexeddb/IDBCursor)

## Syntax

``` js
var object = object.update(value);
```

## Parameters

### value

 Data-type
:   Blob

## Return Value

Returns an object of type DOM NodeDOM Node

[**IDBRequest**](/apis/indexeddb/IDBRequest)

An object representing the update request.

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
<td align="left">When an object store uses inline keys, this exception indicates that the key value of the update object does not match the key value of a corresponding record in the object store.</td>
</tr>
<tr class="odd">
<td align="left"><dl>
<p></p>
<dt>
<strong>name</strong>: DataCloneError
</dt>
<dt>
<strong>code</strong>: DOMException.DATA_CLONE_ERR (25)
</dt>
</dl></td>
<td align="left">The data could not be copied.</td>
</tr>
<tr class="even">
<td align="left"><dl>
<p></p>
<dt>
<strong>name</strong>: InvalidStateError
</dt>
<dt>
<strong>code</strong>: DOMException.INVALID_STATE_ERR (11)
</dt>
</dl></td>
<td align="left">The update is not allowed for one of the following reasons:
<ul>
<li>the cursor was created using <a href="/w/index.php?title=apis/indexedDB/methods/openKeyCursor&amp;action=edit&amp;redlink=1"><strong>openKeyCursor</strong></a>.</li>
<li>the cursor is iterating to a new record.</li>
<li>the cursor has moved past the last record.</li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><dl>
<p></p>
<dt>
<strong>name</strong>: ReadOnlyError
</dt>
</dl></td>
<td align="left">The associated transaction is read-only.</td>
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
