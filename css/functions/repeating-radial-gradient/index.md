---
title: 'repeating-radial-gradient'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/functions/
    href: '/w/index.php?title=css/functions/&action=edit&redlink=1'
tags:
  - API
  - Object
  - Properties
  - DOM
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - css/functions/
uri: css/functions/repeating-radial-gradient

---
<p><br/></p>
<div class="editors-only">
<p><b>Needs Summary</b>:   This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article. 
</p>
</div>
<div data-template="API_Object_Property">
<p><br/></p><p><br/></p><p>Property of <a href="/w/index.php?title=css/functions/&amp;action=edit&amp;redlink=1" class="new">css/functions/</a><a href="/w/index.php?title=css/functions/&amp;action=edit&amp;redlink=1" class="new">css/functions/</a>
</p>
<h2>Syntax</h2>
<pre class="js">
var result = element.repeating-radial-gradient;
element.repeating-radial-gradient = value;
</pre>
<p><br/></p>
</div>
<h2>Examples</h2>
<p>The following declaration creates a repeating circular gradient.
</p>
<div class="example">
<pre class="html">
background-image: repeating-radial-gradient(closest-side circle at 40px 50px, #FFF133, #16D611, #00A3EF);

</pre>
<p><br/></p>
</div>
<p><br/></p>
<div class="example">
<pre class="html">
background-image: repeating-radial-gradient(closest-side at 40px 50px, #FFF133, #16D611, #00A3EF, #FFF133);

</pre>
<p>[The following declaration creates a repeating elliptical gradient. View live example]
</p>
</div>
<h2>Notes</h2>
<h3>Remarks</h3>
<p>Once the last color stop has been reached, the gradient starts again at the first color stop and repeats. It's a good idea to specify identical colors for the first and last color stops to prevent abrupt color changes between each repeating group.
The syntax for the <b>repeating-radial-gradient</b> function is identical to that of the <a href="/css/radial-gradient" class="mw-redirect"><b>radial-gradient</b></a> function.
<b>Important</b>  The Cascading Style Sheets (CSS) Gradients properties do not require a vendor prefix (that is, "-ms-") to work correctly in Internet Explorer 10. The syntax for the <b>repeating-radial-gradient</b> function given in this topic is different from that supported in previous pre-releases of Internet Explorer 10, which required the "-ms-" prefix. To maximize backward compatibility, those older implementations are still recognized, as described in <a href="/css/properties/-ms-repeating-radial-gradient"><b>-ms-repeating-radial-gradient</b></a>.
</p>
<h3>Syntax</h3>
<p><b>repeating-radial-gradient</b>
<code>(<b>[</b> <b>[</b> 
&lt;shape&gt;
<i> || </i>
&lt;size&gt;
<i> <b>]</b> <b>[</b> at </i>
&lt;position&gt;
<i> <b>]</b> ? ,  <b>|</b> at </i>
&lt;position&gt;
<i> ,  <b>]</b> ? </i>
&lt;color-stop&gt;
<i> <b>[</b> ,  </i>
&lt;color-stop&gt;
<i> <b>]</b> +)</i></code>
</p>
<h3>Parameters</h3>
<dl><dt><i>position</i></dt>
<dd>Optional value that specifies the center of the gradient. This value can take the same values as the <a href="/css/properties/background-position"><b>background-position</b></a> property. If this value is omitted, it defaults to <b>center</b>.</dd>
<dt><i>shape</i></dt>
<dd>Optional value that specifies the ending shape of the gradient. If this value is omitted, the ending shape is a circle if the <i>size</i> parameter is a single length value, and an ellipse otherwise.<table><tr><th>Value</th><th>Meaning</th></tr><tr><td width="40%">&lt;a id="ellipse"/&gt;&lt;a id="ELLIPSE"/&gt;<dl><dt><b>ellipse</b></dt></dl></td><td width="60%">Indicates gradient is in the shape of an ellipse.</td></tr><tr><td width="40%">&lt;a id="circle"/&gt;&lt;a id="CIRCLE"/&gt;<dl><dt><b>circle</b></dt></dl></td><td width="60%">Indicates gradient is in the shape of an circle.</td></tr></table> </dd>
<dt><i>size</i></dt>
<dd>Optional value that specifies the size of the gradient's ending shape. If this value is omitted, it defaults to <b>farthest-corner</b>.<table><tr><th>Value</th><th>Meaning</th></tr><tr><td width="40%">&lt;a id="_length_s__"/&gt;&lt;a id="_LENGTH_S__"/&gt;<dl><dt><b>&lt;length(s)&gt;</b></dt></dl></td><td width="60%">One or two space-delimited length values or two percentages. If one length value is specified, it indicates the radius of the circle. If two values (length or percent) are specified, the first value represents the horizontal radius, and the second the vertical radius. Percentage values are relative to the corresponding dimension of the gradient box. Percentages can only be used to specify the size of an elliptical gradient, not a circular one.Negative values are invalid. </td></tr><tr><td width="40%">&lt;a id="closest-side"/&gt;&lt;a id="CLOSEST-SIDE"/&gt;<dl><dt><b>closest-side</b></dt></dl></td><td width="60%">For circular gradients, this value indicates that the ending-shape is circle sized so that it exactly meets the side of the box closest to its center. For elliptical gradients, the gradient-shape is an ellipse size so that it exactly meets the vertical and horizontal sides of the box closest to its center.</td></tr><tr><td width="40%">&lt;a id="closest-corner"/&gt;&lt;a id="CLOSEST-CORNER"/&gt;<dl><dt><b>closest-corner</b></dt></dl></td><td width="60%">Sizes the gradient-shape so that it exactly meets the closest corner of the box from its center. For elliptical gradients, the gradient-shape has the same ratio of width to height that it would if <b>closest-side</b> was specified.</td></tr><tr><td width="40%">&lt;a id="farthest-side"/&gt;&lt;a id="FARTHEST-SIDE"/&gt;<dl><dt><b>farthest-side</b></dt></dl></td><td width="60%">Similar to <b>closest-side</b>, except the gradient-shape is sized to meet the side of the box that is farthest from its center (for circular gradients) or the farthest vertical and horizontal sides (for elliptical gradients).</td></tr><tr><td width="40%">&lt;a id="farthest-corner"/&gt;&lt;a id="FARTHEST-CORNER"/&gt;<dl><dt><b>farthest-corner</b></dt></dl></td><td width="60%">Sizes the gradient-shape so that it exactly meets the farthest corner of the box from its center. For elliptical gradients, the gradient-shape has the same ratio of width to height that it would if <b>farthest-side</b> was specified.</td></tr></table> </dd>
<dt><i>color-stop</i></dt>
<dd>At least two color stops are required. Each color stop has one or two components—a color component and an optional position component. The first component defines the color component of a stop point for the gradient. Each stop point has its own designated color, and the area between each point is filled with a continuous color transition from one to the other. This value can be any supported color value.The second component is an optional percentage or decimal value that indicates where along the gradient ray (similar to a gradient line in a <a href="/css/linear-gradient" class="mw-redirect"><b>linear-gradient</b></a>, but from the center outward) to place the color stop. "0%" indicates the start of the gradient ray, and "100%" indicates the point where the gradient ray intersects the ending shape. For instance, a value of "20%" indicates the color stop should be placed at a point 20% of the length of the gradient ray, starting from the beginning of the line. Values can be negative, which indicates that the specified color for that value is at mid-transition to the next color at the center of the gradient, so the visible color at the center will be somewhere between the specified color and the next color. Values can be greater than 100%, which specifies a location a correspondingly greater distance from the center of the gradient.</dd></dl><p><br/></p>
<h2>See also</h2>
<h3>Related articles</h3>
<h4>Gradients</h4>
<ul><li> <a href="/css/functions/linear-gradient">linear-gradient</a></li></ul><p><br/></p>
<ul><li> <a href="/css/functions/radial-gradient">css/functions/radial-gradient</a></li></ul><p><br/></p>
<ul><li> <a href="/css/functions/repeating-linear-gradient">repeating-linear-gradient</a></li></ul><p><br/></p>
<ul><li> <strong class="selflink">repeating-radial-gradient</strong></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/-ms-radial-gradient">-ms-radial-gradient</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/-ms-repeating-linear-gradient">-ms-repeating-linear-gradient</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/-ms-repeating-radial-gradient">-ms-repeating-radial-gradient</a></li></ul>
