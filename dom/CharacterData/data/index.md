---
title: data
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
    value: String
    href: /dom/CharacterData
standardization_status: 'W3C Recommendation'
summary: 'Sets or gets a node''s character data.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/CharacterData/data

---
## <span>Summary</span>

Sets or gets a node's character data.

Property of [dom/CharacterData](/dom/CharacterData)[dom/CharacterData](/dom/CharacterData)

## <span>Syntax</span>

``` js
var text = textualNode.html/elements/data;
textualNode.html/elements/data = newText;
```

## <span>Return Value</span>

Returns an object of type StringString

The value of the text node.

## <span>Examples</span>

``` js
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

``` html
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

## <span>Related specifications</span>

[DOM Level 1](http://www.w3.org/TR/REC-DOM-Level-1/)
:   Recommendation
