---
title: splitText
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Text.splitText](https://developer.mozilla.org/en-US/docs/Web/API/Text.splitText) Article]'
  - 'Microsoft Developer Network: [[splitText Method](http://msdn.microsoft.com/en-us/library/ie/ms536764(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Text
    href: /dom/Text
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Text
standardization_status: 'W3C Recommendation'
summary: 'Divides a text node at the specified index.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Text/splitText

---
## Summary

Divides a text node at the specified index.

Method of [dom/Text](/dom/Text)[dom/Text](/dom/Text)

## Syntax

``` js
var textNode = textNode.splitText(/* see parameter list */);
```

## Parameters

### offset

 Data-type
:   String

 The index of the string that indicates where the separation occurs. If a value is not provided, a new text node with no value is created.

## Return Value

Returns an object of type DOM NodeDOM Node

A text node object.

## Examples

This example uses the **splitText** method to divide a text node in half in a **ul** object. When the text node splits, the [**createElement**](/dom/Document/createElement) method creates a new **li** object. The [**appendChild**](/dom/Node/appendChild) method appends the new **li** element and the split text node to the **ul** object.

``` html
<script>
function fnSplitNode(){
   var oNode=oList.firstChild.childNodes(0);
   var oNewNode=document.createElement("LI");
   var oSplitNode = oNode.splitText(oNode.nodeValue.length/2);
   oList.appendChild(oNewNode);
   oNewNode.appendChild(oSplitNode);
}
</script>
<ul onclick="fnSplitNode()" id="oList">
<li>This is a list item.</li>
</ul>
```

## Notes

The text node that invokes the **splitText** method has a [**nodeValue**](/dom/Node/nodeValue) equal to the substring of the value, from zero to *offset*. The new text node has a **nodeValue** of the substring of the original value, from the specified index to the value length. Text node integrity is not preserved when the document is saved or persisted.

## Related specifications

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
