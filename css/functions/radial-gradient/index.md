{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=Often different radial gradient syntax can be used to produce the same results. For instance, all three of the following examples, when applied to a 250×150-pixel [[html/elements/div|'''div''']] element, produce the image shown here.



<span codelanguage{{=}}"CSS"><table>
<tr>
<th>CSS</th>
</tr>
<tr>
<td>
<pre>
background-image: radial-gradient(yellow, blue);

background-image: radial-gradient(ellipse at center, yellow 0%, blue 100%);

background-image: radial-gradient(farthest-corner at 50% 50%, yellow, blue);</pre>
</td>
</tr>
</table></span>

The following example is similar to the previous example, but a circular gradient has been specified.



<span codelanguage{{=}}"CSS"><table>
<tr>
<th>CSS</th>
</tr>
<tr>
<td>
<pre>background-image: radial-gradient(circle, yellow, blue);</pre>
</td>
</tr>
</table></span>

The following example has three colors specified. Either of the declarations produces the image here.



<span codelanguage{{=}}"CSS"><table>
<tr>
<th>CSS</th>
</tr>
<tr>
<td>
<pre>background-image: radial-gradient(#FFF133, #16D611, #00A3EF);

background-image: radial-gradient(ellipse at center, #FFF133 0%, #16D611 50%, #00A3EF 100%);</pre>
</td>
</tr>
</table></span>

Of course, you can also originate the radial gradient in locations other than the center of the gradient box. Use the '''closest-side''' or '''farthest-side''' keywords to size the gradient so that the ending shape meets either the closest or farthest side, respectively, of the gradient box.
|LiveURL=
|Code=
background-image: radial-gradient(farthest-side at left bottom, #FFF133, #16D611 100px, #00A3EF);
}}
{{Single_Example
|Description=The following examples set the center of the gradient at 40px from the left side of the gradient box and 50px from the top side of the gradient box. The first example uses '''closest-side''', so the ending shape of the gradient is defined by the closest sides of the gradient box—namely, the top and left sides.


|LiveURL='
|Code=
background-image: radial-gradient(closest-side at 40px 50px, #FFF133, #16D611, #00A3EF);
}}
{{Single_Example
|Description=The second example uses '''farthest-side''', so the ending shape of the gradient is defined the farthest sides of the gradient box—namely, the right and bottom sides.
|LiveURL=
|Code=
background-image: radial-gradient(farthest-side at 40px 50px, #FFF133, #16D611, #00A3EF);
}}
{{Single_Example
|Description=If you use '''closest-side''' or '''farthest-side''' with circular gradients, the size is determined by the closest side of the gradient box. For the following '''closest-side''' example, that side is the left side.
|LiveURL=
|Code=
background-image: radial-gradient(closest-side circle at 40px 50px, #FFF133, #16D611, #00A3EF);
}}
{{Single_Example
|Description=For the following '''farthest-side''' example, the size of the circle gradient is determined by the right side of the gradient box.
|LiveURL=
|Code=
background-image: radial-gradient(farthest-side circle at 40px 50px, #FFF133, #16D611, #00A3EF);
}}}}
{{Notes_Section
|Notes=
===Remarks===
'''Important'''  The Cascading Style Sheets (CSS) Gradients properties do not require a vendor prefix (that is, "-ms-") to work correctly in Internet Explorer 10. The syntax for the '''radial-gradient''' function given in this topic is different from that supported in previous pre-releases of Internet Explorer 10, which required the "-ms-" prefix. To maximize backward compatibility, those older implementations are still recognized, as described in [[css/properties/-ms-radial-gradient|'''-ms-radial-gradient''']].
|Import_Notes=
===Syntax===
'''radial-gradient'''
<code>('''[''' '''[''' ''
&lt;shape&gt;
'' {{!}}{{!}} ''
&lt;size&gt;
'' ''']''' '''[''' at ''
&lt;position&gt;
'' ''']''' ? ,  '''{{!}}''' at ''
&lt;position&gt;
'' ,  ''']''' ? ''
&lt;color-stop&gt;
'' '''[''' ,  ''
&lt;color-stop&gt;
'' ''']''' +)</code>
===Parameters===
;''position'':Optional value that specifies the center of the gradient. This value can take the same values as the [[css/properties/background-position|'''background-position''']] property. If this value is omitted, it defaults to '''center'''.
;''shape'':Optional value that specifies the ending shape of the gradient. If this value is omitted, the ending shape is a circle if the ''size'' parameter is a single length value, and an ellipse otherwise.<table><tr><th>Value</th><th>Meaning</th></tr><tr><td width{{=}}"40%"><a id{{=}}"ellipse"/><a id{{=}}"ELLIPSE"/><dl><dt>'''ellipse'''</dt></dl></td><td width{{=}}"60%">Indicates gradient is in the shape of an ellipse.</td></tr><tr><td width{{=}}"40%"><a id{{=}}"circle"/><a id{{=}}"CIRCLE"/><dl><dt>'''circle'''</dt></dl></td><td width{{=}}"60%">Indicates gradient is in the shape of an circle.</td></tr></table> 
;''size'':Optional value that specifies the size of the gradient's ending shape. If this value is omitted, it defaults to '''farthest-corner'''.<table><tr><th>Value</th><th>Meaning</th></tr><tr><td width{{=}}"40%"><a id{{=}}"_length_s__"/><a id{{=}}"_LENGTH_S__"/><dl><dt>'''&lt;length(s)&gt;'''</dt></dl></td><td width{{=}}"60%">One or two space-delimited length values or two percentages. If one length value is specified, it indicates the radius of the circle. If two values (length or percent) are specified, the first value represents the horizontal radius, and the second the vertical radius. Percentage values are relative to the corresponding dimension of the gradient box. Percentages can only be used to specify the size of an elliptical gradient, not a circular one.Negative values are invalid. </td></tr><tr><td width{{=}}"40%"><a id{{=}}"closest-side"/><a id{{=}}"CLOSEST-SIDE"/><dl><dt>'''closest-side'''</dt></dl></td><td width{{=}}"60%">For circular gradients, this value indicates that the ending-shape is circle sized so that it exactly meets the side of the box closest to its center. For elliptical gradients, the gradient-shape is an ellipse size so that it exactly meets the vertical and horizontal sides of the box closest to its center.</td></tr><tr><td width{{=}}"40%"><a id{{=}}"closest-corner"/><a id{{=}}"CLOSEST-CORNER"/><dl><dt>'''closest-corner'''</dt></dl></td><td width{{=}}"60%">Sizes the gradient-shape so that it exactly meets the closest corner of the box from its center. For elliptical gradients, the gradient-shape has the same ratio of width to height that it would if '''closest-side''' was specified.</td></tr><tr><td width{{=}}"40%"><a id{{=}}"farthest-side"/><a id{{=}}"FARTHEST-SIDE"/><dl><dt>'''farthest-side'''</dt></dl></td><td width{{=}}"60%">Similar to '''closest-side''', except the gradient-shape is sized to meet the side of the box that is farthest from its center (for circular gradients) or the farthest vertical and horizontal sides (for elliptical gradients).</td></tr><tr><td width{{=}}"40%"><a id{{=}}"farthest-corner"/><a id{{=}}"FARTHEST-CORNER"/><dl><dt>'''farthest-corner'''</dt></dl></td><td width{{=}}"60%">Sizes the gradient-shape so that it exactly meets the farthest corner of the box from its center. For elliptical gradients, the gradient-shape has the same ratio of width to height that it would if '''farthest-side''' was specified.</td></tr></table> 
;''color-stop'':At least two color stops are required. Each color stop has one or two components—a color component and an optional position component. The first component defines the color component of a stop point for the gradient. Each stop point has its own designated color, and the area between each point is filled with a continuous color transition from one to the other. This value can be any supported color value.The second component is an optional percentage or decimal value that indicates where along the gradient ray (similar to a gradient line in a [[css/linear-gradient|'''linear-gradient''']], but from the center outward) to place the color stop. "0%" indicates the start of the gradient ray, and "100%" indicates the point where the gradient ray intersects the ending shape. For instance, a value of "20%" indicates the color stop should be placed at a point 20% of the length of the gradient ray, starting from the beginning of the line. Values can be negative, which indicates that the specified color for that value is at mid-transition to the next color at the center of the gradient, so the visible color at the center will be somewhere between the specified color and the next color. Values can be greater than 100%, which specifies a location a correspondingly greater distance from the center of the gradient.
}}
{{See_Also_Section
|Topic_clusters=Gradients
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}