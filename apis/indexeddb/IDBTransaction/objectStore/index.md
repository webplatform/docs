---
title: objectStore
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
readiness: 'In Progress'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'Returns an object store that has already been added to the scope of this transaction.'
uri: apis/indexeddb/IDBTransaction/objectStore
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/indexedDB/IDBTransaction

---
# objectStore

## Summary

Returns an object store that has already been added to the scope of this transaction.

*Method of [apis/indexeddb/IDBTransaction](/apis/indexeddb/IDBTransaction)*

## Syntax

``` {.js}
var object = object.objectStore(name);
```

## Parameters

### name

 Data-typeÂ
:   any

 Name of the object store to return.

## Return Value

Returns an object of type DOM Node.

**Needs Examples**: This section should include examples.

## Notes

### Remarks

This method can throw the following [**DOMException**](/dom/DOMException) exceptions: {

### Syntax

### Standards information

-   [Indexed Database API](http://go.microsoft.com/fwlink/p/?LinkId=224519)

## See also

### Related pages (MSDN)

-   `IDBTransaction`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

