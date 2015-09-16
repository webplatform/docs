---
title: 'lower'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/indexeddb/IDBKeyRange
    href: /apis/indexeddb/IDBKeyRange
summary: 'This value is the lower-bound of the key range.'
tags:
  0: API
  1: Object
  2: Properties
  4: IndexedDB
uri: apis/indexeddb/IDBKeyRange/lower

---
## Summary

This value is the lower-bound of the key range.

Property of [apis/indexeddb/IDBKeyRange](/apis/indexeddb/IDBKeyRange)[apis/indexeddb/IDBKeyRange](/apis/indexeddb/IDBKeyRange)

## Syntax

``` js
var result = element.lower;
element.lower = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

A key range is said to be *open* if the lower bound value is included in the range and *closed* if the range does not include the lower bound value. Use the [**lowerOpen**](/apis/indexeddb/IDBKeyRange/lowerOpen) property to determine if the lower value is open or closed.

### Syntax

### Standards information

-   [Indexed Database API](http://go.microsoft.com/fwlink/p/?LinkId=224519)
