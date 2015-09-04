---
title: createAttribute
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'Could use a more detailed summmary'
summary: "Creates an attribute object\_with a specified name."
uri: dom/Document/createAttribute

---
# createAttribute

## Summary

Creates an attribute objectÂ with a specified name.

*Method of [dom/Document](/dom/Document)*

## Syntax

``` {.js}
var attribute = document.createAttribute(name);
```

## Parameters

### name

 Data-typeÂ
:   String

 The name of the attribute.

## Return Value

Returns an object of type DOM Node.

The created attribute node.

## Examples

``` {.js}
//create a "style" attribute
var attr = document.createAttribute("style");
//assign a value to the attribute
attr.value = "color: blue";
//apply the attribute to a specific element
document.getElementById("header").setAttributeNode(attr);
```

## Notes

This method will fail if the *name* parameter value contains invalid (non-Unicode Transformation Format (UTF)-16) characters.

This method only creates the attribute in the document; it does not assign a value to the attribute nor assign it to any HTML element(s). See example.

### Standards information

-   [Document Object Model (DOM) Level 3 Core Specification](http://go.microsoft.com/fwlink/p/?linkid=182717), Section 1.4

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

