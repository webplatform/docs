---
title: 'item'
notes:
  - 'Needs example, spec reference'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/HTMLCollection
    href: /dom/HTMLCollection
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/HTMLCollection
standardization_status: 'W3C Recommendation'
summary: 'Retrieves a node specified by ordinal index. Nodes are numbered in tree order (depth-first traversal order).'
tags:
  - API
  - Object
  - Methods
  - DOM
  - HTML
  - JavaScript
uri: dom/HTMLCollection/item

---
## Summary

Retrieves a node specified by ordinal index. Nodes are numbered in tree order (depth-first traversal order).

Method of [dom/HTMLCollection](/dom/HTMLCollection)[dom/HTMLCollection](/dom/HTMLCollection)

## Syntax

``` js
var node = collection.item(index);
```

## Parameters

### index

 Data-type
:   unsigned long

 The index of the node to be fetched. The index origin is 0.

## Return Value

Returns an object of type DOM NodeDOM Node

The **Node** at the corresponding position upon success. A value of **null** is returned if the index is out of range.

**Needs Examples**: This section should include examples.

