---
title: 'currentNode'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[TreeWalker.currentNode](https://developer.mozilla.org/en-US/docs/Web/API/TreeWalker.currentNode) Article]'
  - 'Microsoft Developer Network: [[currentNode Property](http://msdn.microsoft.com/en-us/library/ie/ff974804(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/TreeWalker
    href: /dom/TreeWalker
  return:
    predicate: 'Returns an object of type '
    value: 'DOM Node'
    href: /dom/TreeWalker
standardization_status: 'W3C Recommendation'
summary: 'Sets or retrieves where the current node in a filtered TreeWalker hierarchy is positioned.'
tags:
  - API_Object_Properties
  - DOM
uri: dom/TreeWalker/currentNode

---
## Summary

Sets or retrieves where the current node in a filtered TreeWalker hierarchy is positioned.

Property of [dom/TreeWalker](/dom/TreeWalker)[dom/TreeWalker](/dom/TreeWalker)

## Syntax

``` js
var node = walker.currentNode;
walker.currentNode = value;
```

## Return Value

Returns an object of type DOM NodeDOM Node

The currentNode of the TreeWalker object.

## Examples

``` html
<div id="divcontent">
<p>Some text</p>
<b>Bold text</b>
</div>

<script type="text/javascript">

var rootnode=document.getElementById('divcontent');
var walker=document.createTreeWalker(rootnode, NodeFilter.SHOW_ELEMENT, null, false);

//Alert the starting node Tree Walker currently points to (root node)
alert(walker.currentNode.tagName) //alerts DIV (with id=divcontent)

//Step through and alert all child nodes
while (walker.nextNode())
alert(walker.currentNode.tagName) //alerts P, SPAN, and B.

//Go back to the first child node of the collection and alert it
walker.currentNode=rootnode; //reset TreeWalker pointer to point to root node
alert(walker.firstChild().tagName); //alerts P

</script>
```

## Notes

### Remarks

**currentNode** will never return null in Windows Internet Explorer 9, even when the traversing method returns null.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 1.2

## Related specifications

[DOM](http://dom.spec.whatwg.org/#dom-treewalker-currentnode)
:   Living Standard
