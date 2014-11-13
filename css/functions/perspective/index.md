{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Defines how many pixels away a 3D element is placed from the viewer. This allows you to change the apparent perspective of how 3D elements are viewed.}}
{{CSS_Function
|Content=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=
|Description=The following code snippet is an example of the '''perspective''' function in use. When applied to a square blue [[html/elements/div|'''div''']] element along with the [[css/functions/translateZ()|'''translateZ''']] function (which enables the specified element to appear to have moved away from the viewer), it has the effect illustrated in the image. (The light-blue square indicates the original position of the transformed element.)
|Code=div {    
  transform: perspective(500px) translateZ(-60px);
}
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
The value must be greater than 0 and is given in pixels.

For more information about transformation matrices, see [http://go.microsoft.com/fwlink/p/?LinkId{{=}}256246 Mathematical Description of Transform Functions], in the [http://go.microsoft.com/fwlink/?LinkID{{=}}223145 CSS3 Transforms] specification.
The '''perspective''' function is often necessary for other  3-D transformation functions to have a visible effect.
|Import_Notes====Syntax===
'''perspective'''
<code>(''
&lt;length&gt;
'')</code>
===Parameters===
;''length'':Value in pixels that specifies a perspective projection matrix. This value is expressed as a number followed by "px".
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkID{{=}}223145 CSS Transforms Module, Level 3], Section 13.2
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=
|External_links=
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
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}