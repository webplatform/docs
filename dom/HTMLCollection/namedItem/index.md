---
title: 'namedItem'
notes:
  - 'Needs example, spec reference, standardization status'
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
summary: 'This method retrieves a Node using a name. With HTML 4.01 documents, it first searches for a Node with a matching id attribute. If it doesn''t find one, it then searches for a Node with a matching name attribute, but only on those elements that are allowed a name attribute. With XHTML 1.0 documents, this method only searches for Nodes with a matching id attribute. This method is case insensitive in HTML documents and case sensitive in XHTML documents.'
tags:
  - API
  - Object
  - Methods
  - DOM
  - HTML
  - JavaScript
uri: dom/HTMLCollection/namedItem

---
## Summary

This method retrieves a Node using a name. With HTML 4.01 documents, it first searches for a Node with a matching id attribute. If it doesn't find one, it then searches for a Node with a matching name attribute, but only on those elements that are allowed a name attribute. With XHTML 1.0 documents, this method only searches for Nodes with a matching id attribute. This method is case insensitive in HTML documents and case sensitive in XHTML documents.

Method of [dom/HTMLCollection](/dom/HTMLCollection)[dom/HTMLCollection](/dom/HTMLCollection)

## Syntax

``` js
var item = collection.namedItem(name);
```

## Parameters

### name

 Data-type
:   String

 The name of the Node to be fetched.

## Return Value

Returns an object of type DOM NodeDOM Node

The **Node** with a **name** or **id** attribute whose value corresponds to the specified string. Upon failure (e.g., no node with this name exists), returns **null**.

**Needs Examples**: This section should include examples.

