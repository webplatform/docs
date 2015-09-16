---
title: 'compareDocumentPosition'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.compareDocumentPosition](https://developer.mozilla.org/en-US/docs/Web/API/Node.compareDocumentPosition) Article]'
  - 'Microsoft Developer Network: [[compareDocumentPosition Method](http://msdn.microsoft.com/en-us/library/ie/ff975125(v=vs.85).aspx) Article]'
notes:
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Node
    href: /dom/Node
  return_type:
    predicate: 'Returns an object of type  '
    value: Number
    href: /dom/Node
standardization_status: 'W3C Recommendation'
summary: 'Compares the position of two nodes in a document.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Node/compareDocumentPosition

---
<p>
</p>
<h2>Summary</h2>
<p>
Compares the position of two nodes in a document.</p><p>Method of <a href="/dom/Node">dom/Node</a><a href="/dom/Node">dom/Node</a>
</p>
<h2>Syntax</h2>
<pre class="js">
var positionBitmask = node.compareDocumentPosition(/* see parameter list */);
</pre>
<h2>Parameters</h2>
<h3>otherNode</h3>
<dl><dt> Data-type</dt>
<dd> DOM Node</dd></dl><p><br/>
The node to be compared to the reference node, which is the node executing the method.
</p>
<h2>Return Value</h2>
<p>Returns an object of type  NumberNumber
</p><p>Describes how the position of the node specified by the <i>otherNode</i> parameter relates to the position of the reference node. The return value contains one or more of the following flag values:
</p>
<table class="wikitable"><tr><th><a href="/dom/Node">Node</a> constant name
</th>
<th>Return value (Integer)
</th>
<th>Return value (Hexadecimal)
</th>
<th>Description
</th></tr><tr><td>DOCUMENT_POSITION_DISCONNECTED
</td>
<td>1
</td>
<td>0x01
</td>
<td>The nodes are disconnected.
</td></tr><tr><td>DOCUMENT_POSITION_PRECEDING
</td>
<td>2
</td>
<td>0x02
</td>
<td>The position of the node specified by the otherNode parameter precedes the position of the reference node.
</td></tr><tr><td>DOCUMENT_POSITION_FOLLOWING
</td>
<td>4
</td>
<td>0x04
</td>
<td>The position of the node specified by the otherNode parameter follows the position of the reference node.
</td></tr><tr><td>DOCUMENT_POSITION_CONTAINS
</td>
<td>8
</td>
<td>0x08
</td>
<td>The reference node contains the node specified by the otherNode parameter.
</td></tr><tr><td>DOCUMENT_POSITION_CONTAINED_BY
</td>
<td>16
</td>
<td>0x10
</td>
<td>The node specified by the otherNode parameter contains the reference node.
</td></tr><tr><td>DOCUMENT_POSITION_IMPLEMENTATION_SPECIFIC
</td>
<td>32
</td>
<td>0x20
</td>
<td>The node positions depend on the DOM implementation and cannot be compared.
</td></tr></table><p> 
</p>
<h2>Examples</h2>
<p>This example determines if the web document is incorrectly marked up with the body element before the head element.
Note: Web browsers sometimes self correct markup errors. HTML5 is the first specification to give guidelines to browser vendors on how they should correct markup errors.
</p>
<div class="example">
<pre class="html">
var head = document.getElementsByTagName('head').item(0);
if (head.compareDocumentPosition(document.body) &amp; Node.DOCUMENT_POSITION_FOLLOWING) {
  console.log("well-formed document");
} else {
  console.log("&lt;head&gt; is not before &lt;body&gt;");
}

</pre>
<p><br/></p>
</div>
<h2>Notes</h2>
<p>For information about the factors that affect the position of nodes within the DOM, see the related specifications.
</p><p><br/></p>
<h2>Related specifications</h2>

<dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/DOM-Level-3-Core/">DOM Level 3 Core</a></dt>
  <dd>Recommendation</dd>
</dl>
