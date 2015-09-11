---
title: setVersion
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Deletion candidate. Not in spec: http://www.w3.org/TR/IndexedDB/'
readiness: 'Not Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/indexeddb/IDBDatabase
    href: /apis/indexeddb/IDBDatabase
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /apis/indexeddb/IDBDatabase
summary: 'Deletion candidate. Not in spec: http://www.w3.org/TR/IndexedDB/'
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/indexedDB/methods/open
    - apis/indexedDB/properties/indexedDB
    - apis/indexedDB/events/onupgradeneeded
    - apis/indexedDB/IDBDatabase
uri: apis/indexeddb/IDBDatabase/setVersion

---
## <span>Summary</span>

Deletion candidate. Not in spec: http://www.w3.org/TR/IndexedDB/

Method of [apis/indexeddb/IDBDatabase](/apis/indexeddb/IDBDatabase)[apis/indexeddb/IDBDatabase](/apis/indexeddb/IDBDatabase)

## <span>Syntax</span>

``` js
var object = object.setVersion(/* see parameter list */);
```

## <span>Parameters</span>

### <span>version</span>

 Data-type
:   Blob

 The new version identifier.

### <span>retVal</span>

 Data-type
:   Blob

 The transaction associated with the VERSION\_CHANGE request.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

This method can return one of these values.

{

**Needs Examples**: This section should include examples.

## <span>Notes</span>

### <span>Remarks</span>

The **setVersion** method was specified by an early draft of the [Indexed Database specification](http://go.microsoft.com/fwlink/p/?LinkID=224519). The method was removed from later drafts of the specification and is no longer supported. To create object stores, indexes, and other IndexedDB objects, use the **version** parameter of the [**open**](/w/index.php?title=apis/indexedDB/methods/open&action=edit&redlink=1) method of the [**indexedDB**](/w/index.php?title=apis/indexedDB/properties/indexedDB&action=edit&redlink=1) property to generate an [**onupgradeneeded**](/w/index.php?title=apis/indexedDB/events/onupgradeneeded&action=edit&redlink=1) event.

### <span>Syntax</span>

### <span>Standards information</span>

-   [Indexed Database API](http://go.microsoft.com/fwlink/p/?LinkId=224519)

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `IDBDatabase`
-   `onupgradeneeded`
-   `open`
