---
title: length
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Gets the number of characters in a text node.'
uri: dom/CharacterData/length

---
# length

## Summary

Gets the number of characters in a text node.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/CharacterData](/dom/CharacterData)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var textLength = textualNode.length;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

The number of characters in the node.

## Examples

``` {.js}
//create text node
var phrase = document.createTextNode ("A flawed plan today is better than a perfect plan tomorrow.");
//report length
alert(phrase.length);
```

This example uses the **length** property to specify where a [**Text**](/dom/Text) node is split by using the [**splitText**](/dom/Text/splitText) method.

``` {.html}
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

Specification
:   Status
[DOM Level 1](http://www.w3.org/TR/REC-DOM-Level-1/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

