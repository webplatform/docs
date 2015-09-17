---
title: 'address'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: address
  topic: html
notes:
  - 'Add syntax, attribute, example, compatibility.'
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLElement](/dom/HTMLElement)'
readiness: 'Not Ready'
summary: 'The address element (&lt;address&gt;) encloses contact information of the owner or the author of the document or the article.'
tags:
  - Markup_Elements
  - HTML
uri: html/elements/address

---
<p><br/></p>
<h2>Summary</h2>
<p>
The address element (&amp;lt;address&amp;gt;) encloses contact information of the owner or the author of the document or the article.</p><p><br/></p>
<h2>Overview Table</h2>

<dl><dt><a href="/dom/interface"> DOM Interface</a></dt>
  <dd><a href="/dom/HTMLElement">HTMLElement</a></dd>
</dl><ul><li> The address element must not be used to represent arbitrary addresses, unless those addresses are in fact the relevant contact information.</li>
<li> The address element must not contain information other than contact information.</li>
<li> Typically, the address element would be included along with other information in a footer element.</li></ul><h2>Examples</h2>
<p>A page at the W3C Web site might include the following contact information
</p>
<div class="example">
<pre class="html">
&lt;address&gt;
    &lt;p&gt;&lt;a href="http://www.w3.org/Consortium/contact-mit"&gt;MIT&lt;/a&gt;&lt;/p&gt;
&lt;/address&gt;

</pre>
<p><br/></p>
</div>
<p>Example of information that would be incorrect if placed inside an address element
</p>
<div class="example">
<pre class="html">
&lt;div&gt;Last Modified: 1999/12/24 23:37:50&lt;/div&gt;

</pre>
<p><br/></p>
</div>
<h2>Notes</h2>
<p>Webkit (Safari, old Android and similar) and Trident (Internet Explorer) user agent default style -
</p>
<pre>address {
	display:block;
	font-style: italic;
}</pre>
<p>Gecko (Firefox) user agent default style -
</p>
<pre>address, address[dir]{
         unicode-bidi: -moz-isolate;
         display:block;
         font-style:italic;
}</pre>
<h3>Standards information</h3>
<ul><li><a rel="nofollow" class="external text" href="http://go.microsoft.com/fwlink/p/?linkid=25320">HTML 4.01 Specification</a>, Section 7.5.6</li></ul><p><br/></p>
<h3>HTML information</h3>
<table class="wikitable"><tr><th>Closing Tag
</th>
<td>required
</td></tr><tr><th>CSS Display
</th>
<td>block
</td></tr></table><p> 
</p>
<h2>Related specifications</h2>

<dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/html51/sections.html#the-address-element">HTML 5.1</a></dt>
  <dd>W3C Working Draft</dd>
</dl><dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/html5/sections.html#the-address-element">HTML 5</a></dt>
  <dd>W3C Recommendation</dd>
</dl><dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/html401/struct/global.html#edef-ADDRESS">HTML 4.01</a></dt>
  <dd>W3C Recommendation</dd>
</dl>
