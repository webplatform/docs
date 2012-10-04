{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Notes_Section
|Notes=
===Remarks===
For JavaScript, the <code>orderX</code> property indicates the number of columns in the [[svg/properties/kernelMatrix|'''kernelMatrix''']]. For HTML, the <code>order</code> attribute is used to set both ''orderX'' and ''orderY'', as described next.
Indicates the number of cells in each dimension for [[svg/properties/kernelMatrix|'''kernelMatrix''']]. The values provided must be integers greater than zero. The first number, ''orderX'', indicates the number of columns in the matrix. The second number, ''orderY'', indicates the number of rows in the matrix. If ''orderY'' is not provided, it defaults to ''orderX''.
A typical value is <code>order{{=}}"3"</code>. It is recommended that only small values (such as 3) be used; higher values may result in very high CPU overhead and usually do not produce results that justify the impact on performance.
If the <code>order</code> attribute is not specified, the effect is as if a value of 3 were specified.
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