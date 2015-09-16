---
title: 'outline-offset'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5579301'
compatibility:
  feature: outline-offset
  topic: css
notes:
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`0`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': '\<length\> value in absolute units (px or physical).'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`outlineOffset`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The outline-offset property offsets the outline and draw it beyond the border edge.'
tags:
  - CSS
  - Properties
uri: css/properties/outline-offset

---
<p>
</p>
<h2>Summary</h2>
<p>
The outline-offset property offsets the outline and draw it beyond the border edge.</p>
<h2>Overview table</h2>

<dl><dt><a href="/css/concepts/initial_value"> Initial value</a></dt>
  <dd><code>0</code></dd>
</dl><dl><dt>Applies to</dt>
  <dd>All elements</dd>
</dl><dl><dt><a href="/css/concepts/inherited"> Inherited</a></dt>
  <dd>No</dd>
</dl><dl><dt>Media</dt>
  <dd>visual</dd>
</dl><dl><dt><a href="/css/concepts/computed_value"> Computed value</a></dt>
  <dd>&lt;length&gt; value in absolute units (px or physical).</dd>
</dl><dl><dt>Animatable</dt>
  <dd>Yes</dd>
</dl><dl><dt><a href="/css/concepts/cssom"> CSS Object Model Property</a></dt>
  <dd><code>outlineOffset</code></dd>
</dl><dl><dt>Percentages</dt>
  <dd>N/A</dd>
</dl><h2>Syntax</h2>
<ul><li>

<code>outline-offset: &lt;length&gt;</code>
</li>
	<li>

<code>outline-offset: inherit</code>
</li>
</ul><p><br/></p>
<h2>Values</h2>
<dl><dt>&lt;length&gt;</dt>
<dd> Floating-point number, followed by an absolute units designator (cm, mm, in, pt, or pc) or a relative units designator (em, ex, or px). For more information about the supported length units, see CSS Values and Units Reference (Length). </dd></dl><p><br/></p>
<dl><dt>inherit</dt>
<dd> This is a keyword indicating that the value is inherited from their parent's element calculated value.</dd></dl><p><br/></p>
<h2>Examples</h2>
<p>A simple example showing multiple &lt;span&gt;s with border and outline.
</p>
<div class="example">
<pre class="html">
&lt;div class="all"&gt;
    &lt;p&gt;
      &lt;span class="one"&gt;One&lt;/span&gt;
    &lt;/p&gt;
    &lt;p&gt;
      &lt;span class="two"&gt;Two&lt;/span&gt;
    &lt;/p&gt;
    &lt;p&gt;
      &lt;span class="three"&gt;Three&lt;/span&gt;
    &lt;/p&gt;
&lt;/div&gt;

</pre>
<p><a rel="nofollow" class="external text" href="http://code.webplatform.org/gist/5579301">View live example</a>
</p>
</div>
<p><br/></p>
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
  border: red solid 3px;
  outline: blue solid 3px;
}

.all .one {
  outline-offset: 0px;
}

.all .two {
  outline-offset: 5px;
}

.all .three {
  outline-offset: 0.2em;
}

</pre>
<p><a rel="nofollow" class="external text" href="http://code.webplatform.org/gist/5579301">View live example</a>
</p>
</div>
<h2>Usage</h2>
<pre> If the computed value of ‘outline-offset’ is anything other than 0, then the outline is outset from the border edge by that amount.
</pre>
<p><br/></p>
<h2>Related specifications</h2>

<dl><dt><a rel="nofollow" class="external text" href="http://dev.w3.org/csswg/css-ui/#outline-offset0">CSS Basic User Interface Module Level 3 (CSS3 UI)</a></dt>
  <dd>Working Draft</dd>
</dl>
