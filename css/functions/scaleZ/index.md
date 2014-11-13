{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Defines a 3D scale transformation by giving a value for the Z-axis.}}
{{CSS_Function
|Content=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following code snippet is an example of the '''scaleZ''' function in use as applied to a square blue [[html/elements/div|'''div''']] element along with the [[css/functions/perspective()|'''perspective''']] function (which simulates depth) and the [[css/functions/rotateX()|'''rotateX''']] function.
|Code=div {
  transform: perspective(500px) scaleZ(2) rotateX(45deg);
}
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
The effect of the '''scaleZ''' function is most evident when used in combination with functions such as the [[css/functions/perspective()|'''perspective''']] and [[css/functions/rotate()|'''rotate''']] (and related) functions.
|Import_Notes====Syntax===
'''scaleZ'''
<code>(''
&lt;scaling-value-z&gt;
'')</code>
===Parameters===
;''scaling-value-z'':Numerical value by which to scale the specified element in the ''z''-direction.

}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Transforms Module Level 3
|URL=http://www.w3.org/TR/css3-transforms/
|Status=Working Draft
|Relevant_changes=
}}
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