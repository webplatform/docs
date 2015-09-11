---
title: direction
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example, spec reference'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/indexeddb/IDBCursor
    href: /apis/indexeddb/IDBCursor
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /apis/indexeddb/IDBCursor
standardization_status: 'W3C Working Draft'
summary: 'Indicates the direction of travel within a cursor.'
tags:
  0: API
  1: Object
  2: Properties
  4: IndexedDB
uri: apis/indexeddb/IDBCursor/direction

---
## <span>Summary</span>

Indicates the direction of travel within a cursor.

Property of [apis/indexeddb/IDBCursor](/apis/indexeddb/IDBCursor)[apis/indexeddb/IDBCursor](/apis/indexeddb/IDBCursor)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = cursor.direction;
```

## <span>Return Value</span>

Returns an object of type StringString

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

## <span>Related specifications</span>

[Indexed Database API](http://www.w3.org/TR/IndexedDB/)
:   Working Draft
