{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS_Function}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following code snippet is an example of the '''rotate3d''' function in use. When applied to a square blue [[html/elements/div|'''div''']] element, it has the effect illustrated in the image. (The light-blue square indicates the original position of the transformed element.)
|Code=div {
   transform: rotate3d(0.7, 0.5, 0.7, 45deg);
}
}}
}}
{{Notes_Section
|Notes====Remarks===
The element rotates by the angle specified in the last parameter, and about the [''x'',''y'',''z''] direction vector described by the first three parameters. If the direction vector is not of unit length, it will be normalized. A direction vector that cannot be normalized, such as [0, 0, 0], results in no rotation.
|Import_Notes====Syntax===
'''rotate3d'''
<code>(''
&lt;number&gt;
'' , ''
&lt;number&gt;
'' , ''
&lt;number&gt;
'' , ''
&lt;angle&gt;
'')</code>
===Parameters===
;''number'':A component of the direction vector about which the element is rotated.
;''angle'':The angle by which the element is rotated. This value is expressed as a number followed by a supported angle unit.
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
===Related pages (HTML5Rocks)===
*<code>[http://www.html5rocks.com/en/tutorials/3d/css/ 3D and CSS]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN, HTML5Rocks
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=http://www.html5rocks.com/en/tutorials/3d/css/
}}