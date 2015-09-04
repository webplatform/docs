---
title: direction
tags:
  0: API
  1: Object
  2: Properties
  4: IndexedDB
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs example, spec reference'
summary: 'Indicates the direction of travel within a cursor.'
uri: apis/indexeddb/IDBCursor/direction

---
# direction

## Summary

Indicates the direction of travel within a cursor.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/indexeddb/IDBCursor](/apis/indexeddb/IDBCursor)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = cursor.direction;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The return value describes the direction of travel and the uniqueness of data within the cursor. It corresponds to one of the following:

 next
:   The cursor is travelling in ascending order and contains all matching records, including duplicate values.
nextunique
:   The cursor is travelling in ascending order and contains just one instance of matching key values.
prev
:   The cursor is travelling in descending order and all matching records, including duplicate values.
prevunique
:   The cursor is travelling in descending order and contains just one instance of matching key values.

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[Indexed Database API](http://www.w3.org/TR/IndexedDB/)
:   Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

