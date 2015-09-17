---
title: 'RangeException'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Summary, examples, compat, better spec link'
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Element
    href: /dom/Element
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Element
standardization_status: 'W3C Candidate Recommendation'
tags:
  - API_Object_Methods
  - DOM
  - Needs_Summary
  - Needs_Examples
uri: dom/Element/RangeException

---
<p>
</p>

<p>Method of <a href="/dom/Element">dom/Element</a><a href="/dom/Element">dom/Element</a>
</p>
<h2>Syntax</h2>
<pre class="js">
var object = object.RangeException(fragment, retVal);
</pre>
<h2>Parameters</h2>
<h3>fragment</h3>
<dl><dt> Data-type</dt>
<dd> any</dd></dl><p><br/>
String containing HTML to be parsed.
</p><p><br/></p>
<h3>retVal</h3>
<dl><dt> Data-type</dt>
<dd> any</dd></dl><p><br/>
A document fragment representing the parsed HTML.
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
</td></tr><tr><td>W3CException_INVALID_STATE_ERR
</td>
<td>Throws this exception if the range has been detached.
</td></tr></table><p> 
</p><p>DocumentFragment
</p><p>A document fragment representing the parsed HTML.
</p>

<h2>Notes</h2>
<h3>Remarks</h3>
<p>When inserting elements into a DOM structure, some elements behave according to their context. Using createContextualFragment, you can ensure the parsed HTML will work as expected when inserted or added to the document.
</p>
<h3>Syntax</h3>
<h3>Standards information</h3>
<ul><li><a rel="nofollow" class="external text" href="http://go.microsoft.com/fwlink/p/?linkid=221374">HTML5 A vocabulary and associated APIs for HTML and XHTML</a></li></ul><p><br/></p>
<h2>See also</h2>
<h3>Related pages</h3>
<ul><li>Range<a href="/dom/Range">Range</a></li></ul>
