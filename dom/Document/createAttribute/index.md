---
title: 'createAttribute'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Could use a more detailed summmary'
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
summary: "Creates an attribute object\_with a specified name."
tags:
  - API_Object_Methods
  - DOM
uri: dom/Document/createAttribute

---
## Summary

Creates an attribute object with a specified name.

Method of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

``` js
var attribute = document.createAttribute(name);
```

## Parameters

### name

 Data-type
:   String

 The name of the attribute.

## Return Value

Returns an object of type DOM NodeDOM Node

The created attribute node.

## Examples

``` js
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

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
