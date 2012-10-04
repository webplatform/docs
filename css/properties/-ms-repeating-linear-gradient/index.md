{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following declaration creates a repeating linear gradient.
|LiveURL=
|Code=
background-image: -ms-repeating-linear-gradient(top right, #FFF133 0%, #16D611 50%, #00A3EF 80%);
}}}}
{{Notes_Section
|Notes=
===Remarks===
'''Important'''  The '''-ms-repeating-linear-gradient()''' function has been superseded by the [[css/repeating-linear-gradient|'''repeating-linear-gradient''']] function, which does not require the "-ms-" prefix and has a different syntax. Though the '''-ms-repeating-linear-gradient()''' function is still recognized by Internet Explorer 10, Microsoft encourages you to use the [[css/repeating-linear-gradient|'''repeating-linear-gradient''']] function, as it is compliant with the latest version of the [http://go.microsoft.com/fwlink/p/?LinkId{{=}}252389 CSS Image Values and Replaced Content Module Level 3 specification].
Once the last stop point has been reached, the gradient transitions to the first stop point and repeats.
The syntax for the '''-ms-repeating-linear-gradient()''' function is identical to that of the [[css/properties/-ms-linear-gradient|'''-ms-linear-gradient()''']] function.
|Import_Notes=
===Syntax===
'''-ms-repeating-linear-gradient'''
<code>(''
&lt;angle&gt;
'' ''
&lt;starting-point&gt;
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
;''angle'':Optional. The angle the gradient-line should assume, expressed as a number followed by an angle units designator(<code>deg</code>, <code>grad</code>, <code>rad</code>, or <code>turn</code>).For more information about supported angle units,see CSS Values and Units.For instance, 0deg points upwards, 90deg points toward the right, and positive angles go clockwise. If no angle is provided, the gradient line starts in the corner or side specified by ''&lt;starting-point&gt;'' and ends in the opposite corner or side.
;''starting-point'':Optional value that specifies a starting point for the gradient. This value can be one or two of the following keywords.<table><tr><th>Value</th><th>Meaning</th></tr><tr><td width{{=}}"40%"><a id{{=}}"left"/><a id{{=}}"LEFT"/><dl><dt>'''left'''</dt></dl></td><td width{{=}}"60%">First value only. Indicates gradient starts from left.</td></tr><tr><td width{{=}}"40%"><a id{{=}}"right"/><a id{{=}}"RIGHT"/><dl><dt>'''right'''</dt></dl></td><td width{{=}}"60%">First value only. Indicates gradient starts from right.</td></tr><tr><td width{{=}}"40%"><a id{{=}}"top"/><a id{{=}}"TOP"/><dl><dt>'''top'''</dt></dl></td><td width{{=}}"60%">Default. Second value only. Indicates gradient starts from top.</td></tr><tr><td width{{=}}"40%"><a id{{=}}"bottom"/><a id{{=}}"BOTTOM"/><dl><dt>'''bottom'''</dt></dl></td><td width{{=}}"60%">Second value only. Indicates gradient starts from bottom.</td></tr></table> 
;''stop-color'':Required. Defines the color component of a stop point for the gradient. Each stop point has its own designated color, and the area between each point is filled with a continuous color transition from one to the other. This value can be any supported color value, as described in CSS Values and Units.
;''stop-offset'':Optional percentage or decimal value that indicates where along the gradient line to place the color stop.
}}
{{See_Also_Section
|Topic_clusters=Gradients, Deprecated
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}