---
title: objectStore
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/indexeddb/IDBTransaction
    href: /apis/indexeddb/IDBTransaction
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /apis/indexeddb/IDBTransaction
summary: 'Returns an object store that has already been added to the scope of this transaction.'
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/indexedDB/IDBTransaction
uri: apis/indexeddb/IDBTransaction/objectStore

---
## Summary

Returns an object store that has already been added to the scope of this transaction.

Method of [apis/indexeddb/IDBTransaction](/apis/indexeddb/IDBTransaction)[apis/indexeddb/IDBTransaction](/apis/indexeddb/IDBTransaction)

## Syntax

``` js
var object = object.objectStore(name);
```

## Parameters

### name

 Data-type
:   any

 Name of the object store to return.

## Return Value

Returns an object of type DOM NodeDOM Node

**Needs Examples**: This section should include examples.

## Notes

### Remarks

This method can throw the following [**DOMException**](/dom/DOMException) exceptions: {

### Syntax

### Standards information

-   [Indexed Database API](http://go.microsoft.com/fwlink/p/?LinkId=224519)

## See also

### Related pages

-   `IDBTransaction`
