---
title: attributes
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Associatve array containing the attributes of node.'
uri: dom/Node/attributes

---
# attributes

## Summary

Associatve array containing the attributes of node.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Node](/dom/Node)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.attributes;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value"></span></span>

NamedNodeMap that allows to access attributes through their names.

## Usage

     Retrieve a listing of ALL Nodes of an element, including developer defined attributes and data- prefixed attributes.

The depreciated presentational attributes are datafld, datasrc, marginwidth, marginheight, allowtransparency, vspace, hspace, height, width, align, valign, alink, link, vlink, background, bgcolor, color, fgcolor, border, cellpadding, cellspacing, clear, frameborder, nowrap, scrolling

## Notes

For backwards compatibility first test if an attribute Node is null. Binary attributes may or may not have a value

## Related specifications

Specification
:   Status
[Document Object Model (DOM) Level 3 Core Specification](http://www.w3.org/TR/DOM-Level-3-Core/core.html#ID-84CF096)
:   W3C Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.attributes](https://developer.mozilla.org/en-US/docs/Web/API/Node.attributes) Article]

Portions of this content come from the Microsoft Developer Network: [[attributes Collection](http://msdn.microsoft.com/en-us/library/ie/ms537438(v=vs.85).aspx) Article]

