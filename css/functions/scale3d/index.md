{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Defines a three-dimensional transformation to change the scale of the element by setting specific scaling factors in each of the ''x'', ''y'', and ''z'' directions.  All three parameters must be specified.}}
{{CSS_Function}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following code snippet is an example of the '''scale3d''' function in use. When applied to a square blue [[html/elements/div|'''div''']] element, it has the effect illustrated in the image. (The light-blue square indicates the original position of the transformed element.)
|Code=div {
  transform: scale3d(0.5, -0.5, 1.5);
}
|LiveURL=http://code.webplatform.org/gist/5305309
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
'''scale3d'''
<code>(''
&lt;scaling-value-x&gt;
'' , ''
&lt;scaling-value-y&gt;
'' , ''
&lt;scaling-value-z&gt;
'')</code>
===Parameters===
;''scaling-value-x'':Numerical value by which to scale the specified element in the ''x''-direction.
;''scaling-value-y'':Numerical value by which to scale the specified element in the ''y''-direction.
;''scaling-value-z'':Numerical value by which to scale the specified element in the ''z''-direction.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkID{{=}}223145 CSS Transforms Module, Level 3], Section 13.2
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
|Topic_clusters=Transforms
|Manual_sections====Related pages (MSDN)===
*<code>Transform Functions</code>
*<code>[http://go.microsoft.com/fwlink/p/?LinkId{{=}}256246 Mathematical Description of Transform Functions]</code>
*<code>Direct3D: Matrices</code>
*<code>[http://go.microsoft.com/fwlink/?LinkId{{=}}227893 Hands On: 3-D Transforms]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}