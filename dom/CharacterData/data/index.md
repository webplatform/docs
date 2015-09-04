---
title: data
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Sets or gets a node''s character data.'
uri: dom/CharacterData/data

---
# data

## Summary

Sets or gets a node's character data.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/CharacterData](/dom/CharacterData)</span></span>

## Syntax

``` {.js}
var text = textualNode.data;
textualNode.data = newText;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The value of the text node.

## Examples

``` {.js}
//create text node
var phrase = document.createTextNode ("A flawed plan today is better than a perfect plan tomorrow.");
//report contents
alert(phrase.data);
//modify contents
phrase.data = "Any plan is better than no plan at all.";
//report contents
alert(phrase.data);
```

This example uses the **data** property to change the value of a text node.

``` {.html}
<script>
function fnChangeValue(){
   var oNode = oList.firstChild.childNodes(0);
   var oNewText = document.createTextNode();
   oNewText.data="Create Data";
   oNode.replaceNode(oNewText);
   oNode.data = "New Node Value";
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

