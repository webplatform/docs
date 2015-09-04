---
title: setVersion
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
readiness: 'Not Ready'
notes:
  - 'Deletion candidate. Not in spec: http://www.w3.org/TR/IndexedDB/'
summary: 'Deletion candidate. Not in spec: http://www.w3.org/TR/IndexedDB/'
uri: apis/indexeddb/IDBDatabase/setVersion
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/indexedDB/methods/open
    - apis/indexedDB/properties/indexedDB
    - apis/indexedDB/events/onupgradeneeded
    - apis/indexedDB/IDBDatabase

---
# setVersion

## Summary

Deletion candidate. Not in spec: http://www.w3.org/TR/IndexedDB/

*Method of [apis/indexeddb/IDBDatabase](/apis/indexeddb/IDBDatabase)*

## Syntax

``` {.js}
var object = object.setVersion(/* see parameter list */);
```

## Parameters

### version

 Data-typeÂ
:   Blob

 The new version identifier.

### retVal

 Data-typeÂ
:   Blob

 The transaction associated with the VERSION\_CHANGE request.

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

This method can return one of these values.

{

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The **setVersion** method was specified by an early draft of the [Indexed Database specification](http://go.microsoft.com/fwlink/p/?LinkID=224519). The method was removed from later drafts of the specification and is no longer supported. To create object stores, indexes, and other IndexedDB objects, use the **version** parameter of the [**open**](/w/index.php?title=apis/indexedDB/methods/open&action=edit&redlink=1) method of the [**indexedDB**](/w/index.php?title=apis/indexedDB/properties/indexedDB&action=edit&redlink=1) property to generate an [**onupgradeneeded**](/w/index.php?title=apis/indexedDB/events/onupgradeneeded&action=edit&redlink=1) event.

### Syntax

### Standards information

-   [Indexed Database API](http://go.microsoft.com/fwlink/p/?LinkId=224519)

## See also

### Related pages (MSDN)

-   `IDBDatabase`
-   `onupgradeneeded`
-   `open`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

