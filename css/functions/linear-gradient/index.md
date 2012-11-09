{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS_Function}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=background: #1e5799;
background: -moz-linear-gradient(top, #1e5799 0%, #7db9e8 100%);
background: -webkit-gradient(linear, left top, left bottom, color-stop(0%,#1e5799), color-stop(100%,#7db9e8));
background: -webkit-linear-gradient(top, #1e5799 0%,#7db9e8 100%);
background: -o-linear-gradient(top, #1e5799 0%,#7db9e8 100%);
background: -ms-linear-gradient(top, #1e5799 0%,#7db9e8 100%);
background: linear-gradient(to bottom, #1e5799 0%,#7db9e8 100%);
filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#1e5799', endColorstr='#7db9e8',GradientType=0 );
|LiveURL=http://jsfiddle.net/denbuzze/J2CLV/
}}
}}
{{Notes_Section
|Notes====Remarks===
'''Important'''  The Cascading Style Sheets (CSS) Gradients properties do not require a vendor prefix (that is, "-ms-") to work correctly in Internet Explorer 10. The syntax for the '''linear-gradient''' function given in this topic is different from that supported in previous pre-releases of Internet Explorer 10, which required the "-ms-" prefix. To maximize backward compatibility, those older implementations are still recognized, as described in [[css/properties/-ms-linear-gradient|'''-ms-linear-gradient''']].
|Import_Notes====Syntax===
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
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Yes
|Internet_explorer_prefixed_version=10
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Gradients
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}