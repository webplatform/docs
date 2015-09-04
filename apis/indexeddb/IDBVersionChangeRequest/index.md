---
title: IDBVersionChangeRequest
tags:
  0: API
  1: Objects
  3: IndexedDB
readiness: 'Out of Date'
standardization_status: Deprecated
notes:
  - 'Deprecated; no longer in spec'
summary: "Deprecated; no longer in spec. \nUsed to change the version of the database.\n"
uri: apis/indexeddb/IDBVersionChangeRequest
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/indexedDB/methods/setVersion
    - apis/indexedDB/methods/open
    - apis/indexedDB/properties/indexedDB
    - apis/indexedDB/events/onupgradeneeded

---
# IDBVersionChangeRequest

## Summary

Deprecated; no longer in spec. Used to change the version of the database.

## Properties

API Name
:   Summary
[onblocked](/apis/indexeddb/IDBVersionChangeRequest/onblocked)
:   The event handler for the blocked event.

## Methods

*No methods.*

## Events

*No events.*

## Notes

### Remarks

The **IDBVersionChangeRequest** object was returned by the [**setVersion**](/w/index.php?title=apis/indexedDB/methods/setVersion&action=edit&redlink=1) method, as specified by an early draft of the [Indexed Database specification](http://go.microsoft.com/fwlink/p/?LinkID=224519). The object and method were removed from later drafts of the specification and are no longer supported. To create object stores, indexes, and other IndexedDB objects, use the **version** parameter of the [**open**](/w/index.php?title=apis/indexedDB/methods/open&action=edit&redlink=1) method of the [**indexedDB**](/w/index.php?title=apis/indexedDB/properties/indexedDB&action=edit&redlink=1) property to generate an [**onupgradeneeded**](/w/index.php?title=apis/indexedDB/events/onupgradeneeded&action=edit&redlink=1) event.

## Related specifications

Specification
:   Status
[W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation

## See also

### Related pages (MSDN)

-   `onupgradeneeded`
-   `open`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

