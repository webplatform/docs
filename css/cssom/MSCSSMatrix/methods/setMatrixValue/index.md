---
title: 'setMatrixValue'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Little content; browser-specific; move/deletion candidate'
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
readiness: 'Not Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: css/cssom/MSCSSMatrix
    href: '/w/index.php?title=css/cssom/MSCSSMatrix&action=edit&redlink=1'
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: '/w/index.php?title=css/cssom/MSCSSMatrix&action=edit&redlink=1'
tags:
  - API_Object_Methods
  - DOM
  - Needs_Summary
  - Needs_Examples
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - css/cssom/MSCSSMatrix
uri: css/cssom/MSCSSMatrix/methods/setMatrixValue

---
<p><br/></p>

<p>Method of <a href="/w/index.php?title=css/cssom/MSCSSMatrix&amp;action=edit&amp;redlink=1" class="new">css/cssom/MSCSSMatrix</a><a href="/w/index.php?title=css/cssom/MSCSSMatrix&amp;action=edit&amp;redlink=1" class="new">css/cssom/MSCSSMatrix</a>
</p>
<h2>Syntax</h2>
<pre class="js">
var object = object.setMatrixValue();
</pre>
<p><br/></p>
<h2>Return Value</h2>
<p>Returns an object of type  DOM NodeDOM Node
</p><p>Type: <b>HRESULT</b>
</p><p>This method can return one of these values.
</p>
<table class="wikitable"><tr><th>Return code/value
</th>
<th>Description
</th></tr><tr><td>S_OK
</td>
<td>The operation completed successfully.
</td></tr><tr><td>DOMException.SYNTAX_ERR
<p>12
</p>
</td>
<td>The transformValue string cannot be parsed into an MSCSSMatrix. This occurs when the string is not a valid value for the transform property, or if the string contains relative units.
</td></tr></table><p> 
</p>

<h2>Notes</h2>
<h3>Remarks</h3>
<p>Using the <b>setMatrixValue</b> method and setting the <a href="/css/transforms/MSCSSMatrix"><b>MSCSSMatrix</b></a> attributes individually are the only ways to modify the current matrix. No other method will alter the current matrix.
</p>
<h3>Syntax</h3>
<h3>Standards information</h3>
<ul><li><a rel="nofollow" class="external text" href="http://go.microsoft.com/fwlink/p/?linkid=223140">CSS Transitions Module Level 3</a>, Section 10.1</li></ul><p><br/></p>
<h3>Parameters</h3>
<dl><dt><i>transformValue</i> [in]</dt>
<dd>Type: <b>DOMString</b>A string in the form of an acceptable value for the <a href="/css/transforms/transform" class="mw-redirect"><b>transform</b></a> property in CSS.</dd></dl><p><br/></p>
<h2>See also</h2>
<h3>Related pages</h3>
<ul><li>MSCSSMatrix<a href="/css/transforms/MSCSSMatrix">MSCSSMatrix</a></li></ul>
