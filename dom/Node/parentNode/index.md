---
title: parentNode
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Retrieves the parent node in the document hierarchy.'
uri: dom/Node/parentNode

---
# parentNode

## Summary

Retrieves the parent node in the document hierarchy.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Node](/dom/Node)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var parentNode = node.parentNode;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">DOM Node</span></span>

The parent node of the node.

## Examples

This example assigns the **parentNode** of a **span** object to a variable.

``` {.html}
<script>
var oParent = document.getElementById("oSpan").parentNode;
</script>
:
<body>
<span ID="oSpan">A Span</span>
</body>
```

This example assigns the **parentNode** of a node, created with the [**createElement**](/dom/Document/createElement) method, to a variable.

``` {.js}
var oNode = document.createElement("B");
document.body.insertBefore(oNode);
// This returns document.body.
var oParent = oNode.parentNode;
```

This example demonstrates the difference between parentNode and parentElement when queried on the documents root element (\<html\>)

``` {.html}
<!DOCTYPE html>
<html id="root">

<head>
<meta content="text/html; charset=utf-8" http-equiv="Content-Type">
<title>parentElement/parentNode</title>
</head>

<body>
<script type="text/javascript">
var root=document.getElementById('root');
try{document.write('typeof root.parentNode:'+ typeof(root.parentNode)+'');}catch(e){alert(e);}
try{document.write('root.parentNode.tagName:'+root.parentNode.tagName+'');}catch(e){alert(e);}
try{document.write('typeof root.parentElement:'+typeof(root.parentElement)+'');}catch(e){alert(e);}
try{document.write('root.parentElement.tagName:'+root.parentElement.tagName+'');}catch(e){alert(e);}
</script>
</body>

</html>
```

## Usage

     Use to find the parent of a node (if any).

## Notes

The topmost object returns null as its parent.

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.parentNode](https://developer.mozilla.org/en-US/docs/Web/API/Node.parentNode) Article]

Portions of this content come from the Microsoft Developer Network: [[parentNode Property](http://msdn.microsoft.com/en-us/library/ie/ms534328(v=vs.85).aspx) Article]

