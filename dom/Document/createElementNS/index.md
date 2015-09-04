---
title: createElementNS
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
summary: 'Creates an element from the specified namespace as a stand-alone object (unattached to the DOM).'
uri: dom/Document/createElementNS

---
# createElementNS

## Summary

Creates an element from the specified namespace as a stand-alone object (unattached to the DOM).

*Method of [dom/Document](/dom/Document)*

## Syntax

``` {.js}
var element = document.createElementNS(namespace, tagName);
```

## Parameters

### namespace

 Data-typeÂ
:   String

 The URI of the desired namespace. This is the actual URI value, *not* the prefix used in the mark-up.

### tagName

 Data-typeÂ
:   String

 The name of the desired element.

## Return Value

Returns an object of type DOM Node.

The created element.

## Examples

The following code example creates a circle element from the SVG namespace.

``` {.js}
var sNamespace = "http://www.w3.org/2000/svg";
var oCircle = document.createElementNS(sNamespace, "circle");
```

## Notes

The **createElementNS** method is supported only for XML namespaces.

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

