---
title: hasChildNodes
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs some more content.'
summary: 'Gets a value that indicates whether the Node has any direct Node descendant of any type.'
uri: dom/Node/hasChildNodes

---
# hasChildNodes

## Summary

Gets a value that indicates whether the Node has any direct Node descendant of any type.

*Method of [dom/Node](/dom/Node)*

## Syntax

``` {.js}
var hasChildNodes = element.hasChildNodes();
```

## Return Value

Returns an object of type Boolean.

Whether or not the Node contains any direct Node descendant of any type

## Examples

The following example removes the first child node inside the element with the id "foo" if foo has child nodes.

``` {.js}
var foo = document.getElementById("foo");

if (foo.hasChildNodes()) {
  foo.removeChild(foo.childNodes[0]);
}
```

{{Notes\_Section |Notes=If the Node contains any [[dom/Element|Element], [dom/Text|Text] or other type of nodes, they can be accessed from the [**childNodes**](/dom/Node/childNodes) collection. }}

## Related specifications

Specification
:   Status
[Document Object Model (DOM) Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/core.html#ID-810594187)
:   W3C Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.hasChildNodes](https://developer.mozilla.org/en-US/docs/Web/API/Node.hasChildNodes) Article]

Portions of this content come from the Microsoft Developer Network: [[hasChildNodes() Method](http://msdn.microsoft.com/en-us/library/ie/ms536445(v=vs.85).aspx) Article]

