---
title: 'outline-width'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://code.webplatform.org/gist/5579241'
compatibility:
  feature: outline-width
  topic: css
notes:
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`medium`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'absolute length; ‘0’ if the outline style is ‘none’.'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`outlineWidth`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The outline-width property sets the width of the outline of an element. An outline is a line that is drawn around elements, outside the border edge, to make the element stand out.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/outline-width

---
<p>
</p>
<h2>Summary</h2>
<p>
The outline-width property sets the width of the outline of an element. An outline is a line that is drawn around elements, outside the border edge, to make the element stand out.</p>
<h2>Overview table</h2>

<dl><dt><a href="/css/concepts/initial_value"> Initial value</a></dt>
  <dd><code>medium</code></dd>
</dl><dl><dt>Applies to</dt>
  <dd>All elements</dd>
</dl><dl><dt><a href="/css/concepts/inherited"> Inherited</a></dt>
  <dd>No</dd>
</dl><dl><dt>Media</dt>
  <dd>visual</dd>
</dl><dl><dt><a href="/css/concepts/computed_value"> Computed value</a></dt>
  <dd>absolute length; ‘0’ if the outline style is ‘none’.</dd>
</dl><dl><dt>Animatable</dt>
  <dd>Yes</dd>
</dl><dl><dt><a href="/css/concepts/cssom"> CSS Object Model Property</a></dt>
  <dd><code>outlineWidth</code></dd>
</dl><dl><dt>Percentages</dt>
  <dd>N/A</dd>
</dl><h2>Syntax</h2>
<ul><li>

<code>outline-width: &lt;width&gt;</code>
</li>
	<li>

<code>outline-width: inherit</code>
</li>
	<li>

<code>outline-width: medium</code>
</li>
	<li>

<code>outline-width: thick</code>
</li>
	<li>

<code>outline-width: thin</code>
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
<dd> Floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For more information about the supported length units, see CSS Values and Units Reference.</dd></dl><p><br/></p>
<dl><dt>inherit</dt>
<dd> This is a keyword indicating that the value is inherited from their parent's element calculated value.</dd></dl><p><br/></p>
<h2>Examples</h2>
<p>A simple example showing multiple &lt;span&gt;s.
</p>
<div class="example">
<pre class="html">
&lt;div class="all"&gt;
    &lt;p&gt;
      &lt;span class="medium"&gt;Medium&lt;/span&gt;
    &lt;/p&gt;
    &lt;p&gt;
      &lt;span class="thin"&gt;Thin&lt;/span&gt;
    &lt;/p&gt;
    &lt;p&gt;
      &lt;span class="thick"&gt;Thick&lt;/span&gt;
    &lt;/p&gt;
    &lt;p&gt;
      &lt;span class="width"&gt;10px&lt;/span&gt;
    &lt;/p&gt;
&lt;/div&gt;

</pre>
<p><a rel="nofollow" class="external text" href="http://code.webplatform.org/gist/5579241">View live example</a>
</p>
</div>
<p>CSS outline width values.
</p>
<div class="example">
<pre class="css">
.all {
  background-color: lightgrey;
}

.all p {
  padding: 20px;
}
  
.all span {
  padding: 10px;
  margin: 10px 10px 10px 10px;
  font-size: 36px;
  font-family: Bitter;
  outline-style: solid;
}

.all .medium {
  outline-width: medium;
}

.all .thin {
  outline-width: thin;
}

.all .thick {
  outline-width: thick;
}

.all .width {
  outline-width: 10px;
}

</pre>
<p><a rel="nofollow" class="external text" href="http://code.webplatform.org/gist/5579241">View live example</a>
</p>
</div>
<h2>Notes</h2>
<ul><li> Displaying an outline does not cause reflow, no matter how wide the outline is. The outline frame is drawn over an element, and does not influence the position or size of the box, or of any other boxes.</li>
<li> The <a href="/css/properties/outline">outline</a> property is a shorthand property for setting one or more of the individual outline properties <a href="/css/properties/outline-style">outline-style</a>, <strong class="selflink">outline-width</strong> and <a href="/css/properties/outline-color">outline-color</a> in a single rule. In most cases the use of this shortcut is preferable and more convenient.</li></ul><p><br/></p>
<h2>Related specifications</h2>

<dl><dt><a rel="nofollow" class="external text" href="http://dev.w3.org/csswg/css-ui/#outline-width0">CSS Basic User Interface Module Level 3 (CSS3 UI)</a></dt>
  <dd>Working Draft</dd>
</dl>
