---
title: '-ms-radial-gradient'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Add summery, specifications, compatibility.'
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/properties
    href: /css/properties
tags:
  - API
  - Object
  - Properties
  - DOM
uri: css/properties/-ms-radial-gradient

---
<p><br/></p>
<div class="editors-only">
<p><b>Needs Summary</b>:   This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article. 
</p>
</div>
<div data-template="API_Object_Property">
<p><br/></p><p><br/></p><p>Property of <a href="/css/properties">css/properties</a><a href="/css/properties">css/properties</a>
</p>
<h2>Syntax</h2>
<pre class="js">
var result = element.-ms-radial-gradient;
element.-ms-radial-gradient = value;
</pre>
<p><br/></p>
</div>
<h2>Examples</h2>
<p>The following radial gradient (used as the argument for the <a href="/css/properties/background-image"><b>background-image</b></a> property) has the same three color stops as the linear gradient example  . This circular gradient’s line begins in the lower-left corner of the box that contains it and ends at the side of the box that is farthest from its center.
</p>
<div class="example">
<pre class="html">
background-image: -ms-radial-gradient(left bottom, circle farthest-side, #F7FF08 0%, #21AD11 50%, #00A3EF 80%);

</pre>
<p><br/></p>
</div>
<p><br/></p>
<div class="example">
<pre class="html">
background-image: -ms-radial-gradient(left bottom, ellipse farthest-side, #F7FF08 0%, #21AD11 50%, #00A3EF 80%);

</pre>
<p>[Simply changing the shape in the previous declaration from <b>circle</b> to <b>ellipse</b> makes the gradient appear as follows: View live example]
</p>
</div>
<h2>Notes</h2>
<h3>Remarks</h3>
<p><b>Important</b>  The <b>-ms-radial-gradient()</b> function has been superseded by the <a href="/css/radial-gradient" class="mw-redirect"><b>radial-gradient</b></a> function, which does not require the "-ms-" prefix and has a different syntax. Though the <b>-ms-radial-gradient()</b> function is still recognized by Internet Explorer 10, Microsoft encourages you to use the <a href="/css/radial-gradient" class="mw-redirect"><b>radial-gradient</b></a> function, as it is compliant with the latest version of the <a rel="nofollow" class="external text" href="http://go.microsoft.com/fwlink/p/?LinkId=252389">CSS Image Values and Replaced Content Module Level 3 specification</a>.
</p>
<h3>Syntax</h3>
<p><b>-ms-radial-gradient</b>
<code>(
&lt;starting-point&gt;
<i> ,  </i>
&lt;shape&gt;
<i> </i>
&lt;size&gt;
<i> ,  </i>
&lt;stop-color&gt;
<i> </i>
&lt;stop-offset&gt;
<i> ,  </i>
&lt;stop-color&gt;
<i> </i>
&lt;stop-offset&gt;
<i> , ...)</i></code>
</p>
<h3>Parameters</h3>
<dl><dt><i>starting-point</i></dt>
<dd>Optional value that specifies a starting point for the gradient. This value can be one or two of the following keywords.<table><tr><th>Value</th><th>Meaning</th></tr><tr><td width="40%">&lt;a id="left"/&gt;&lt;a id="LEFT"/&gt;<dl><dt><b>left</b></dt></dl></td><td width="60%">First value only. Indicates gradient starts from left.</td></tr><tr><td width="40%">&lt;a id="center"/&gt;&lt;a id="CENTER"/&gt;<dl><dt><b>center</b></dt></dl></td><td width="60%">First value only. Indicates gradient starts from center.</td></tr><tr><td width="40%">&lt;a id="right"/&gt;&lt;a id="RIGHT"/&gt;<dl><dt><b>right</b></dt></dl></td><td width="60%">First value only. Indicates gradient starts from right.</td></tr><tr><td width="40%">&lt;a id="top"/&gt;&lt;a id="TOP"/&gt;<dl><dt><b>top</b></dt></dl></td><td width="60%">Default. Second value only. Indicates gradient starts from top.</td></tr><tr><td width="40%">&lt;a id="middle"/&gt;&lt;a id="MIDDLE"/&gt;<dl><dt><b>middle</b></dt></dl></td><td width="60%">Second value only. Indicates gradient starts from middle</td></tr><tr><td width="40%">&lt;a id="bottom"/&gt;&lt;a id="BOTTOM"/&gt;<dl><dt><b>bottom</b></dt></dl></td><td width="60%">Second value only. Indicates gradient starts from bottom.</td></tr></table> </dd>
<dt><i>shape</i></dt>
<dd>Optional value that specifies the shape of the gradient.<table><tr><th>Value</th><th>Meaning</th></tr><tr><td width="40%">&lt;a id="ellipse"/&gt;&lt;a id="ELLIPSE"/&gt;<dl><dt><b>ellipse</b></dt></dl></td><td width="60%">Indicates gradient is in the shape of an ellipse.</td></tr><tr><td width="40%">&lt;a id="circle"/&gt;&lt;a id="CIRCLE"/&gt;<dl><dt><b>circle</b></dt></dl></td><td width="60%">Indicates gradient is in the shape of an circle.</td></tr></table> </dd>
<dt><i>size</i></dt>
<dd>Optional value that specifies the size relative to the box closest to its center. Its possible values are either two space-delimited length values (or percentages) or one of the following keywords.<table><tr><th>Value</th><th>Meaning</th></tr><tr><td width="40%">&lt;a id="lengths"/&gt;&lt;a id="LENGTHS"/&gt;<dl><dt><b>lengths</b></dt></dl></td><td width="60%">Two space-delimited length values or percentages.</td></tr><tr><td width="40%">&lt;a id="closest-side"/&gt;&lt;a id="CLOSEST-SIDE"/&gt;<dl><dt><b>closest-side</b></dt></dl></td><td width="60%">For circular gradients, this value indicates that the ending-shape is circle sized so that it exactly meets the side of the box closest to its center. For elliptical gradients, the gradient-shape is an ellipse size so that it exactly meets the vertical and horizontal sides of the box closest to its center.</td></tr><tr><td width="40%">&lt;a id="closest-corner"/&gt;&lt;a id="CLOSEST-CORNER"/&gt;<dl><dt><b>closest-corner</b></dt></dl></td><td width="60%">Sizes the gradient-shape so that it exactly meets the closest corner of the box from its center. For elliptical gradients, the gradient-shape has the same ratio of width to height that it would if <b>closest-side</b> were specified.</td></tr><tr><td width="40%">&lt;a id="farthest-side"/&gt;&lt;a id="FARTHEST-SIDE"/&gt;<dl><dt><b>farthest-side</b></dt></dl></td><td width="60%">Similar to <b>closest-side</b>, except the gradient-shape is sized to meet the side of the box that is farthest from its center (for circular gradients) or the farthest vertical and horizontal sides (for elliptical gradients).</td></tr><tr><td width="40%">&lt;a id="farthest-corner"/&gt;&lt;a id="FARTHEST-CORNER"/&gt;<dl><dt><b>farthest-corner</b></dt></dl></td><td width="60%">Sizes the gradient-shape so that it exactly meets the farthest corner of the box from its center. For elliptical gradients, the gradient-shape has the same ratio of width to height that it would if <b>farthest-side</b> were specified.</td></tr><tr><td width="40%">&lt;a id="contain"/&gt;&lt;a id="CONTAIN"/&gt;<dl><dt><b>contain</b></dt></dl></td><td width="60%">Same as <b>closest-side</b>.</td></tr><tr><td width="40%">&lt;a id="cover"/&gt;&lt;a id="COVER"/&gt;<dl><dt><b>cover</b></dt></dl></td><td width="60%">Default. Same as <b>farthest-corner</b>.</td></tr></table> </dd>
<dt><i>stop-color</i></dt>
<dd>Required. Defines the color component of a stop point for the gradient. Each stop point has its own designated color, and the area between each point is filled with a continuous color transition from one to the other. This value can be any supported color value, as described in CSS Values and Units.</dd>
<dt><i>stop-offset</i></dt>
<dd>Optional percentage or decimal value that indicates where along the gradient line (from the center outward) to place the color stop. For instance, a value of 20% or 0.2 indicates the color stop should be placed at a point 20% of the length of the gradient line, starting from the beginning of the line.</dd></dl><p><br/></p>
<h2>See also</h2>
<h3>Related articles</h3>
<h4>Deprecated</h4>
<ul><li> <strong class="selflink">-ms-radial-gradient</strong></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/-ms-repeating-linear-gradient">-ms-repeating-linear-gradient</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/-ms-repeating-radial-gradient">-ms-repeating-radial-gradient</a></li></ul><p><br/></p>
<ul><li> <a href="/dom/MutationEvent">MutationEvent</a></li></ul><p><br/></p>
<ul><li> <a href="/dom/MutationEvent/attrChange">attrChange</a></li></ul><p><br/></p>
<ul><li> <a href="/dom/MutationEvent/attrName">attrName</a></li></ul><p><br/></p>
<ul><li> <a href="/dom/MutationEvent/initMutationEvent">initMutationEvent</a></li></ul><p><br/></p>
<ul><li> <a href="/dom/MutationEvent/newValue">newValue</a></li></ul><p><br/></p>
<ul><li> <a href="/dom/MutationEvent/prevValue">prevValue</a></li></ul><p><br/></p>
<ul><li> <a href="/dom/MutationEvent/relatedNode">relatedNode</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/!DOCTYPE">!DOCTYPE</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/!DOCTYPE/ja">!DOCTYPE</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/acronym">acronym</a></li></ul><p><br/></p>
<ul><li> <a href="/javascript/escape">escape</a></li></ul><p><br/></p>
<ul><li> <a href="/javascript/unescape">unescape</a></li></ul><h4>Gradients</h4>
<ul><li> <a href="/css/functions/linear-gradient">linear-gradient</a></li></ul><p><br/></p>
<ul><li> <a href="/css/functions/radial-gradient">css/functions/radial-gradient</a></li></ul><p><br/></p>
<ul><li> <a href="/css/functions/repeating-linear-gradient">repeating-linear-gradient</a></li></ul><p><br/></p>
<ul><li> <a href="/css/functions/repeating-radial-gradient">repeating-radial-gradient</a></li></ul><p><br/></p>
<ul><li> <strong class="selflink">-ms-radial-gradient</strong></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/-ms-repeating-linear-gradient">-ms-repeating-linear-gradient</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/-ms-repeating-radial-gradient">-ms-repeating-radial-gradient</a></li></ul>
