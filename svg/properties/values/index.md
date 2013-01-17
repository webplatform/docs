{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Examples_Section
|Not_required=No
|Examples=}}
{{Topics|SVG}}
{{Notes_Section
|Notes=

===Remarks===

The contents of '''values''' depends on the value of attribute [[svg/properties/type (SVGFEColorMatrixElement)|'''type''']], as indicated in the following:

For '''type{{=}}"matrix"''', '''values''' is a list of 20 matrix values (a00 a01 a02 a03 a04 a10 a11 ... a34), separated by whitespace and/or a comma. For example, the identity matrix could be expressed as:

For '''type{{=}}"saturate"''', '''values''' is a single real number value (0 to 1). A saturate operation is equivalent to the following matrix operation:
For '''type{{=}}"hueRotate"''', '''values''' is a single real number value (degrees). A hueRotate operation is equivalent to the following matrix operation:
where the terms a00, a01, ..., a22 are calculated as follows:
Thus, the upper-left term of the hue matrix turns out to be:
For '''type{{=}}"luminanceToAlpha"''', '''values''' is not applicable. A luminanceToAlpha operation is equivalent to the following matrix operation:

If the '''values''' attribute is not specified, then the default behavior depends on the value of attribute [[svg/properties/type (SVGFEColorMatrixElement)|'''type''']]. If '''type{{=}}"matrix"''', then this attribute defaults to the identity matrix. If '''type{{=}}"saturate"''', then this attribute defaults to the value 1, which results in the identity matrix. If '''type{{=}}"hueRotate"''', then this attribute defaults to the value 0, which results in the identity matrix.
|Import_Notes=

===Syntax===

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}226062 Scalable Vector Graphics: Filter Effects], Section 15.25.4

}}
{{See_Also_Section
|Manual_sections=

===Related pages (MSDN)===

*[[svg/elements/feColorMatrix|'''SVGFEColorMatrixElement''']]
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}
[[Category:SVG]]