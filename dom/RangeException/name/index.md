---
title: 'name'
attributions:
  - 'Microsoft Developer Network: [[name Property](http://msdn.microsoft.com/en-us/library/ie/hh974331(v=vs.85).aspx) Article]'
notes:
  - "Depreciated?\nsee DOM/RangeException"
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/RangeException
    href: /dom/RangeException
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/RangeException
standardization_status: Deprecated
summary: 'Returns a DOMString value that is the name of the error that occurred during a Range operation.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/RangeException/name

---
<p>
</p>
<h2>Summary</h2>
<p>
Returns a DOMString value that is the name of the error that occurred during a Range operation.</p>
<div data-template="API_Object_Property">
<p><br/></p><p><br/></p><p>Property of <a href="/dom/RangeException">dom/RangeException</a><a href="/dom/RangeException">dom/RangeException</a>
</p>
<h2>Syntax</h2>
<p><b>Note</b>: This property is read-only.
</p>
<pre class="js">
var sErrName = rangeException.name;

</pre>
<h2>Return Value</h2>
<p>Returns an object of type StringString
</p><p>The name of the specific RangeException that occured.
</p>
</div>
<p><br/></p>
<h2>Notes</h2>
<h3>Remarks</h3>
<p>Range exception also supports a code value. The following table shows the code associated with the specific RangeException:
</p>
<table class="wikitable"><tr><th>Code value
</th>
<th>Name value
</th></tr><tr><td>1
</td>
<td>BadBoundarypointsError
</td></tr><tr><td>2
</td>
<td>InvalidNodeTypeError
</td></tr></table><p> 
</p>
<h3>Syntax</h3>
<h2>Related specifications</h2>

<dl><dt><a rel="nofollow" class="external text" href="http://dom.spec.whatwg.org/#interface-range">DOM</a></dt>
  <dd>Living Standard</dd>
</dl>
