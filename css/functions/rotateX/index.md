{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Syntax and Examples are in different positions compared to other CSS function pages. 
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
|Description=The following code snippet is an example of the '''rotateX''' function in use. When applied to a square blue [[html/elements/div|'''div''']] element along with the [[css/functions/perspective()|'''perspective''']] function (which simulates depth), it has the effect illustrated in the image. (The light-blue square indicates the original position of the transformed element.)
|Code=div {
  transform: perspective(500px) rotateX(45deg);
}
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''rotateX''' transform function is the same as [[css/functions/rotate3d()|'''rotate3d''']](1, 0, 0, &lt;''angle''&gt;).
|Import_Notes====Syntax===
'''rotateX'''
<code>(''
&lt;angle&gt;
'')</code>
===Parameters===
;''angle'':The angle by which to rotate the element about the ''x''-axis. This value is expressed as a number followed by a supported angle unit.
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