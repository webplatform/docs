---
title: 'toString'
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
  - API
  - Object
  - Methods
  - DOM
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - css/cssom/MSCSSMatrix
    - css/MSCSSMatrix/apis/properties/a
uri: css/cssom/MSCSSMatrix/methods/toString

---
<p><br/></p>
<div class="editors-only">
<p><b>Needs Summary</b>:   This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article. 
</p>
</div>
<p>Method of <a href="/w/index.php?title=css/cssom/MSCSSMatrix&amp;action=edit&amp;redlink=1" class="new">css/cssom/MSCSSMatrix</a><a href="/w/index.php?title=css/cssom/MSCSSMatrix&amp;action=edit&amp;redlink=1" class="new">css/cssom/MSCSSMatrix</a>
</p>
<h2>Syntax</h2>
<pre class="js">
var object = object.toString();
</pre>
<p><br/></p>
<h2>Return Value</h2>
<p>Returns an object of type  DOM NodeDOM Node
</p><p>Type: <b>HRESULT</b>
</p><p>This method can return one of these values.
</p>
<table class="wikitable"><tr><th>Return value
</th>
<th>Description
</th></tr><tr><td>S_OK
</td>
<td>The operation completed successfully.
</td></tr></table><p> 
</p><p>DOMString
</p><p>A string value that corresponds to the matrix. This string value contains matrix(, followed by a comma-and-whitespace-delimited list of matrix values, followed by ).
</p><p>For a 2-D transform matrix, the matrix value list is ordered <a href="/w/index.php?title=css/MSCSSMatrix/apis/properties/a&amp;action=edit&amp;redlink=1" class="new"><b>a</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/b"><b>b</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/c"><b>c</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/d"><b>d</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/e"><b>e</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/f"><b>f</b></a>.
</p><p>For a 3-D transform matrix, the matrix value list is ordered <a href="/css/cssom/MSCSSMatrix/properties/m11"><b>m11</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m21"><b>m21</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m31"><b>m31</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m41"><b>m41</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m12"><b>m12</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m22"><b>m22</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m32"><b>m32</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m42"><b>m42</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m13"><b>m13</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m23"><b>m23</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m33"><b>m33</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m43"><b>m43</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m14"><b>m14</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m24"><b>m24</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m34"><b>m34</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m44"><b>m44</b></a>.
</p>
<div class="editors-only">
<p><b>Needs Examples</b>:  This section should include examples. 
</p>
</div>
<p><br/></p>
<h3>Syntax</h3>
<h3>Standards information</h3>
<ul><li><a rel="nofollow" class="external text" href="http://go.microsoft.com/fwlink/p/?linkid=223140">CSS Transitions Module Level 3</a>, Section 10.1</li></ul><p><br/></p>
<h3>Parameters</h3>
<dl><dt><i>matrixString</i> [out, retval]</dt>
<dd>Type: <b>DOMString</b>A string value that corresponds to the matrix. This string value contains <code>matrix(</code>, followed by a comma-and-whitespace-delimited list of matrix values, followed by <code>)</code>.<table><tr><th>Value</th><th>Meaning</th></tr><tr><td width="40%">&lt;a id="matrix_a__b__c__d__e__f_"/&gt;&lt;a id="MATRIX_A__B__C__D__E__F_"/&gt;<dl><dt><b>matrix(a, b, c, d, e, f)</b></dt></dl></td><td width="60%">For a 2-D transform matrix, the matrix value list is ordered <a href="/w/index.php?title=css/MSCSSMatrix/apis/properties/a&amp;action=edit&amp;redlink=1" class="new"><b>a</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/b"><b>b</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/c"><b>c</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/d"><b>d</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/e"><b>e</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/f"><b>f</b></a>.</td></tr><tr><td width="40%">&lt;a id="matrix_m11__m21__m31__m41__m12__m22__m32__m42__m13__m23__m33__m43__m14__m24__m34__m44_"/&gt;&lt;a id="MATRIX_M11__M21__M31__M41__M12__M22__M32__M42__M13__M23__M33__M43__M14__M24__M34__M44_"/&gt;<dl><dt><b>matrix(m11, m21, m31, m41, m12, m22, m32, m42, m13, m23, m33, m43, m14, m24, m34, m44)</b></dt></dl></td><td width="60%">For a 3-D transform matrix, the matrix value list is ordered <a href="/css/cssom/MSCSSMatrix/properties/m11"><b>m11</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m21"><b>m21</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m31"><b>m31</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m41"><b>m41</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m12"><b>m12</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m22"><b>m22</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m32"><b>m32</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m42"><b>m42</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m13"><b>m13</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m23"><b>m23</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m33"><b>m33</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m43"><b>m43</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m14"><b>m14</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m24"><b>m24</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m34"><b>m34</b></a>, <a href="/css/cssom/MSCSSMatrix/properties/m44"><b>m44</b></a>.</td></tr></table> </dd></dl><p><br/></p>
<h2>See also</h2>
<h3>Related pages</h3>
<ul><li>MSCSSMatrix<a href="/css/transforms/MSCSSMatrix">MSCSSMatrix</a></li></ul>
