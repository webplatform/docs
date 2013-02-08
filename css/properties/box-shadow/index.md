{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The ‘box-shadow’ property attaches one or more shadows inside or outside of a box-model element_ The property is a comma-separated list of shadows, each specified by 2-4 length values, an optional color, and an optional ‘inset’ keyword_ This simple effect can be manipulated to generate complex effects_

Given a box, the shadow style is represented as follows:

<pre><shadow>=inset? && [ <length>{2,4} && <color>? ]</pre>
}}
{{CSS Property
|Initial value=none
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=any <length> made absolute; any specified color computed; otherwise as specified
|Animatable=No
|CSS object model property=boxShadow
|CSS percentages=???
|Values={{CSS Property Value
|Data Type=[[css/properties/border-style#inset|'''inset''']]
|Description=If not specified (default), the shadow is assumed to be a drop shadow (as if the box were raised above the content). The presence of the inset keyword changes the shadow to one inside the frame (as if the content was depressed inside the box). Inset shadows are drawn inside the border (even transparent ones), above the background, but below content.
}}{{CSS Property Value
|Data Type=<offset-x> <offset-y>
|Description=These are two <length> values to set the shadow offset. <offset-x> specifies the horizontal distance. Negative values place the shadow to the left of the element. <offset-y> specifies the vertical distance. Negative values place the shadow above the element. See <length> for possible units. If both values are 0, the shadow is placed behind the element (and may generate a blur effect if <blur-radius> and/or <spread-radius> is set).
}}{{CSS Property Value
|Data Type=<blur-radius>
|Description=This is a third <length> value. The larger this value, the bigger the blur, so the shadow becomes bigger and lighter. Negative values are not allowed. If not specified, it will be 0 (the shadow's edge is sharp).
}}{{CSS Property Value
|Data Type=<spread-distance>
|Description=This is a fourth <length> value. Positive values will cause the shadow to expand and grow bigger, negative values will cause the shadow to shrink. If not specified, it will be 0 (the shadow will be the same size as the element). For inner shadows, expanding the shadow (creating more shadow area) means contracting the shadow's perimeter shape.
}}{{CSS Property Value
|Data Type=<color>
|Description=See <color> values for possible keywords and notations. If not specified, the color used depends on the browser - it is usually the value of the color property, but note that Safari currently paints a transparent shadow in this case.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=&lt;article&gt;
	&lt;h1&gt;Drop Shadows - Web Platform Docs Examples&lt;/h1&gt;
	&lt;p&gt;Examples of Drop Shadows&lt;/p&gt;
	&lt;footer role=&quot;contentinfo&quot;&gt;
		&lt;a href=&quot;http://docs.webplatform.org/wiki/css/properties/box-shadow&quot;&gt;Learn more about Drop Shadows&lt;/a&gt;
	&lt;/footer&gt;
&lt;/article&gt;
}}{{Single Example
|Language=CSS
|Description=An example of a basic Drop Shadow
|Code=article {
/* box-shadow: left-offset top-offset blur color; */
   box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
}
|LiveURL=http://dabblet.com/gist/4739446
}}{{Single Example
|Language=CSS
|Description=An example of inner drop shadows
|Code=article {
/* box-shadow: left-offset top-offset blur color; */
   box-shadow: 0 0 10px rgba(0, 0, 0, 0.5) inset;
}
|LiveURL=http://dabblet.com/gist/4739547
}}{{Single Example
|Language=CSS
|Description=An example of how a positive spread distance length value affects the drop shadow
|Code=article {
/* box-shadow: left-offset top-offset blur spread color; */
   box-shadow: 0 0 5px 10px rgba(0, 0, 0, 0.5);
}
|LiveURL=http://dabblet.com/gist/4739759
}}{{Single Example
|Language=CSS
|Description=Negative values cause the shadow shape to contract.
|Code=article {
/* box-shadow: left-offset top-offset blur spread color; */
   box-shadow: 0 20px 5px -10px rgba(0, 0, 0, 0.5);
}
|LiveURL=http://dabblet.com/gist/4739654
}}{{Single Example
|Language=CSS
|Description=If the blur value is zero, the shadow's edge is sharp.
|Code=article {
/* box-shadow: left-offset top-offset blur spread color; */
   box-shadow: 0 0 0 5px rgba(0, 0, 0, 0.5);
}
|LiveURL=http://dabblet.com/gist/4739845
}}{{Single Example
|Language=CSS
|Description=If the box has a nonzero ‘border-radius’, the shadow shape is rounded in the same way.
|Code=article {
/* box-shadow: left-offset top-offset blur color; */
   box-shadow: 0 0 10px rgba(0, 0, 0, 1);
	
   border-radius: 10px;
}
|LiveURL=http://dabblet.com/gist/4740320
}}
}}
{{Notes_Section
|Usage=The ‘box-shadow’ property attaches one or more drop-shadows to the box. The property is a comma-separated list of shadows, each specified by 2-4 length values, an optional color, and an optional ‘inset’ keyword. Omitted lengths are 0; omitted colors are a UA-chosen color. 

An outer box-shadow casts a shadow as if the border-box of the element were opaque. The shadow is drawn outside the border edge only: it is clipped inside the border-box of the element.

An inner box-shadow casts a shadow as if everything outside the padding edge were opaque. The inner shadow is drawn inside the padding edge only: it is clipped outside the padding box of the element.

If the box has a nonzero ‘border-radius’, the shadow shape is rounded in the same way. The ‘border-image’ does not affect the shape of the box-shadow.

If a spread distance is defined, the shadow is expanded outward or contracted inward by an operation equivalent to applying the absolute value of the spread value to a blur operation as defined below and thresholding the result such that for a positive spread distance all non-transparent pixels are given the full shadow color and for a negative spread distance all non-opaque pixels are made transparent. The UA may approximate this operation by taking an outward outset of the specified amount normal to the original shadow perimeter. Alternatively the UA may approximate the transformed shadow perimeter shape by outsetting (insetting, for inner shadows) the shadow's straight edges by the spread distance and increasing (decreasing, for inner shadows) and flooring at zero the corner radii by the same amount. (The UA may even combine these methods, using one method for outer shadows and another for inner ones.) For corners with a zero border-radius, however, the corner must remain sharp—the operation is equivalent to scaling the shadow shape. In any case, the effective width and height of the shadow shape is floored at zero. (A zero-sized shadow shape would cause an outer shadow to disappear, and an inner shadow to cover the entire padding-box.)

A non-zero blur distance indicates that the resulting shadow should be blurred, such as by a Gaussian filter. The exact algorithm is not defined; however the resulting shadow must approximate (with each pixel being within 5% of its expected value) the image that would be generated by applying to the shadow a Gaussian blur with a standard deviation equal to half the blur radius

Note this means for a long, straight shadow edge, the blur radius will create a visibly apparent color transition approximately the twice length of the blur radius that is perpendicular to and centered on the shadow's edge, and that ranges from the full shadow color at the endpoint inside the shadow to fully transparent at the endpoint outside it.

====Remarks===
The '''box-shadow''' property can specify one or more drop shadows. The components of each shadow are interpreted as follows:
*Required: The first length is the ''horizontal offset'' of the shadow. A positive value draws a shadow that is offset to the right of the box, a negative length to the left.
*Required: The second length is the ''vertical offset''. A positive value offsets the shadow down, a negative one up.
*Optional: The third length is a ''blur distance''. Negative values are not allowed. If the blur value is zero, the shadow's edge is sharp. Otherwise, the larger the value, the more the shadow's edge is blurred.
*Optional: The fourth length is a ''spread distance''. Positive values cause the shadow shape to expand in all directions by the specified radius. Negative values cause the shadow shape to contract.
*Optional: The ''color'' is the color of the shadow.
*Optional: An <code>inset</code> keyword, if present, changes the drop shadow from an outer shadow (one that shadows the box onto the canvas, as if it were lifted above the canvas) to an inner shadow (one that shadows the canvas onto the box, as if the box were cut out of the canvas and shifted behind it).
|Import_Notes====Syntax===
<code>
''box-shadow:  ''none '''{{!}}''' ''offset-x offset-y (blur-radius) (spread-radius) (color) (inset)''
</code>


<syntaxhighlight lang="xml">
<text x="12px" y="12px" font-family="sans-serif" font-size="120%"/>
</syntaxhighlight>
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}