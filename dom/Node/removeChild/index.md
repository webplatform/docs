---
title: 'removeChild'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.removeChild](https://developer.mozilla.org/en-US/docs/Web/API/Node.removeChild) Article]'
  - 'Microsoft Developer Network: [[removeChild Method](http://msdn.microsoft.com/en-us/library/ie/ms536702(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Node
    href: /dom/Node
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Node
standardization_status: 'W3C Recommendation'
summary: 'Removes a child node from a node.'
tags:
  - API_Object_Methods
  - DOM
uri: dom/Node/removeChild

---
## Summary

Removes a child node from a node.

Method of [dom/Node](/dom/Node)[dom/Node](/dom/Node)

## Syntax

``` js
var removedNode = node.removeChild(/* see parameter list */);
```

## Parameters

### oldChild

 Data-type
:   Blob

 The node to be removed from the document.

## Return Value

Returns an object of type DOM NodeDOM Node

The removed node.

## Examples

This example uses the **removeChild** method to remove a bold element from a **div**.

``` html
<!doctype html>
<html>
<head>
<script type="application/javascript">
function removeElement()
{
  var div1 = document.getElementById("Div1");
  try
  {
      //The first child of the div is the bold element.
    var oChild=div1.children(0);
    div1.removeChild(oChild);
  }
  catch(x)
  {
    alert("You have already removed the bold element.\nPage will be refreshed when you click OK.")
    document.location.reload();
  }
}
</script>
</head>
<body>
<div id="Div1" onclick="removeElement()">
Click anywhere in this sentence to remove this <strong>Bold</strong> word.
</div>
</body>
</html>
```

Remove all children from a node.

``` js
while (element.lastChild) {
  element.removeChild(element.lastChild);
}
```

## Notes

The node to be removed must be an immediate child of the parent node. This method is accessible at run time. If elements are removed at run time, before the closing tag is parsed, areas of the document might not render.

## Related specifications

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
