---
title: '@media'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: '@media'
  topic: css
notes:
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Sets the media types for a set of rules in a styleSheet object.'
tags:
  - CSS
  - At
  - Rules
uri: css/atrules/@media

---
<p>
</p>
<h2>Summary</h2>
<p>
Sets the media types for a set of rules in a styleSheet object.</p>
<h2>Examples</h2>
<p>In the following example,  the <b>@media</b> rule is used to specify the <a href="/css/properties/font-size"><b>font-size</b></a> attribute of the <b>body</b> element for two media types.
</p>
<div class="example">
<pre class="css">
// For computer screens, the font size is 12pt.
@media screen {
   BODY {font-size:12pt;}
}
// When printed, the font size is 8pt.
@media print {
   BODY {font-size:8pt;}
}

</pre>
<p><br/></p>
</div>
<p>The following declaration is a typical media query. In this case, <code>screen</code> indicates the target media type, and <code>max-width</code> is the target media property. The declaration states that the specified rules (no border on <b>div</b> elements) are only to be applied when the page is displayed on a screen in a browser window with a width of at most 400 pixels.
</p>
<div class="example">
<pre class="css">
@media screen and (max-width:400px) {
   div {border:none;}
}

</pre>
<p><br/></p>
</div>
<p>You can use media properties together to create even more specific queries, such as the following. This declaration applies the specified rules when the medium is a screen and the browser window has a width of no more than 400 pixels <i>and</i> a height of no more than 600 pixels.
</p>
<div class="example">
<pre class="css">
@media screen and (max-width:400px) and (max-height:600px) {
   ...
}

</pre>
<p><br/></p>
</div>
<h2>Notes</h2>
<h3>Remarks</h3>
<p>The rule has no default value.
Dynamic HTML (DHTML) expressions can be used in place of the preceding value(s). As of Windows Internet Explorer 8, expressions are not supported in IE8 Standards mode. For more information, see About Dynamic Properties.
Windows Internet Explorer 9 introduces support for media queries. Media queries enable you to scope a style sheet to a set of precise device capabilities. For instance, you might want to design pages differently for users browsing on a mobile device (that has a very small screen, limited color palette, low resolution, and so on) versus a netbook (that has a small screen, full color palette, high resolution, and so on) versus a standard computer (that has a large screen, full color palette, high resolution, and so on).
A media query consists of a media type (<i>sMediaType</i>) and zero or more expressions (<i>sMediaFeatures</i>) that check for the conditions of particular media features. A media query is a logical expression that is either true or false. A media query is true if the media type of the media query matches the media type of the computer on which Windows Internet Explorer is running, and all expressions in the media query are true. The following media features are supported:
</p>
<ul><li><a href="/css/media_queries/width">width</a></li>
<li><a href="/css/media_queries/height">height</a></li>
<li><a href="/css/media_queries/device-width">device-width</a></li>
<li><a href="/css/media_queries/device-height">device-height</a></li>
<li><a href="/css/media_queries/orientation">orientation</a></li>
<li><a href="/css/media_queries/aspect-ratio">aspect-ratio</a></li>
<li><a href="/css/media_queries/device-aspect-ratio">device-aspect-ratio</a></li>
<li><a href="/css/media_queries/colors_by">color</a></li>
<li><a href="/css/media_queries/color-index">color-index</a></li>
<li><a href="/css/media_queries/monochrome">monochrome</a></li>
<li><a href="/css/media_queries/resolution">resolution</a></li></ul><h3>Syntax</h3>
<p><code><b>@media </b><i>sMediaType</i> { <i>Media-Rule</i><b>+</b> }</code>
<b>Media-Rule</b>
<code><b>@media </b><i>sRules</i></code>
</p>
<h3>Parameters</h3>
<dl><dt><i>sMediaType</i></dt>
<dd><b>String</b> that specifies one of the following media types:<table><tr><th>Value</th><th>Meaning</th></tr><tr><td width="40%">&lt;a id="screen"/&gt;&lt;a id="SCREEN"/&gt;<dl><dt><b>screen</b></dt></dl></td><td width="60%">Output is intended for computer screens.</td></tr><tr><td width="40%">&lt;a id="print"/&gt;&lt;a id="PRINT"/&gt;<dl><dt><b>print</b></dt></dl></td><td width="60%">Output is intended for printed material and for documents viewed in Print Preview mode.</td></tr><tr><td width="40%">&lt;a id="all"/&gt;&lt;a id="ALL"/&gt;<dl><dt><b>all</b></dt></dl></td><td width="60%">Output is intended for all devices.</td></tr></table> </dd>
<dt><i>sRules</i></dt>
<dd><b>String</b> that specifies one or more rules in a <a href="/css/cssom/styleSheet"><b>styleSheet</b></a> object.</dd></dl><h2>Related specifications</h2>

<dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/css3-mediaqueries/">Media Queries</a></dt>
  <dd>Recommendation</dd>
</dl><h2>See also</h2>
<h3>Related pages</h3>
<ul><li>media<a href="/css/cssom/properties/media">media</a></li></ul>
