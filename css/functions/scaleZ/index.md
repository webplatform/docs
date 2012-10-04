{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Function
|Content=
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following code snippet is an example of the '''scaleZ''' function in use. When applied to a square blue [[html/elements/div|'''div''']] element along with the [[css/functions/perspective()|'''perspective''']] function (which simulates depth) and the [[css/functions/rotateX()|'''rotateX''']] function, it has the effect illustrated in the image. (The light-blue square indicates the original position of the transformed element.)
|LiveURL=
|Code=
div {
  transform: perspective(500px) scaleZ(2) rotateX(45deg);
}
}}}}
{{Notes_Section
|Notes=
===Remarks===
The effect of the '''scaleZ''' function is most evident when used in combination with functions such as the [[css/functions/perspective()|'''perspective''']] and [[css/functions/rotate()|'''rotate''']] (and related) functions.
|Import_Notes=
===Syntax===
'''scaleZ'''
<code>(''
&lt;scaling-value-z&gt;
'')</code>
===Parameters===
;''scaling-value-z'':Numerical value by which to scale the specified element in the ''z''-direction.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkID{{=}}223145 CSS Transforms Module, Level 3], Section 13.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>Transform Functions</code>
*<code>[http://go.microsoft.com/fwlink/p/?LinkId{{=}}256246 Mathematical Description of Transform Functions]</code>
*<code>Direct3D: Matrices</code>
*<code>[http://go.microsoft.com/fwlink/?LinkId{{=}}227893 Hands On: 3-D Transforms]</code>
|Topic_clusters=Transforms
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}