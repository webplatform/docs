---
title: 'attributes'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.attributes](https://developer.mozilla.org/en-US/docs/Web/API/Node.attributes) Article]'
  - 'Microsoft Developer Network: [[attributes Collection](http://msdn.microsoft.com/en-us/library/ie/ms537438(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Node
    href: /dom/Node
  return:
    predicate: 'Returns an object of type '
    value: ''
    href: /dom/Node
standardization_status: 'W3C Recommendation'
summary: 'Associatve array containing the attributes of node.'
tags:
  - API_Object_Properties
  - DOM
uri: dom/Node/attributes

---
## Summary

Associatve array containing the attributes of node.

Property of [dom/Node](/dom/Node)[dom/Node](/dom/Node)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.attributes;
```

## Return Value

Returns an object of type

NamedNodeMap that allows to access attributes through their names.

## Usage

     Retrieve a listing of ALL Nodes of an element, including developer defined attributes and data- prefixed attributes.

The depreciated presentational attributes are datafld, datasrc, marginwidth, marginheight, allowtransparency, vspace, hspace, height, width, align, valign, alink, link, vlink, background, bgcolor, color, fgcolor, border, cellpadding, cellspacing, clear, frameborder, nowrap, scrolling

## Notes

For backwards compatibility first test if an attribute Node is null. Binary attributes may or may not have a value

## Related specifications

[Document Object Model (DOM) Level 3 Core Specification](http://www.w3.org/TR/DOM-Level-3-Core/core.html#ID-84CF096)
:   W3C Recommendation
