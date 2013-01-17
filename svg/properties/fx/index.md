{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Topics|SVG}}
{{Notes_Section
|Notes=

===Remarks===

The '''fx''' and [[svg/properties/fy|'''fy''']] properties define the focal point for the radial gradient. The
gradient is drawn such that the 0% gradient stop is mapped to the point (fx, fy).
If you do not specify the '''fx'''  attribute, '''fx'''  coincides with the presentational
value of [[svg/properties/cx (SVGRadialGradientElement)|'''cx''']]  for the element, whether the value for  '''cx'''  is inherited or not. If the
element references an element that specifies a value for '''fx''', the value of  '''fx'''
is inherited from the referenced element.
You can animate the '''fx'''  property.
|Import_Notes=

===Syntax===

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199811 Scalable Vector Graphics: Gradients and Patterns], Section 13.4.3

}}
{{See_Also_Section
|Manual_sections=

===Related pages (MSDN)===

*[[svg/elements/radialGradient|'''SVGRadialGradientElement''']]

===Reference===

*[[svg/properties/fy|'''fy''']]
*[[svg/properties/r (SVGRadialGradientElement)|'''r''']]
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}
[[Category:SVG]]