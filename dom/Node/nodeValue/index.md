---
title: nodeValue
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Gets or sets the value of a Node, if the type of Node supports it.'
uri: dom/Node/nodeValue
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/Attr/value

---
# nodeValue

## Summary

Gets or sets the value of a Node, if the type of Node supports it.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Node](/dom/Node)</span></span>

## Syntax

``` {.js}
var value = node.nodeValue;
node.nodeValue = newValue;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The value of the node.

## Examples

The following code example alters the text of the specified list item by setting the **nodeValue** property of the text node that is contained by that list item.

``` {.html}
<!DOCTYPE html>
<html>
<head>
<title>Title</title>
<script>
function changeValue(list, itemIndex, newValue) {
   // only perform the operation on lists
   if (list.nodeName !== "UL" && list.nodeName != "OL")
      return false;
   // only perform the operation if the specified index is
   // within the acceptable range of available list items
   if (itemIndex > list.childNodes.length -1)
      return false;
   // get a reference to the specified list item
   var liElements = list.childNodes[itemIndex];
   if (!liElements)
      return false;
   // get a reference to the text node contained by the list item
   var textNode = liElements.childNodes[0];
   // ensure that the node is a text node
   if (textNode.nodeType !== 3)
      return false;
   textNode.nodeValue = newValue;
   return true;
}
function initialize() {
  document.getElementById("list").addEventListener(
    "click",
    function () {
     changeValue(this, 0, "New Node value");
    },
    false);
}
document.addEventListener("DOMContentLoaded", initialize, false);
</script>
</head>
<body>
<ul id="list"><li>Old Node Value</li></ul>
</body>
```

## Usage

     Use this property to get or set the value of a Node. The concept of nodeValue changes between the various Node types (Element, Text and the rest).

## Notes

-   The value of this property for [Text](/dom/Text) nodes is their [Text.textContent](/dom/Node/textContent).
-   This property is deprecated for [Attr](/dom/Attr) nodes. Use [Attr.value](/w/index.php?title=dom/Attr/value&action=edit&redlink=1) instead. The value of this property for Attr nodes is their Attr.value.
-   The value of this property for [Element](/dom/Element) nodes is always `null`. Use [Node.nodeName](/dom/Node/nodeName) to get their name or [dom/Node/textContent](/dom/Node/textContent) to get all of the text included in their tree.

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   W3C Recommendation
[WHATWG DOM](http://dom.spec.whatwg.org/#dom-node-nodevalue)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.nodeValue](https://developer.mozilla.org/en-US/docs/Web/API/Node.nodeValue) Article]

Portions of this content come from the Microsoft Developer Network: [[nodeValue Property](http://msdn.microsoft.com/en-us/library/ie/ms534192(v=vs.85).aspx) Article]

