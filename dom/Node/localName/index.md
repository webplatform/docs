---
title: localName
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
notes:
  - "Needs example\nMust be served with XML content type, such as text/xml or application/xhtml+xml"
summary: 'Retrieves the local name of the fully qualified XML declaration for a node.'
uri: dom/Node/localName

---
# localName

## Summary

Retrieves the local name of the fully qualified XML declaration for a node.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Node](/dom/Node)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var localName = node.localName;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The local name portion of the **qualified name** of the node.

**Needs Examples**: This section should include examples.

## Usage

     In XML documents, elements can be declared using qualified names, which consist of a prefix and a local name. This property returns the latter value.

For more information, see [W3C Namespaces in XML](http://go.microsoft.com/fwlink/p/?linkid=203781).

## Notes

Must be served with XML content type, such as text/xml or application/xhtml+xml

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.localName](https://developer.mozilla.org/en-US/docs/Web/API/Node.localName) Article]

Portions of this content come from the Microsoft Developer Network: [[localName Property](http://msdn.microsoft.com/en-us/library/ie/ff974770(v=vs.85).aspx) Article]

