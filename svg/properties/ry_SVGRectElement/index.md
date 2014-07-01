{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Unreviewed MSDN import
|Checked_Out=No
|High-level issues=Needs Flags, Stub
}}
{{Standardization_Status|}}
{{API_Name}}
{{Topics|SVG}}
{{Notes_Section
|Notes=

===Remarks===

If  you properly specify a  value  for  the [[svg/properties/rx (SVGRectElement)|'''rx''']]  property but not for the  '''ry''' property,  the [[svg/elements/rect|'''rect''']] element is rendered with the effective value of '''ry'''  equal to '''rx'''. If  you  properly specify a  value  for '''ry''' but not for '''rx''',  the '''rect''' element is rendered with the effective value of '''rx'''  equal to '''ry'''.

If  you do not properly specify [[svg/properties/rx (SVGRectElement)|'''rx''']] or '''ry''' ,  the [[svg/elements/rect|'''rect''']] element is rendered  without  rounding, resulting in square corners.

If [[svg/properties/rx (SVGRectElement)|'''rx''']] is greater than half of the width of the rectangle,  the [[svg/elements/rect|'''rect''']] element is rendered with the effective value for '''rx''' as half of the width of the rectangle. If '''ry''' is greater than half of the height of the rectangle,  the '''rect''' element is rendered with the effective value for '''ry''' as half of the height of the rectangle.
|Import_Notes=

===Syntax===

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204737 Scalable Vector Graphics: Basic Shapes], Section 9.8.1

}}
{{See_Also_Section
|Manual_sections=

===Related pages (MSDN)===

*[[svg/elements/rect|'''SVGRectElement''']]
*[[svg/elements/ellipse|'''ellipse''']]
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}
[[Category:SVG]]