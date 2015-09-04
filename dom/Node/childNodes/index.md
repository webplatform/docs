---
title: childNodes
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs some more content.'
summary: 'Gets a collection of direct Node descendants of the Node, including Element, Text and any other type of nodes.'
uri: dom/Node/childNodes

---
# childNodes

## Summary

Gets a collection of direct Node descendants of the Node, including Element, Text and any other type of nodes.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Node](/dom/Node)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.childNodes;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value"></span></span>

A live collection of the direct Node descendants of the Node.

## Examples

This example shows how to assign to a variable the **childNodes** collection of the **body** object.

    <script>
    var aNodeList = oBody.childNodes;
    </script>
    <body id="oBody">
    <span id="oSpan">A Span</span>
    </body>

This example shows how to assign to a variable the **childNodes** collection of a node created with the [**createElement**](/dom/Document/createElement) method.

``` {.js}
var oParentNode = document.createElement("DIV");
var oNode = document.createElement("B");
document.body.insertBefore(oParentNode);
oParentNode.insertBefore(oNode);
var aNodeList = oParentNode.childNodes;
```

## Notes

The **childNodes** collection can contain [**Element**](/dom/Element) and [**Text**](/dom/Text) nodes. If you check the **childNodes** collection of an element created through standard HTML, you encounter [**Text**](/dom/Text) nodes in unexpected places—in place of line breaks, for example. Alternately, if you create an element using the Document Object Model (DOM), no unintended [**Text**](/dom/Text) nodes are created.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.childNodes](https://developer.mozilla.org/en-US/docs/Web/API/Node.childNodes) Article]

Portions of this content come from the Microsoft Developer Network: [[childNodes Property](http://msdn.microsoft.com/en-us/library/ie/ms537445(v=vs.85).aspx) Article]

