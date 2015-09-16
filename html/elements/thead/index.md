---
title: 'thead'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: thead
  topic: html
notes:
  - 'Should have automatic child links generated.'
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLTableSectionElement](/dom/HTMLTableSectionElement)'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The thead element  (&lt;thead&gt;) identifies header rows at the top of a table, usually containing column labels.  It may contain one or more rows of &lt;th&gt; or &lt;td&gt; cells.'
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/thead

---
<p>
</p>
<h2>Summary</h2>
<p>
The thead element  (&amp;lt;thead&amp;gt;) identifies header rows at the top of a table, usually containing column labels.  It may contain one or more rows of &amp;lt;th&amp;gt; or &amp;lt;td&amp;gt; cells.</p><p><br/></p>
<h2>Overview Table</h2>

<dl><dt><a href="/dom/interface"> DOM Interface</a></dt>
  <dd><a href="/dom/HTMLTableSectionElement">HTMLTableSectionElement</a></dd>
</dl><h2>Examples</h2>
<p>The following code example uses the <i>thead'</i> element and the <a href="/html/elements/table"><b>table</b></a>, <a href="/html/elements/tbody"><b>tbody</b></a>, <a href="/html/elements/td"><b>td</b></a>, and <a href="/html/elements/tr"><b>tr</b></a> elements to create a table that includes the first row in the table header and the second row in the table body.
</p>
<div class="example">
<pre class="html">
&lt;table&gt;
&lt;thead&gt;
  &lt;tr&gt;
    &lt;th scope="col"&gt;Player&lt;/th&gt;
    &lt;th scope="col"&gt;Position&lt;/th&gt;
  &lt;/tr&gt;
&lt;/thead&gt;
&lt;tbody&gt;
  &lt;tr&gt;
    &lt;td&gt;James, Lebron&lt;/td&gt;
    &lt;td&gt;SF&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;Wade, Dwayne&lt;/td&gt;
    &lt;td&gt;SG&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;Bosh, Chris&lt;/td&gt;
    &lt;td&gt;PF&lt;/td&gt;
  &lt;/tr&gt;
&lt;/tbody&gt;
&lt;/table&gt;

</pre>
<p><br/></p>
</div>
<h2>Notes</h2>
<h3>Remarks</h3>
<p>Valid tags within the <b>THEAD</b> element include:
</p>
<ul><li><b>td</b> * chances are should be a th not a td, and scope of column</li>
<li><b>th</b></li>
<li><b>tr</b></li></ul><p>You can specify only one <b>thead</b> object specified for any given <a href="/html/elements/table"><b>table</b></a> object.
The <a href="/html/elements/table"><b>table</b></a> object and its associated elements have a separate table object model, which uses different methods than the general object model.
</p>
<h3>Standards information</h3>
<ul><li><a rel="nofollow" class="external text" href="http://go.microsoft.com/fwlink/p/?linkid=196991">Document Object Model (DOM) Level 2 HTML Specification</a>, Section 1.6.5</li>
<li><a rel="nofollow" class="external text" href="http://go.microsoft.com/fwlink/p/?linkid=25320">HTML 4.01 Specification</a>, Section 11.2.3</li></ul><p><br/></p><p> 
</p>
<h2>Related specifications</h2>

<dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/html51/tabular-data.html#the-thead-element">HTML 5.1</a></dt>
  <dd>W3C Working Draft</dd>
</dl><dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/html5/tabular-data.html#the-thead-element">HTML 5</a></dt>
  <dd>W3C Recommendation</dd>
</dl><dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/html401/struct/tables.html#edef-THEAD">HTML 4.01</a></dt>
  <dd>W3C Recommendation</dd>
</dl>
