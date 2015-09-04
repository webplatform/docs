---
title: upperBound
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
readiness: 'In Progress'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'Creates and returns a new key range with lower set to undefined, lowerOpen set to true, upper set to upper and and upperOpen set to open.'
uri: apis/indexeddb/IDBKeyRange/upperBound

---
# upperBound

## Summary

Creates and returns a new key range with lower set to undefined, lowerOpen set to true, upper set to upper and and upperOpen set to open.

*Method of [apis/indexeddb/IDBKeyRange](/apis/indexeddb/IDBKeyRange)*

## Syntax

``` {.js}
var object = object.upperBound(bound, open);
```

## Parameters

### bound

 Data-typeÂ
:   Blob

 The upper value of the key range.

### open

 Data-typeÂ
:   Boolean

 Indicates whether the key range includes the **bound** value.

## Return Value

Returns an object of type DOM Node.

**Needs Examples**: This section should include examples.

### Syntax

### Standards information

-   [Indexed Database API](http://go.microsoft.com/fwlink/p/?LinkId=224519)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

