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

If multiple glyphs are used to render the specified character and if the glyphs each have different rotations (for example, because of text-on-a-path), the '''getRotationOfChar''' method  returns an average value (that is, the rotation angle at the midpoint along the path for all glyphs that are used to render the specified  character).

The rotation value represents the rotation that is supplemental to any rotation because of the [[svg/attributes/glyph-orientation-horizontal|'''glyphOrientationHorizontal''']] and [[svg/attributes/glyph-orientation-vertical|'''glyphOrientationVertical''']] properties.  Any glyph rotations because of these properties are not included in the returned rotation value.

If multiple consecutive characters are rendered inseparably (for example, as a single glyph or a sequence of glyphs), each of the inseparable characters returns the same rotation value.
|Import_Notes=

===Syntax===

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199818 Scalable Vector Graphics: Text], Section 10.17.1

}}
{{See_Also_Section
|Manual_sections=

===Related pages (MSDN)===

*[[svg/elements/text|'''SVGTextElement''']]
*[[svg/elements/textPositioning|'''SVGTextPositioningElement''']]
*[[svg/elements/tspan|'''SVGTSpanElement''']]
*[[svg/elements/textPath|'''SVGTextPathElement''']]
*[[svg/elements/etextContent|'''SVGTextContentElement''']]
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}

[[Category:SVG]]