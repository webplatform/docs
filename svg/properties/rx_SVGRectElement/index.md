{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Notes_Section
|Notes=
===Remarks===
If you  properly specify a  value  for  the '''rx'''  property but not for the  [[svg/properties/ry (SVGRectElement)|'''ry''']]  property,  the [[svg/elements/rect|'''rect''']] element is rendered with the effective value of '''ry'''   equal to '''rx'''. If  you  properly specify a  value  for '''ry''' but not for '''rx''',  the '''rect''' element is rendered with the effective value of '''rx'''  equal to '''ry'''.
If you do not property specify '''rx''' or [[svg/properties/ry (SVGRectElement)|'''ry''']] ,  the [[svg/elements/rect|'''rect''']] element is rendered  without  rounding, resulting in square corners.
If '''rx''' is greater than half of the width of the rectangle,  the [[svg/elements/rect|'''rect''']] element is rendered with the effective value for '''rx''' as half of the width of the rectangle. If [[svg/properties/ry (SVGRectElement)|'''ry''']] is greater than half of the height of the rectangle,  the '''rect''' element is rendered with the effective value for '''ry''' as half of the height of the rectangle.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204737 Scalable Vector Graphics: Basic Shapes], Section 9.8.1


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[svg/elements/rect|SVGRectElement]]</code>
*<code>[[svg/elements/ellipse|ellipse]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}
[[Category:SVG]]