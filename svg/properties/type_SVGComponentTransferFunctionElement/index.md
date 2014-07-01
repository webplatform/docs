{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Unreviewed MSDN import
|Checked_Out=No
|High-level issues=Needs Flags, Stub
}}
{{Standardization_Status|}}
{{API_Name}}
{{Topics|SVG}}
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

 identity '''{{!}}''' table '''{{!}}''' discrete '''{{!}}''' linear '''{{!}}''' gamma

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}226062 Scalable Vector Graphics: Filter Effects], Section 15.11

}}
{{See_Also_Section
|Manual_sections=

===Related pages (MSDN)===

*[[svg/objects/SVGComponentTransferFunctionElement|'''SVGComponentTransferFunctionElement''']]
*[[svg/elements/feFuncR|'''SVGFEFuncRElement''']]
*[[svg/elements/feFuncGelement|'''SVGFEFuncGElement''']]
*[[svg/elements/feFuncB|'''SVGFEFuncBElement''']]
*[[svg/elements/feFuncA|'''SVGFEFuncAElement''']]
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}
[[Category:SVG]]