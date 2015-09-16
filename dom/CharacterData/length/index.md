---
title: length
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/CharacterData
    href: /dom/CharacterData
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /dom/CharacterData
standardization_status: 'W3C Recommendation'
summary: 'Gets the number of characters in a text node.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/CharacterData/length

---
## Summary

Gets the number of characters in a text node.

Property of [dom/CharacterData](/dom/CharacterData)[dom/CharacterData](/dom/CharacterData)

## Syntax

**Note**: This property is read-only.

``` js
var textLength = textualNode.length;
```

## Return Value

Returns an object of type NumberNumber

The number of characters in the node.

## Examples

``` js
//create text node
var phrase = document.createTextNode ("A flawed plan today is better than a perfect plan tomorrow.");
//report length
alert(phrase.length);
```

This example uses the **length** property to specify where a [**Text**](/dom/Text) node is split by using the [**splitText**](/dom/Text/splitText) method.

``` html
<script>
function fnChangeValue(){
   var oListItem = document.createElement("LI");
   var oList = document.getElementById("oList");
   oList.appendChild(oListItem);
   var oNode = oList.firstChild.childNodes(0);
   var oTextNode = oList.firstChild.childNodes(0);
   var oSplit = oTextNode.splitText(oTextNode.length/2);
   oListItem.appendChild(oSplit);
}
</script>
<ul id="oList" onclick="fnChangeValue()">
<li>Start Here</li>
</ul>
```

## Related specifications

[DOM Level 1](http://www.w3.org/TR/REC-DOM-Level-1/)
:   Recommendation
