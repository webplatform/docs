---
title: 'RangeException'
attributions:
  - 'Microsoft Developer Network: [[RangeException Object](http://msdn.microsoft.com/en-us/library/ie/ff974358(v=vs.85).aspx) Article]'
notes:
  - 'Missing code and message properties'
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
readiness: 'Not Ready'
standardization_status: Deprecated
summary: 'Describes errors thrown by selection and range operations.'
tags:
  - API
  - Objects
  - DOM
uri: dom/RangeException

---
<p>
</p>
<h2>Summary</h2>
<p>
Describes errors thrown by selection and range operations.</p><p><br/></p>
<h2>Properties</h2>

<dl><dt>API Name</dt>
  <dd>Summary</dd>
</dl><dl><dt><a href="/dom/RangeException/name">name</a></dt>
  <dd>Returns a DOMString value that is the name of the error that occurred during a Range operation.</dd>
</dl><p><br/></p>
<h2>Methods</h2>
<p><i>No methods.</i>
</p>
<h2>Events</h2>
<p><i>No events.</i>
</p><p><br/></p>
<h2>Usage</h2>
<pre> Use <a rel="nofollow" class="external text" href="http://docs.webplatform.org/wiki/dom/DOMException">DOMException</a> instead.
</pre>
<h2>Notes</h2>
<p>Starting with Gecko 13.0 (Firefox 13.0 / Thunderbird 13.0 / SeaMonkey 2.10) the Range object throws a DOMException as defined in DOM 4, instead of a RangeException defined in prior specifications.
</p><p>Gecko supported it up to Gecko 1.9, then removed it until Gecko 17 where it was reimplemented, matching the spec
</p>
<h3>Standards information</h3>
<ul><li><a rel="nofollow" class="external text" href="http://go.microsoft.com/fwlink/p/?linkid=182712">Document Object Model (DOM) Level 2 Traversal and Range Specification</a>, Section 2.13</li></ul><p> 
</p>
<h2>Related specifications</h2>

<dl><dt><a rel="nofollow" class="external text" href="http://dom.spec.whatwg.org/#interface-range">DOM</a></dt>
  <dd>Living Standard</dd>
</dl>
