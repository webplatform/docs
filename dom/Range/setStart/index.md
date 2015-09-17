---
title: 'setStart'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Range.setStart](https://developer.mozilla.org/en-US/docs/Web/API/Range.setStart) Article]'
  - 'Microsoft Developer Network: [[setStart Method](http://msdn.microsoft.com/en-us/library/ie/ff975451(v=vs.85).aspx) Article]'
notes:
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Range
    href: /dom/Range
  return_type:
    predicate: 'Returns an object of type  '
    value: Number
    href: /dom/Range
standardization_status: 'W3C Recommendation'
summary: 'Sets the starting point of a range'
tags:
  - API_Object_Methods
  - DOM
uri: dom/Range/setStart

---
<p>
</p>
<h2>Summary</h2>
<p>
Sets the starting point of a range</p><p>Method of <a href="/dom/Range">dom/Range</a><a href="/dom/Range">dom/Range</a>
</p>
<h2>Syntax</h2>
<pre class="js">
var result = range.setStart(/* see parameter list */);
</pre>
<h2>Parameters</h2>
<h3>startNode</h3>
<dl><dt> Data-type</dt>
<dd> DOM Node</dd></dl><p><br/>
Node in the document hierarchy.
</p><p><br/></p>
<h3>startOffset</h3>
<dl><dt> Data-type</dt>
<dd> Number</dd></dl><p><br/>
Specifies the offset value for the starting point.
</p>
<h2>Return Value</h2>
<p>Returns an object of type  NumberNumber
</p><p>Type: <b>HRESULT</b>
</p><p>This method can return one of these values.
</p>
<table class="wikitable"><tr><th>Return code
</th>
<th>Description
</th></tr><tr><td>S_OK
</td>
<td>The operation completed successfully.
</td></tr><tr><td>InvalidStateError
</td>
<td>detach has been invoked on the object.
</td></tr><tr><td>W3Exception_DOM_INDEX_SIZE_ERR
</td>
<td>offset is negative or greater than the number of child units in refNode.
</td></tr></table><p> 
</p>
<h2>Examples</h2>
<div class="example">
<pre class="js">
var range = document.createRange();
var startNode = document.getElementsByTagName("p").item(2);
var startOffset = 0;
range.setStart(startNode,startOffset);

</pre>
<p><br/></p>
</div>
<h2>Notes</h2>
<p>If the startNode is a Node of type Text, Comment, or CDATASection, then startOffset is the number of characters from the start of startNode. For other Node types, startOffset is the number of child nodes between the start of the startNode.
</p>
<h3>Syntax</h3>
<p>range.setStart(startNode, startOffset);
</p>
<h3>Standards information</h3>
<ul><li><a rel="nofollow" class="external text" href="http://go.microsoft.com/fwlink/p/?linkid=182712">Document Object Model (DOM) Level 2 Traversal and Range Specification</a>, Section 2.13</li></ul><h2>Related specifications</h2>

<dl><dt><a rel="nofollow" class="external text" href="http://dom.spec.whatwg.org/#dom-range-setstart">DOM</a></dt>
  <dd>Living Standard</dd>
</dl>
