{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples=}}
{{Notes_Section
|Notes=
===Remarks===
'''Important'''  The Cascading Style Sheets (CSS) Gradients properties do not require a vendor prefix (that is, "-ms-") to work correctly in Internet Explorer 10. The syntax for the '''linear-gradient''' function given in this topic is different from that supported in previous pre-releases of Internet Explorer 10, which required the "-ms-" prefix. To maximize backward compatibility, those older implementations are still recognized, as described in [[css/properties/-ms-linear-gradient|'''-ms-linear-gradient''']].
|Import_Notes=
===Syntax===
'''linear-gradient'''
<code>('''[''' '''[''' ''
&lt;angle&gt;
'' '''{{!}}''' to ''
&lt;side-or-corner&gt;
'' ''']''' , ''']''' ? ''
&lt;color-stop&gt;
'' '''[''' ,  ''
&lt;color-stop&gt;
'' ''']''' +)</code>
===Parameters===
;''angle'':Optional. The angle the gradient line should assume, expressed as a number followed by an angle units designator(for instance, "deg")."0deg" points upward and positive angles increase in a clockwise direction. Therefore, "90deg" points toward the right, "180deg" points downward, and so on.If no angle is provided, the gradient line starts in the corner or side opposite the corner or side specified by ''&lt;side-or-corner&gt;''.
;''side-or-corner'':Optional value that specifies an ending corner or side for the gradient. This value begins with "to", which is followed by one or two of the following keywords. Including one keyword specifies an ending side, and two keywords specify an ending corner. <ul><li>The following values can be used as the first value only:<ul><li>'''left'''   Indicates gradient ends on the left.</li><li>'''right'''   Indicates gradient ends on the  right.</li></ul></li><li>The following values can be used as the second value only:<ul><li>'''top'''   Indicates gradient ends on the top.</li><li>'''bottom'''   Indicates gradient ends on the  bottom.</li></ul></li><li>Not including any keywords or angle is equivalent to "to bottom".</li></ul>
;''color-stop'':At least two color stops are required. Each color stop has one or two components—a color component and an optional position component. The first component defines the color component of a stop point for the gradient. Each stop point has its own designated color, and the area between each point is filled with a continuous color transition from one to the other. This value can be any supported color value.Each stop point can have an optional percentage or supported length value that indicates where along the gradient line to place the color stop. "0%" (or "0px", "0em", and so on) indicates the starting point (or side); "100%" indicates the ending point (or side).
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