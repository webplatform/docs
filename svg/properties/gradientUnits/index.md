{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Notes_Section
|Notes=
===Remarks===
When ''p'' is '''objectBoundingBox'''  and the [[svg/properties/gradientTransform|'''gradientTransform''']] property is the identity matrix, the normal of the linear gradient is perpendicular to the gradient vector in object bounding box space. When the object's bounding box is not square, the gradient normal (which is initially perpendicular to the gradient vector within object bounding box space) might render non-perpendicular relative to the gradient vector in user space. If the gradient vector is parallel to one of the axes of the bounding box, the gradient normal remains perpendicular. This transformation occurs because of the non-uniform scaling transformation from bounding box space to user space.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199811 Scalable Vector Graphics: Gradients and Patterns], Section 13.4.1


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[svg/elements/gradient|SVGGradientElement]]</code>
*<code>[[svg/elements/linearGradient|SVGLinearGradientElement]]</code>
*<code>[[svg/elements/radialGradient|SVGRadialGradientElement]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}