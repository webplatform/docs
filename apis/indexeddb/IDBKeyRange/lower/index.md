---
title: lower
tags:
  0: API
  1: Object
  2: Properties
  4: IndexedDB
readiness: 'In Progress'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'This value is the lower-bound of the key range.'
uri: apis/indexeddb/IDBKeyRange/lower

---
# lower

## Summary

This value is the lower-bound of the key range.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/indexeddb/IDBKeyRange](/apis/indexeddb/IDBKeyRange)</span></span>

## Syntax

``` {.js}
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

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

