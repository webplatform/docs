---
title: put
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
summary: 'Creates a structured clone of the value parameter.'
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
uri: apis/indexeddb/IDBObjectStore/put

---
## Summary

Creates a structured clone of the value parameter.

Method of [apis/indexeddb/IDBObjectStore](/apis/indexeddb/IDBObjectStore)[apis/indexeddb/IDBObjectStore](/apis/indexeddb/IDBObjectStore)

## Syntax

``` js
var object = object.put(value, key);
```

## Parameters

### value

 Data-type
:   Blob

 An object literal containing the values to be stored in the object store.

### key

 Data-type
:   Blob

 The key value of the new record.

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
<strong>name</strong>: DataCloneError
</dt>
<dt>
<strong>code</strong>: DOMException.DATA_CLONE_ERR (25)
</dt>
</dl></td>
<td align="left">The data could not be saved to the object store.</td>
</tr>
<tr class="odd">
<td align="left"><dl>
<p></p>
<dt>
<strong>name</strong>: DataError
</dt>
</dl></td>
<td align="left">The specified <strong>key</strong> value is invalid or the value specified for an indexed attribute is invalid.</td>
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
<td align="left">The object store has been deleted or is otherwise unavailable.</td>
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
