---
title: lowerBound
tags:
  0: API
  1: Object
  2: Methods
  4: IndexedDB
readiness: 'In Progress'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'Creates and returns a new key range with lower set to lower, lowerOpen set to open, upper set to undefined and and upperOpen set to true.'
uri: apis/indexeddb/IDBKeyRange/lowerBound

---
# lowerBound

## Summary

Creates and returns a new key range with lower set to lower, lowerOpen set to open, upper set to undefined and and upperOpen set to true.

*Method of [apis/indexeddb/IDBKeyRange](/apis/indexeddb/IDBKeyRange)*

## Syntax

``` {.js}
var object = object.lowerBound(bound, open);
```

## Parameters

### bound

 Data-typeÂ
:   Blob

 The lower value of the key range.

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

