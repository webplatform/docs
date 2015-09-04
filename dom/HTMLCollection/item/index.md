---
title: item
tags:
  - API
  - Object
  - Methods
  - DOM
  - HTML
  - JavaScript
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs example, spec reference'
summary: 'Retrieves a node specified by ordinal index. Nodes are numbered in tree order (depth-first traversal order).'
uri: dom/HTMLCollection/item

---
# item

## Summary

Retrieves a node specified by ordinal index. Nodes are numbered in tree order (depth-first traversal order).

*Method of [dom/HTMLCollection](/dom/HTMLCollection)*

## Syntax

``` {.js}
var node = collection.item(index);
```

## Parameters

### index

 Data-typeÂ
:   unsigned long

 The index of the node to be fetched. The index origin is 0.

## Return Value

Returns an object of type DOM Node.

The **Node** at the corresponding position upon success. A value of **null** is returned if the index is out of range.

**Needs Examples**: This section should include examples.

