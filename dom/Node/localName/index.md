---
title: localName
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.localName](https://developer.mozilla.org/en-US/docs/Web/API/Node.localName) Article]'
  - 'Microsoft Developer Network: [[localName Property](http://msdn.microsoft.com/en-us/library/ie/ff974770(v=vs.85).aspx) Article]'
notes:
  - "Needs example\nMust be served with XML content type, such as text/xml or application/xhtml+xml"
readiness: 'In Progress'
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
summary: 'Retrieves the local name of the fully qualified XML declaration for a node.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Node/localName

---
## Summary

Retrieves the local name of the fully qualified XML declaration for a node.

Property of [dom/Node](/dom/Node)[dom/Node](/dom/Node)

## Syntax

**Note**: This property is read-only.

``` js
var localName = node.localName;
```

## Return Value

Returns an object of type StringString

The local name portion of the **qualified name** of the node.

**Needs Examples**: This section should include examples.

## Usage

     In XML documents, elements can be declared using qualified names, which consist of a prefix and a local name. This property returns the latter value.

For more information, see [W3C Namespaces in XML](http://go.microsoft.com/fwlink/p/?linkid=203781).

## Notes

Must be served with XML content type, such as text/xml or application/xhtml+xml

## Related specifications

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
