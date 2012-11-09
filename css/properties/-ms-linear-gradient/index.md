{{Page_Title}}
{{Flags
|High-level issues=Merge Candidate, Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Editorial notes={{Editorial/Merge_Candidate
|Other=css/functions/linear-gradient}}
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/Element
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following linear gradient (used as the argument for the [[css/properties/background-image|'''background-image''']] property) has three color stops:
|Code=background-image: -ms-linear-gradient(top right, #FFF133 0%, #16D611 50%, #00A3EF 80%);
|LiveURL=<li>The first color stop is in the top-right corner and defines a gradient line that extends to the bottom-left corner. The first stop is a shade of yellow.</li><li>The second color stop is halfway along the gradient line and is a shade of green.</li><li>The final color stop is 80% of the way along the gradient line and is a shade of blue. From this stop to the end of the gradient line (between 80% and 100%), the color remains this shade of blue.</li>
}}
}}
{{Notes_Section
|Notes====Remarks===
'''Important'''  The '''-ms-linear-gradient()''' function has been superseded by the [[css/linear-gradient|'''linear-gradient''']] function, which does not require the "-ms-" prefix and has a different syntax. Though the '''-ms-linear-gradient()''' function is still recognized by Internet Explorer 10, Microsoft encourages you to use the [[css/linear-gradient|'''linear-gradient''']] function, as it is compliant with the latest version of the [http://go.microsoft.com/fwlink/p/?LinkId{{=}}252389 CSS Image Values and Replaced Content Module Level 3 specification].
The '''-ms-linear-gradient()''' function requires at least two stop points.
|Import_Notes====Syntax===
'''-ms-linear-gradient'''
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
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
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