{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=css/functions/
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following declaration creates a repeating circular gradient.
|Code=background-image: repeating-radial-gradient(closest-side circle at 40px 50px, #FFF133, #16D611, #00A3EF);
}}{{Single Example
|Code=background-image: repeating-radial-gradient(closest-side at 40px 50px, #FFF133, #16D611, #00A3EF, #FFF133);
|LiveURL=The following declaration creates a repeating elliptical gradient.
}}
}}
{{Notes_Section
|Notes====Remarks===
Once the last color stop has been reached, the gradient starts again at the first color stop and repeats. It's a good idea to specify identical colors for the first and last color stops to prevent abrupt color changes between each repeating group.
The syntax for the '''repeating-radial-gradient''' function is identical to that of the [[css/radial-gradient|'''radial-gradient''']] function.
'''Important'''  The Cascading Style Sheets (CSS) Gradients properties do not require a vendor prefix (that is, "-ms-") to work correctly in Internet Explorer 10. The syntax for the '''repeating-radial-gradient''' function given in this topic is different from that supported in previous pre-releases of Internet Explorer 10, which required the "-ms-" prefix. To maximize backward compatibility, those older implementations are still recognized, as described in [[css/properties/-ms-repeating-radial-gradient|'''-ms-repeating-radial-gradient''']].
|Import_Notes====Syntax===
'''repeating-radial-gradient'''
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
{{See_Also_Section
|Topic_clusters=Gradients
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}