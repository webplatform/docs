---
title: 'previousNode'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[NodeIterator.previousNode](https://developer.mozilla.org/en-US/docs/Web/API/NodeIterator.previousNode) Article]'
  - 'Microsoft Developer Network: [[previousNode Method](http://msdn.microsoft.com/en-us/library/ie/ff975284(v=vs.85).aspx) Article]'
notes:
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/NodeIterator
    href: /dom/NodeIterator
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/NodeIterator
standardization_status: 'W3C Recommendation'
summary: 'The NodeIterator.previousNode() method returns the previous node in the set represented by the NodeIterator and moves the position of the iterator backwards within the set.'
tags:
  - API_Object_Methods
  - DOM
uri: dom/NodeIterator/previousNode

---
<p>
</p>
<h2>Summary</h2>
<p>
The NodeIterator.previousNode() method returns the previous node in the set represented by the NodeIterator and moves the position of the iterator backwards within the set.</p><p>Method of <a href="/dom/NodeIterator">dom/NodeIterator</a><a href="/dom/NodeIterator">dom/NodeIterator</a>
</p>
<h2>Syntax</h2>
<pre class="js">
var object = object.previousNode(/* see parameter list */);
</pre>
<h2>Parameters</h2>
<h3>oNode</h3>
<dl><dt> Data-type</dt>
<dd> any</dd></dl><p><br/>
 Object containing the previous node in the list.
</p>
<h2>Return Value</h2>
<p>Returns an object of type  DOM NodeDOM Node
</p><p>Type: <b>HRESULT</b>
</p><p>This method can return one of these values.
</p>
<table class="wikitable"><tr><th>Return code
</th>
<th>Description
</th></tr><tr><td>S_OK
</td>
<td>The operation completed successfully.
</td></tr><tr><td>InvalidStateError _ERR
</td>
<td>NodeIterator raises this exception if detach has been invoked on the object.
</td></tr></table><p> 
</p><p>This method returns null when the current node is the first node in the set.
</p><p><br/><a href="/dom/Node"><b>Node</b></a>
</p><p> Object containing the previous node in the list.
</p>
<h2>Examples</h2>
<div class="example">
<pre class="js">
var nodeIterator = document.createNodeIterator(
    document.body,
    NodeFilter.SHOW_ELEMENT,
    { acceptNode: function(node) { return NodeFilter.FILTER_ACCEPT; } },
    false // this optional argument is not used any more
);
currentNode = nodeIterator.nextNode(); // returns the next node
previousNode = nodeIterator.previousNode(); // same result, since we backtracked to the previous nod

</pre>
<p><br/></p>
</div>
<h2>Notes</h2>
<p>In old browsers, as specified in old versions of the specifications, the method may throws the INVALID_STATE_ERR DOMException if this method is called after the NodeIterator.detach()method. Recent browsers never throw.
</p>
<h3>Syntax</h3>
<p>node = nodeIterator.previousNode();
</p>
<h3>Standards information</h3>
<ul><li><a rel="nofollow" class="external text" href="http://go.microsoft.com/fwlink/p/?linkid=182712">Document Object Model (DOM) Level 2 Traversal and Range Specification</a>, Section 1.2</li></ul><h2>Related specifications</h2>

<dl><dt><a rel="nofollow" class="external text" href="http://dom.spec.whatwg.org/#dom-nodeiterator-previousnode">DOM</a></dt>
  <dd>Living Standard</dd>
</dl>
