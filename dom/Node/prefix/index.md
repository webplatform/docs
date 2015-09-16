---
title: 'prefix'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.prefix](https://developer.mozilla.org/en-US/docs/Web/API/Node.prefix) Article]'
  - 'Microsoft Developer Network: [[prefix Property](http://msdn.microsoft.com/en-us/library/ie/ff974772(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Node
    href: /dom/Node
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/Node
standardization_status: 'W3C Recommendation'
summary: 'Sets or retrieves the prefix of the fully qualified XML declaration for a node.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Node/prefix

---
## Summary

Sets or retrieves the prefix of the fully qualified XML declaration for a node.

Property of [dom/Node](/dom/Node)[dom/Node](/dom/Node)

## Syntax

**Note**: This property is read-only.

``` js
var prefix = node.prefix;
```

## Return Value

Returns an object of type StringString

The prefix portion of the **qualified name** of the node.

## Examples

This example will only work when a namespace-aware parser is used, i.e. when a document is served with an XML mime-type. This will not work for HTML documents.

``` html
<x:div onclick="alert(this.prefix)"/>
```

## Usage

     In XML documents, elements can be declared using qualified names, which consist of a prefix and a localName. This property returns the former value.

For more information, see [W3C Namespaces in XML](http://go.microsoft.com/fwlink/p/?linkid=203781).

## Notes

Prior to Gecko 5.0 (Firefox 5.0 / Thunderbird 5.0 / SeaMonkey 2.2), this property was read-write; the specification says it should be read only, and now it is.

## Related specifications

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
