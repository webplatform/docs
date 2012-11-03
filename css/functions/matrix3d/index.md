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
|Description=The following code snippet is an example of the '''matrix3d''' function in use. When applied to a square blue [[html/elements/div|'''div''']] element, it has the effect illustrated in the image.
|Code=div {
  transform: matrix3d(0.359127, -0.469472, 0.806613, 0, 0.190951, 0.882948, 0.428884, 0, -0.913545, 0, 0.406737, 0, 0, 0, 0, 1);
}
}}
}}
{{Notes_Section
|Notes====Remarks===
All other transformation functions are based on the '''matrix3d''' function.
It is a good idea to become familiar with transform coordinate systems and rendering before attempting to specify 3-D transforms manually.
|Import_Notes====Syntax===
'''matrix3d'''
<code>(''
&lt;number&gt;
'' , ''
&lt;number&gt;
'' , ''
&lt;number&gt;
'' , ''
&lt;number&gt;
'' , ''
&lt;number&gt;
'' , ''
&lt;number&gt;
'' , ''
&lt;number&gt;
'' , ''
&lt;number&gt;
'' , ''
&lt;number&gt;
'' , ''
&lt;number&gt;
'' , ''
&lt;number&gt;
'' , ''
&lt;number&gt;
'' , ''
&lt;number&gt;
'' , ''
&lt;number&gt;
'' , ''
&lt;number&gt;
'' , ''
&lt;number&gt;
'')</code>
===Parameters===
;''number'':A matrix value.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkID{{=}}223145 CSS Transforms Module, Level 3], Section 13.2
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Transforms
|Manual_sections====Related pages (MSDN)===
*<code>Transform Functions</code>
*<code>[http://go.microsoft.com/fwlink/p/?LinkId{{=}}256246 Mathematical Description of Transform Functions]</code>
*<code>Direct3D: Matrices</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}