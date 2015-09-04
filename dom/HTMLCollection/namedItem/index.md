---
title: namedItem
tags:
  - API
  - Object
  - Methods
  - DOM
  - HTML
  - JavaScript
readiness: 'In Progress'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'This method retrieves a Node using a name. With HTML 4.01 documents, it first searches for a Node with a matching id attribute. If it doesn''t find one, it then searches for a Node with a matching name attribute, but only on those elements that are allowed a name attribute. With XHTML 1.0 documents, this method only searches for Nodes with a matching id attribute. This method is case insensitive in HTML documents and case sensitive in XHTML documents.'
uri: dom/HTMLCollection/namedItem

---
# namedItem

## Summary

This method retrieves a Node using a name. With HTML 4.01 documents, it first searches for a Node with a matching id attribute. If it doesn't find one, it then searches for a Node with a matching name attribute, but only on those elements that are allowed a name attribute. With XHTML 1.0 documents, this method only searches for Nodes with a matching id attribute. This method is case insensitive in HTML documents and case sensitive in XHTML documents.

*Method of [dom/HTMLCollection](/dom/HTMLCollection)*

## Syntax

``` {.js}
var item = collection.namedItem(name);
```

## Parameters

### name

 Data-typeÂ
:   String

 The name of the Node to be fetched.

## Return Value

Returns an object of type DOM Node.

The **Node** with a **name** or **id** attribute whose value corresponds to the specified string. Upon failure (e.g., no node with this name exists), returns **null**.

**Needs Examples**: This section should include examples.

