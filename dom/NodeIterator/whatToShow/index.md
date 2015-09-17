---
title: 'whatToShow'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[NodeIterator.whatToShow](https://developer.mozilla.org/en-US/docs/Web/API/NodeIterator.whatToShow) Article]'
  - 'Microsoft Developer Network: [[whatToShow Property](http://msdn.microsoft.com/en-us/library/ie/ff974822(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/NodeIterator
    href: /dom/NodeIterator
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned long'
    href: /dom/NodeIterator
standardization_status: 'W3C Recommendation'
summary: 'The NodeIterator.whatToShow read-only property represents an unsigned integer representing a bitmask signifying what types of nodes should be returned by the NodeIterator.'
tags:
  - API_Object_Properties
  - DOM
uri: dom/NodeIterator/whatToShow

---
## Summary

The NodeIterator.whatToShow read-only property represents an unsigned integer representing a bitmask signifying what types of nodes should be returned by the NodeIterator.

Property of [dom/NodeIterator](/dom/NodeIterator)[dom/NodeIterator](/dom/NodeIterator)

## Syntax

**Note**: This property is read-only.

``` js
var nodeTypes = element.whatToShow;
```

## Return Value

Returns an object of type unsigned longunsigned long

The type of accepted nodes.p is a bitwise OR of the following values:

NodeFilter.SHOW\_ALL (0xFFFFFFFF) Show all nodes.

NodeFilter.SHOW\_ELEMENT (0x00000001) Show Element nodes.

NodeFilter.SHOW\_ATTRIBUTE (0x00000002) show Attribute nodes.

NodeFilter.SHOW\_TEXT (0x00000004) Show Text nodes.

NodeFilter.SHOW\_CDATA\_SECTION (0x00000008) Show CDATASection nodes.

NodeFilter.SHOW\_ENTITY\_REFERENCE (0x00000010) Show EntityReference nodes.

NodeFilter.SHOW\_ENTITY (0x00000020) Show Entity nodes.

NodeFilter.SHOW\_PROCESSING\_INSTRUCTION (0x00000040) Show ProcessingInstruction nodes.

NodeFilter.SHOW\_COMMENT (0x00000080) Show Comment nodes.

NodeFilter.SHOW\_DOCUMENT (0x00000100) Show Document nodes.

NodeFilter.SHOW\_DOCUMENT\_TYPE (0x00000200) Show DocumentType nodes.

NodeFilter.SHOW\_DOCUMENT\_FRAGMENT (0x00000400) Show DocumentFragment nodes.

NodeFilter.SHOW\_NOTATION (0x00000800) Show Notation nodes.

## Examples

``` js
var nodeIterator = document.createNodeIterator(
    document.body,
    NodeFilter.SHOW_ELEMENT + NodeFilter.SHOW_COMMENT + NodeFilter.SHOW_TEXT,
    { acceptNode: function(node) { return NodeFilter.FILTER_ACCEPT; } },
    false
);
if( (nodeIterator.whatToShow == NodeFilter.SHOW_ALL)
```

## Notes

### Remarks

Filtering is based both on the **whatToShow** flags and the [**filter**](/dom/NodeIterator/filter) function.

### Syntax

var nodeTypes = nodeIterator.whatToShow;

### Standards information

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 1.2

## Related specifications

[DOM](http://dom.spec.whatwg.org/#dom-nodeiterator-whattoshow)
:   Living Standard
