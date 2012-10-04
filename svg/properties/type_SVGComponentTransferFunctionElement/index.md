{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Notes_Section
|Notes=
===Remarks===
For a type of '''table''' and a value C &lt; 1, find k such that:
k/''n'' &lt;{{=}} C &lt; (k+1)/''n''
The result C' is given by:
C' {{=}} v<sub>k</sub> + (C - k/''n'')*''n'' * (v<sub>k+1</sub> - v<sub>k</sub>)
If C {{=}} 1 then:
C' {{=}} v''<sub>n</sub>''
For a type of '''discrete''' and a value C &lt; 1 find k such that:
k/''n'' &lt;{{=}} C &lt; (k+1)/''n''
The result C' is given by:
C' {{=}} v<sub>k</sub>
If C {{=}} 1 then:
C' {{=}} v<sub>n-1</sub>
|Import_Notes=
===Syntax===
===String format===
<code>identity '''{{!}}''' table '''{{!}}''' discrete '''{{!}}''' linear '''{{!}}''' gamma</code>

===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}226062 Scalable Vector Graphics: Filter Effects], Section 15.11


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[svg/objects/SVGComponentTransferFunctionElement|SVGComponentTransferFunctionElement]]</code>
*<code>[[svg/elements/feFuncR|SVGFEFuncRElement]]</code>
*<code>[[svg/elements/feFuncGelement|SVGFEFuncGElement]]</code>
*<code>[[svg/elements/feFuncB|SVGFEFuncBElement]]</code>
*<code>[[svg/elements/feFuncA|SVGFEFuncAElement]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}