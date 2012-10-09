{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Notes_Section
|Notes=
===Remarks===
After applying the [[svg/properties/kernelMatrix|'''kernelMatrix''']] to the input image to yield a number and applying the [[svg/properties/divisor|'''divisor''']], the '''bias''' attribute is added to each component. One application of '''bias''' is when it is desirable to have 0.5 gray value be the zero response of the filter. The '''bias''' property shifts the range of the filter. This allows representation of values that would otherwise be clamped to 0 or 1. If '''bias''' is not specified, then the effect is as if a value of 0 were specified.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}226062 Scalable Vector Graphics: Filter Effects], Section 15.25.12


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[svg/elements/feConvolveMatrix|SVGFEConvolveMatrixElement]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}

[[Category:SVG]]