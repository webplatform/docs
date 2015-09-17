---
title: '-ms-repeating-linear-gradient'
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
  - API_Object_Properties
  - DOM
  - Needs_Summary
uri: css/properties/-ms-repeating-linear-gradient

---
<p><br/></p>

<div data-template="API_Object_Property">
<p><br/></p><p><br/></p><p>Property of <a href="/css/properties">css/properties</a><a href="/css/properties">css/properties</a>
</p>
<h2>Syntax</h2>
<pre class="js">
var result = element.-ms-repeating-linear-gradient;
element.-ms-repeating-linear-gradient = value;
</pre>
<p><br/></p>
</div>
<h2>Examples</h2>
<p>The following declaration creates a repeating linear gradient.
</p>
<div class="example">
<pre class="html">
background-image: -ms-repeating-linear-gradient(top right, #FFF133 0%, #16D611 50%, #00A3EF 80%);

</pre>
<p><br/></p>
</div>
<h2>Notes</h2>
<h3>Remarks</h3>
<p><b>Important</b>  The <b>-ms-repeating-linear-gradient()</b> function has been superseded by the <a href="/css/repeating-linear-gradient" class="mw-redirect"><b>repeating-linear-gradient</b></a> function, which does not require the "-ms-" prefix and has a different syntax. Though the <b>-ms-repeating-linear-gradient()</b> function is still recognized by Internet Explorer 10, Microsoft encourages you to use the <a href="/css/repeating-linear-gradient" class="mw-redirect"><b>repeating-linear-gradient</b></a> function, as it is compliant with the latest version of the <a rel="nofollow" class="external text" href="http://go.microsoft.com/fwlink/p/?LinkId=252389">CSS Image Values and Replaced Content Module Level 3 specification</a>.
Once the last stop point has been reached, the gradient transitions to the first stop point and repeats.
The syntax for the <b>-ms-repeating-linear-gradient()</b> function is identical to that of the <a href="/css/properties/-ms-linear-gradient" class="mw-redirect"><b>-ms-linear-gradient()</b></a> function.
</p>
<h3>Syntax</h3>
<p><b>-ms-repeating-linear-gradient</b>
<code>(
&lt;angle&gt;
<i> </i>
&lt;starting-point&gt;
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
<dl><dt><i>angle</i></dt>
<dd>Optional. The angle the gradient-line should assume, expressed as a number followed by an angle units designator(<code>deg</code>, <code>grad</code>, <code>rad</code>, or <code>turn</code>).For more information about supported angle units,see CSS Values and Units.For instance, 0deg points upwards, 90deg points toward the right, and positive angles go clockwise. If no angle is provided, the gradient line starts in the corner or side specified by <i>&lt;starting-point&gt;</i> and ends in the opposite corner or side.</dd>
<dt><i>starting-point</i></dt>
<dd>Optional value that specifies a starting point for the gradient. This value can be one or two of the following keywords.<table><tr><th>Value</th><th>Meaning</th></tr><tr><td width="40%">&lt;a id="left"/&gt;&lt;a id="LEFT"/&gt;<dl><dt><b>left</b></dt></dl></td><td width="60%">First value only. Indicates gradient starts from left.</td></tr><tr><td width="40%">&lt;a id="right"/&gt;&lt;a id="RIGHT"/&gt;<dl><dt><b>right</b></dt></dl></td><td width="60%">First value only. Indicates gradient starts from right.</td></tr><tr><td width="40%">&lt;a id="top"/&gt;&lt;a id="TOP"/&gt;<dl><dt><b>top</b></dt></dl></td><td width="60%">Default. Second value only. Indicates gradient starts from top.</td></tr><tr><td width="40%">&lt;a id="bottom"/&gt;&lt;a id="BOTTOM"/&gt;<dl><dt><b>bottom</b></dt></dl></td><td width="60%">Second value only. Indicates gradient starts from bottom.</td></tr></table> </dd>
<dt><i>stop-color</i></dt>
<dd>Required. Defines the color component of a stop point for the gradient. Each stop point has its own designated color, and the area between each point is filled with a continuous color transition from one to the other. This value can be any supported color value, as described in CSS Values and Units.</dd>
<dt><i>stop-offset</i></dt>
<dd>Optional percentage or decimal value that indicates where along the gradient line to place the color stop.</dd></dl><p><br/></p>
<h2>See also</h2>
<h3>Related articles</h3>
<h4>Deprecated</h4>
<ul><li> <a href="/css/properties/-ms-radial-gradient">-ms-radial-gradient</a></li></ul><p><br/></p>
<ul><li> <strong class="selflink">-ms-repeating-linear-gradient</strong></li></ul><p><br/></p>
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
<ul><li> <a href="/css/properties/-ms-radial-gradient">-ms-radial-gradient</a></li></ul><p><br/></p>
<ul><li> <strong class="selflink">-ms-repeating-linear-gradient</strong></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/-ms-repeating-radial-gradient">-ms-repeating-radial-gradient</a></li></ul>
