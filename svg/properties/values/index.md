{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Examples_Section
|Not_required=No
|Examples=}}
{{Notes_Section
|Notes=
===Remarks===
The contents of <code>values</code> depends on the value of attribute [[svg/properties/type (SVGFEColorMatrixElement)|'''type''']], as indicated in the following:
For <code>type{{=}}"matrix"</code>, <code>values</code> is a list of 20 matrix values (a00 a01 a02 a03 a04 a10 a11 ... a34), separated by whitespace and/or a comma. For example, the identity matrix could be expressed as:
For <code>type{{=}}"saturate"</code>, <code>values</code> is a single real number value (0 to 1). A saturate operation is equivalent to the following matrix operation:
For <code>type{{=}}"hueRotate"</code>, <code>values</code> is a single real number value (degrees). A hueRotate operation is equivalent to the following matrix operation:
where the terms a00, a01, ..., a22 are calculated as follows:
Thus, the upper-left term of the hue matrix turns out to be:
For <code>type{{=}}"luminanceToAlpha"</code>, <code>values</code> is not applicable. A luminanceToAlpha operation is equivalent to the following matrix operation:
If the <code>values</code> attribute is not specified, then the default behavior depends on the value of attribute [[svg/properties/type (SVGFEColorMatrixElement)|'''type''']]. If <code>type{{=}}"matrix"</code>, then this attribute defaults to the identity matrix. If <code>type{{=}}"saturate"</code>, then this attribute defaults to the value 1, which results in the identity matrix. If <code>type{{=}}"hueRotate"</code>, then this attribute defaults to the value 0, which results in the identity matrix.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}226062 Scalable Vector Graphics: Filter Effects], Section 15.25.4


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[svg/elements/feColorMix|SVGFEColorMatrixElement]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}