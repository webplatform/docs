---
title: currentNode
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Sets or retrieves where the current node in a filtered TreeWalker hierarchy is positioned.'
uri: dom/TreeWalker/currentNode

---
# currentNode

## Summary

Sets or retrieves where the current node in a filtered TreeWalker hierarchy is positioned.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/TreeWalker](/dom/TreeWalker)</span></span>

## Syntax

``` {.js}
var node = walker.currentNode;
walker.currentNode = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">DOM Node</span></span>

The currentNode of the TreeWalker object.

## Examples

``` {.html}
<div id="divcontent">
<p>Some <span>text</span></p>
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

Specification
:   Status
[DOM](http://dom.spec.whatwg.org/#dom-treewalker-currentnode)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[TreeWalker.currentNode](https://developer.mozilla.org/en-US/docs/Web/API/TreeWalker.currentNode) Article]

Portions of this content come from the Microsoft Developer Network: [[currentNode Property](http://msdn.microsoft.com/en-us/library/ie/ff974804(v=vs.85).aspx) Article]

