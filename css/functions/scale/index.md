{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Summary needed.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS_Function}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following code snippet is an example of the '''scale''' function in use. When applied to a square blue [[html/elements/div|'''div''']] element, it has the effect illustrated in the image. (The light-blue square indicates the original position of the transformed element.)
|Code=div {    
  transform: scale(1.65, 0.6);
}
}}
}}
{{Notes_Section
|Notes====Remarks===
If the second parameter is not provided, it is takes a value equal to the first.
The function '''scale'''(1, 1) leaves the element unchanged, while '''scale'''(2, 2) causes it to appear twice as long in both the ''x''- and ''y''-axes, or four times its original size.
|Import_Notes====Syntax===
'''scale'''
<code>(''
&lt;scaling-value-x&gt;
'' '''[''' , ''
&lt;scaling-value-y&gt;
'' ''']''')</code>
===Parameters===
;''scaling-value-x'':Numerical value by which to scale the specified element in the ''x''-direction.
;''scaling-value-y'':Optional. Numerical value by which to scale the specified element in the ''y''-direction.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkID{{=}}223145 CSS Transforms Module, Level 3], Section 13.1


===Requirements===
{| class="wikitable"
|}
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
*<code>[http://go.microsoft.com/fwlink/?LinkID{{=}}240163 Hands On: 2D Transforms]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}