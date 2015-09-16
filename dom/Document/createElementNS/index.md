---
title: 'createElementNS'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Document
    href: /dom/Document
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Document
standardization_status: 'W3C Recommendation'
summary: 'Creates an element from the specified namespace as a stand-alone object (unattached to the DOM).'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Document/createElementNS

---
## Summary

Creates an element from the specified namespace as a stand-alone object (unattached to the DOM).

Method of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

``` js
var element = document.createElementNS(namespace, tagName);
```

## Parameters

### namespace

 Data-type
:   String

 The URI of the desired namespace. This is the actual URI value, *not* the prefix used in the mark-up.

### tagName

 Data-type
:   String

 The name of the desired element.

## Return Value

Returns an object of type DOM NodeDOM Node

The created element.

## Examples

The following code example creates a circle element from the SVG namespace.

``` js
var sNamespace = "http://www.w3.org/2000/svg";
var oCircle = document.createElementNS(sNamespace, "circle");
```

## Notes

The **createElementNS** method is supported only for XML namespaces.

## Related specifications

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
