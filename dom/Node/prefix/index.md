---
title: prefix
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Sets or retrieves the prefix of the fully qualified XML declaration for a node.'
uri: dom/Node/prefix

---
# prefix

## Summary

Sets or retrieves the prefix of the fully qualified XML declaration for a node.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Node](/dom/Node)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var prefix = node.prefix;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The prefix portion of the **qualified name** of the node.

## Examples

This example will only work when a namespace-aware parser is used, i.e. when a document is served with an XML mime-type. This will not work for HTML documents.

``` {.html}
<x:div onclick="alert(this.prefix)"/>
```

## Usage

     In XML documents, elements can be declared using qualified names, which consist of a prefix and a localName. This property returns the former value.

For more information, see [W3C Namespaces in XML](http://go.microsoft.com/fwlink/p/?linkid=203781).

## Notes

Prior to Gecko 5.0 (Firefox 5.0 / Thunderbird 5.0 / SeaMonkey 2.2), this property was read-write; the specification says it should be read only, and now it is.

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.prefix](https://developer.mozilla.org/en-US/docs/Web/API/Node.prefix) Article]

Portions of this content come from the Microsoft Developer Network: [[prefix Property](http://msdn.microsoft.com/en-us/library/ie/ff974772(v=vs.85).aspx) Article]

