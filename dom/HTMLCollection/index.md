---
title: 'HTMLCollection'
notes:
  - 'Needs spec reference'
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
summary: "An HTMLCollection is a list of nodes. An individual node may be accessed either by its ordinal index or by the node's name or id attributes.\n"
tags:
  - API_Objects
  - DOM
  - HTML
  - JavaScript
uri: dom/HTMLCollection

---
## Summary

An HTMLCollection is a list of nodes. An individual node may be accessed either by its ordinal index or by the node's name or id attributes.

Note that collections in the HTML DOM are assumed to be live, which means that they are automatically updated when the underlying document is changed.

## Properties

[length](/dom/HTMLCollection/length)
:   The length or size of the list.

## Methods

[item](/dom/HTMLCollection/item)
:   Retrieves a node specified by ordinal index. Nodes are numbered in tree order (depth-first traversal order).

[namedItem](/dom/HTMLCollection/namedItem)
:   This method retrieves a **Node** using a name. With HTML 4.01 documents, it first searches for a **Node** with a matching **id** attribute. If it doesn't find one, it then searches for a **Node** with a matching **name** attribute, but only on those elements that are allowed a **name** attribute. With XHTML 1.0 documents, this method only searches for **Nodes** with a matching **id** attribute. This method is case insensitive in HTML documents and case sensitive in XHTML documents.

## Events

*No events.*
