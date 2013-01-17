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

For JavaScript, the '''orderX''' property indicates the number of columns in the [[svg/properties/kernelMatrix|'''kernelMatrix''']]. For HTML, the '''order''' attribute is used to set both ''orderX'' and ''orderY'', as described next.

Indicates the number of cells in each dimension for [[svg/properties/kernelMatrix|'''kernelMatrix''']]. The values provided must be integers greater than zero. The first number, ''orderX'', indicates the number of columns in the matrix. The second number, ''orderY'', indicates the number of rows in the matrix. If ''orderY'' is not provided, it defaults to ''orderX''.

A typical value is '''order{{=}}"3"'''. It is recommended that only small values (such as 3) be used; higher values may result in very high CPU overhead and usually do not produce results that justify the impact on performance.

If the '''order''' attribute is not specified, the effect is as if a value of 3 were specified.
|Import_Notes=

===Syntax===

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}226062 Scalable Vector Graphics: Filter Effects], Section 15.25.12

}}
{{See_Also_Section
|Manual_sections=

===Related pages (MSDN)===

*[[svg/elements/feConvolveMatrix|'''SVGFEConvolveMatrixElement''']]
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}
[[Category:SVG]]