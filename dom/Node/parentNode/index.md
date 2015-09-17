---
title: 'parentNode'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.parentNode](https://developer.mozilla.org/en-US/docs/Web/API/Node.parentNode) Article]'
  - 'Microsoft Developer Network: [[parentNode Property](http://msdn.microsoft.com/en-us/library/ie/ms534328(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Node
    href: /dom/Node
  return:
    predicate: 'Returns an object of type '
    value: 'DOM Node'
    href: /dom/Node
standardization_status: 'W3C Recommendation'
summary: 'Retrieves the parent node in the document hierarchy.'
tags:
  - API_Object_Properties
  - DOM
uri: dom/Node/parentNode

---
## Summary

Retrieves the parent node in the document hierarchy.

Property of [dom/Node](/dom/Node)[dom/Node](/dom/Node)

## Syntax

**Note**: This property is read-only.

``` js
var parentNode = node.parentNode;
```

## Return Value

Returns an object of type DOM NodeDOM Node

The parent node of the node.

## Examples

This example assigns the **parentNode** of a **span** object to a variable.

``` html
<script>
var oParent = document.getElementById("oSpan").parentNode;
</script>
:
<body>
<span ID="oSpan">A Span</span>
</body>
```

This example assigns the **parentNode** of a node, created with the [**createElement**](/dom/Document/createElement) method, to a variable.

``` js
var oNode = document.createElement("B");
document.body.insertBefore(oNode);
// This returns document.body.
var oParent = oNode.parentNode;
```

This example demonstrates the difference between parentNode and parentElement when queried on the documents root element (\<html\>)

``` html
<!DOCTYPE html>
<html id="root">

<head>
<meta content="text/html; charset=utf-8" http-equiv="Content-Type">
<title>parentElement/parentNode</title>
</head>

<body>
<script type="text/javascript">
var root=document.getElementById('root');
try{document.write('typeof root.parentNode:'+ typeof(root.parentNode)+'<br/>');}catch(e){alert(e);}
try{document.write('root.parentNode.tagName:'+root.parentNode.tagName+'<br/>');}catch(e){alert(e);}
try{document.write('typeof root.parentElement:'+typeof(root.parentElement)+'<br/>');}catch(e){alert(e);}
try{document.write('root.parentElement.tagName:'+root.parentElement.tagName+'<br/>');}catch(e){alert(e);}
</script>
</body>

</html>
```

## Usage

     Use to find the parent of a node (if any).

## Notes

The topmost object returns null as its parent.

## Related specifications

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
