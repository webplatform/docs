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

For JavaScript, the '''kernelUnitLengthX''' property represents ''dx''. For HTML, the '''kernelUnitLength''' attribute is used to set both ''dx'' and ''dy'', as described next.

For the attribute '''kernelUnitLength {{=}} "&lt;''' ''number optional-number'' '''&gt;"''', the first number is the ''dx'' value. The second number is the ''dy'' value. If the ''dy'' value is not specified, it defaults to the same value as ''dx''.

'''kernelUnitLength''' indicates the intended distance in current filter units (as determined by the value of the [[svg/properties/primitiveUnits|'''primitiveUnits''']] attribute) for ''dx'' and ''dy'', respectively, in the surface normal calculation formulas. By specifying value(s) for '''kernelUnitLength''', the kernel becomes defined in a scalable, abstract coordinate system. If '''kernelUnitLength''' is not specified, the ''dx'' and ''dy'' values should represent very small deltas relative to a given (''x'', ''y'') position.

For some level of consistency across display media and browsers, it is necessary that a value be provided for at least one of [[svg/methods/setFilterRes|'''filterRes''']] and '''kernelUnitLength'''.
|Import_Notes=

===Syntax===

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}226062 Scalable Vector Graphics: Filter Effects], Section 15.25.12

}}
{{See_Also_Section
|Manual_sections=

===Related pages (MSDN)===

*[[svg/elements/feConvolveMatrix|'''SVGFEConvolveMatrixElement''']]
*[[svg/elements/feDiffuseLighting|'''SVGFEDiffuseLightingElement''']]
*[[svg/elements/feSpecularLighting|'''SVGFESpecularLightingElement''']]
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}
[[Category:SVG]]