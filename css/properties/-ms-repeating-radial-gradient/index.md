{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add summery, specifications, compatibility.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=css/properties
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following declaration creates a repeating circular gradient.
|Code=background-image: -ms-repeating-radial-gradient(left bottom,circle farthest-side, #F7FF08 0%, #21AD11 10%, #00A3EF 20%);
}}{{Single Example
|Code=background-image: -ms-repeating-radial-gradient(left bottom,ellipse farthest-side, #F7FF08 0%, #21AD11 10%, #00A3EF 20%);
|LiveURL=The following declaration creates a repeating elliptical gradient.
}}
}}
{{Notes_Section
|Notes====Remarks===
'''Important'''  The '''-ms-repeating-radial-gradient()''' function has been superseded by the [[css/repeating-radial-gradient|'''repeating-radial-gradient''']] function, which does not require the "-ms-" prefix and has a different syntax. Though the '''-ms-repeating-radial-gradient()''' function is still recognized by Internet Explorer 10, Microsoft encourages you to use the [[css/repeating-radial-gradient|'''repeating-radial-gradient''']] function, as it is compliant with the latest version of the [http://go.microsoft.com/fwlink/p/?LinkId{{=}}252389 CSS Image Values and Replaced Content Module Level 3 specification].
Once the last stop point has been reached, the gradient transitions to the first stop point and repeats.
The syntax for the '''-ms-repeating-radial-gradient()''' function is identical to that of the [[css/properties/-ms-radial-gradient|'''-ms-radial-gradient()''']] function.
|Import_Notes====Syntax===
'''-ms-repeating-radial-gradient'''
<code>(''
&lt;starting-point&gt;
'' ,  ''
&lt;shape&gt;
'' ''
&lt;size&gt;
'' ,  ''
&lt;stop-color&gt;
'' ''
&lt;stop-offset&gt;
'' ,  ''
&lt;stop-color&gt;
'' ''
&lt;stop-offset&gt;
'' , ...)</code>
===Parameters===
;''starting-point'':Optional value that specifies a starting point for the gradient. This value can be one or two of the following keywords.<table><tr><th>Value</th><th>Meaning</th></tr><tr><td width{{=}}"40%"><a id{{=}}"left"/><a id{{=}}"LEFT"/><dl><dt>'''left'''</dt></dl></td><td width{{=}}"60%">First value only. Indicates gradient starts from left.</td></tr><tr><td width{{=}}"40%"><a id{{=}}"center"/><a id{{=}}"CENTER"/><dl><dt>'''center'''</dt></dl></td><td width{{=}}"60%">First value only. Indicates gradient starts from center.</td></tr><tr><td width{{=}}"40%"><a id{{=}}"right"/><a id{{=}}"RIGHT"/><dl><dt>'''right'''</dt></dl></td><td width{{=}}"60%">First value only. Indicates gradient starts from right.</td></tr><tr><td width{{=}}"40%"><a id{{=}}"top"/><a id{{=}}"TOP"/><dl><dt>'''top'''</dt></dl></td><td width{{=}}"60%">Default. Second value only. Indicates gradient starts from top.</td></tr><tr><td width{{=}}"40%"><a id{{=}}"middle"/><a id{{=}}"MIDDLE"/><dl><dt>'''middle'''</dt></dl></td><td width{{=}}"60%">Second value only. Indicates gradient starts from middle</td></tr><tr><td width{{=}}"40%"><a id{{=}}"bottom"/><a id{{=}}"BOTTOM"/><dl><dt>'''bottom'''</dt></dl></td><td width{{=}}"60%">Second value only. Indicates gradient starts from bottom.</td></tr></table> 
;''shape'':Optional value that specifies the shape of the gradient.<table><tr><th>Value</th><th>Meaning</th></tr><tr><td width{{=}}"40%"><a id{{=}}"ellipse"/><a id{{=}}"ELLIPSE"/><dl><dt>'''ellipse'''</dt></dl></td><td width{{=}}"60%">Indicates gradient is in the shape of an ellipse.</td></tr><tr><td width{{=}}"40%"><a id{{=}}"circle"/><a id{{=}}"CIRCLE"/><dl><dt>'''circle'''</dt></dl></td><td width{{=}}"60%">Indicates gradient is in the shape of an circle.</td></tr></table> 
;''size'':Optional value that specifies the size relative to the box closest to its center. Its possible values are either two space-delimited length values (or percentages) or one of the following keywords.<table><tr><th>Value</th><th>Meaning</th></tr><tr><td width{{=}}"40%"><a id{{=}}"lengths"/><a id{{=}}"LENGTHS"/><dl><dt>'''lengths'''</dt></dl></td><td width{{=}}"60%">Two space-delimited length values or percentages.</td></tr><tr><td width{{=}}"40%"><a id{{=}}"closest-side"/><a id{{=}}"CLOSEST-SIDE"/><dl><dt>'''closest-side'''</dt></dl></td><td width{{=}}"60%">For circular gradients, this value indicates that the ending-shape is circle sized so that it exactly meets the side of the box closest to its center. For elliptical gradients, the gradient-shape is an ellipse size so that it exactly meets the vertical and horizontal sides of the box closest to its center.</td></tr><tr><td width{{=}}"40%"><a id{{=}}"closest-corner"/><a id{{=}}"CLOSEST-CORNER"/><dl><dt>'''closest-corner'''</dt></dl></td><td width{{=}}"60%">Sizes the gradient-shape so that it exactly meets the closest corner of the box from its center. For elliptical gradients, the gradient-shape has the same ratio of width to height that it would if '''closest-side''' were specified.</td></tr><tr><td width{{=}}"40%"><a id{{=}}"farthest-side"/><a id{{=}}"FARTHEST-SIDE"/><dl><dt>'''farthest-side'''</dt></dl></td><td width{{=}}"60%">Similar to '''closest-side''', except the gradient-shape is sized to meet the side of the box that is farthest from its center (for circular gradients) or the farthest vertical and horizontal sides (for elliptical gradients).</td></tr><tr><td width{{=}}"40%"><a id{{=}}"farthest-corner"/><a id{{=}}"FARTHEST-CORNER"/><dl><dt>'''farthest-corner'''</dt></dl></td><td width{{=}}"60%">Sizes the gradient-shape so that it exactly meets the farthest corner of the box from its center. For elliptical gradients, the gradient-shape has the same ratio of width to height that it would if '''farthest-side''' were specified.</td></tr><tr><td width{{=}}"40%"><a id{{=}}"contain"/><a id{{=}}"CONTAIN"/><dl><dt>'''contain'''</dt></dl></td><td width{{=}}"60%">Same as '''closest-side'''.</td></tr><tr><td width{{=}}"40%"><a id{{=}}"cover"/><a id{{=}}"COVER"/><dl><dt>'''cover'''</dt></dl></td><td width{{=}}"60%">Default. Same as '''farthest-corner'''.</td></tr></table> 
;''stop-color'':Required. Defines the color component of a stop point for the gradient. Each stop point has its own designated color, and the area between each point is filled with a continuous color transition from one to the other. This value can be any supported color value, as described in CSS Values and Units.
;''stop-offset'':Optional percentage or decimal value that indicates where along the gradient line (from the center outward) to place the color stop. For instance, a value of 20% or 0.2 indicates the color stop should be placed at a point 20% of the length of the gradient line, starting from the beginning of the line.
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
|Topic_clusters=Deprecated, Gradients
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}