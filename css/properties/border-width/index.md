---
title: 'border-width'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://code.webplatform.org/gist/733bf352438f33914fc0'
compatibility:
  feature: border-width
  topic: css
notes:
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`medium, for all 4 values`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'An absolute length, for all 4 values; 0 if the border style is ''none'' or ''hidden'''
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`borderWidth`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Sets the width of an element''s four borders. This property can have from one to four values. This is a shorthand property for setting values simultaneously for border-top-width, border-right-width, border-bottom-width, and border-left-width.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/border-width

---
<p>
</p>
<h2>Summary</h2>
<p>
Sets the width of an element's four borders. This property can have from one to four values. This is a shorthand property for setting values simultaneously for border-top-width, border-right-width, border-bottom-width, and border-left-width.</p>
<h2>Overview table</h2>

<dl><dt><a href="/css/concepts/initial_value"> Initial value</a></dt>
  <dd><code>medium, for all 4 values</code></dd>
</dl><dl><dt>Applies to</dt>
  <dd>All elements</dd>
</dl><dl><dt><a href="/css/concepts/inherited"> Inherited</a></dt>
  <dd>No</dd>
</dl><dl><dt>Media</dt>
  <dd>visual</dd>
</dl><dl><dt><a href="/css/concepts/computed_value"> Computed value</a></dt>
  <dd>An absolute length, for all 4 values; 0 if the border style is 'none' or 'hidden'</dd>
</dl><dl><dt>Animatable</dt>
  <dd>Yes</dd>
</dl><dl><dt><a href="/css/concepts/cssom"> CSS Object Model Property</a></dt>
  <dd><code>borderWidth</code></dd>
</dl><dl><dt>Percentages</dt>
  <dd>N/A</dd>
</dl><h2>Syntax</h2>
<ul><li>

<code>border-width: &lt;border-top-width&gt; &lt;border-right-width&gt; &lt;border-bottom-width&gt; &lt;border-left-width&gt;</code>
</li>
	<li>

<code>border-width: &lt;width&gt;</code>
</li>
	<li>

<code>border-width: medium</code>
</li>
	<li>

<code>border-width: thick</code>
</li>
	<li>

<code>border-width: thin</code>
</li>
</ul><p><br/></p>
<h2>Values</h2>
<dl><dt>medium</dt>
<dd> Default.  </dd></dl><p><br/></p>
<dl><dt>thin</dt>
<dd> Less than the default width.</dd></dl><p><br/></p>
<dl><dt>thick</dt>
<dd> Greater than the default width.</dd></dl><p><br/></p>
<dl><dt>&lt;width&gt;</dt>
<dd> Floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For more information about the supported length units, see [<a rel="nofollow" class="external text" href="http://www.w3.org/TR/css3-background/#the-border-width%7CCSS">Values and Units Reference</a>].</dd></dl><p><br/></p>
<dl><dt>&lt;border-top-width&gt; &lt;border-right-width&gt; &lt;border-bottom-width&gt; &lt;border-left-width&gt;</dt>
<dd> Shorthand syntax. See notes below.</dd></dl><p><br/></p>
<h2>Examples</h2>
<p>CSS border width values.
</p>
<div class="example">
<pre class="css">
.medium {
  border-width: medium;
}

.thin {
  border-width: thin;
}

.thick {
  border-width: thick;
}

.width {
  border-width: 10px;
}

.various {
  border-width: thick medium thin 10px;
}

</pre>
<p><a rel="nofollow" class="external text" href="http://code.webplatform.org/gist/733bf352438f33914fc0">View live example</a>
</p>
</div>
<h2>Usage</h2>
<pre> * Up to four different widths can be specified, in the following order: top, right, bottom, left. 
</pre>
<ul><li> If one width is specified, it is used for all four sides. If two widths are specified, the first is used for the top and bottom borders, and the second is used for left and right borders. If three widths are specified, they are used for top, right/left, and bottom borders, respectively. If left is missing, it is the same as right; if bottom is missing, it is the same as top; if right is missing, it is the same as top.</li></ul><p><br/></p>
<h2>Related specifications</h2>

<dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/css3-background/#the-border-width">CSS Level 3 - Backgrounds and Borders Module</a></dt>
  <dd>Candidate Recommendation</dd>
</dl><h2>See also</h2>
<h3>Related articles</h3>
<h4>Border</h4>
<ul><li> <a href="/css/properties/border">border</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/border-bottom">border-bottom</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/border-bottom-color">border-bottom-color</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/border-bottom-left-radius">border-bottom-left-radius</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/border-bottom-style">border-bottom-style</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/border-bottom-width">border-bottom-width</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/border-color">border-color</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/border-image">border-image</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/border-image-outset">border-image-outset</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/border-image-repeat">border-image-repeat</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/border-image-slice">border-image-slice</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/border-image-source">border-image-source</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/border-image-width">border-image-width</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/border-left">border-left</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/border-left-color">border-left-color</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/border-left-style">border-left-style</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/border-left-width">border-left-width</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/border-radius">border-radius</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/border-right">border-right</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/border-right-color">border-right-color</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/border-right-style">border-right-style</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/border-right-width">border-right-width</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/border-top">border-top</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/border-top-color">border-top-color</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/border-top-left-radius">border-top-left-radius</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/border-top-right-radius">border-top-right-radius</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/border-top-style">border-top-style</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/border-top-width">border-top-width</a></li></ul><p><br/></p>
<ul><li> <strong class="selflink">border-width</strong></li></ul>
