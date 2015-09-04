---
title: whatToShow
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The NodeIterator.whatToShow read-only property represents an unsigned integer representing a bitmask signifying what types of nodes should be returned by the NodeIterator.'
uri: dom/NodeIterator/whatToShow

---
# whatToShow

## Summary

The NodeIterator.whatToShow read-only property represents an unsigned integer representing a bitmask signifying what types of nodes should be returned by the NodeIterator.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/NodeIterator](/dom/NodeIterator)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var nodeTypes = element.whatToShow;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned long</span></span>

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

``` {.js}
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

Specification
:   Status
[DOM](http://dom.spec.whatwg.org/#dom-nodeiterator-whattoshow)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[NodeIterator.whatToShow](https://developer.mozilla.org/en-US/docs/Web/API/NodeIterator.whatToShow) Article]

Portions of this content come from the Microsoft Developer Network: [[whatToShow Property](http://msdn.microsoft.com/en-us/library/ie/ff974822(v=vs.85).aspx) Article]

