{{Page Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
|State=Not Ready
|Editorial notes=No editing form
}}
{{Standardization_Status|}}
{{API_Name}}
{{Topics|SVG}}
{{Notes_Section
|Notes=

===Remarks===

The '''createSVGTransformFromMatrix''' method creates an [[svg/objects/SVGTransform|'''SVGTransform''']] object, of transform type SVG_TRANSFORM_MATRIX, whose values are given by the ''matrix'' parameter. The values from the ''matrix'' parameter   are copied;  the ''matrix'' parameter is not adopted as  the [[svg/properties/matrix|'''matrix''']] property.

The [[svg/objects/SVGTransform|'''SVGTransform''']] object corresponds to a single '''matrix()''' component within an element's '''transform''' attribute specification.

'''Note:'''  For   [[svg/elements/svg|'''SVGSVGElement''']]  elements, the [[svg/objects/SVGTransform|'''SVGTransform''']] object is created outside of any document trees.
|Import_Notes=

===Syntax===

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204735 Scalable Vector Graphics: Coordinate Systems, Transformations and Units], Section 7.14.5

}}
{{See_Also_Section
|Manual_sections=

===Related pages (MSDN)===

*[[svg/elements/svg|'''SVGSVGElement''']]
*[[svg/objects/SVGTransformList|'''SVGTransformList''']]
*[[svg/objects/SVGMatrix|'''SVGMatrix''']]
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}

[[Category:SVG]]