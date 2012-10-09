{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Notes_Section
|Notes=
===Remarks===
Identifies input for the given filter primitive. The value can be either one of six keywords (see above) or can be a string which matches a previous <code>result</code> attribute value within the same [[svg/elements/filter|'''filter''']] element. If no value is provided and this is the first filter primitive, then this filter primitive will use <code>SourceGraphic</code> as its input. If no value is provided and this is a subsequent filter primitive, then this filter primitive will use the result from the previous filter primitive as its input.
If the value for <code>result</code> appears multiple times within a given [[svg/elements/filter|'''filter''']] element, then a reference to that result will use the closest preceding filter primitive with the given value for attribute <code>result</code>. Forward references to results are an error.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}226062 Scalable Vector Graphics: Filter Effects], Section 15.7.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[svg/elements/feBlend|SVGFEBlendElement]]</code>
*<code>[[svg/elements/feColorMatrix|SVGFEColorMatrixElement]]</code>
*<code>[[svg/elements/feComponentTransfer|SVGFEComponentTransferElement]]</code>
*<code>[[svg/elements/feComposite|SVGFECompositeElement]]</code>
*<code>[[svg/elements/feConvolveMatrix|SVGFEConvolveMatrixElement]]</code>
*<code>[[svg/elements/feDiffuseLighting|SVGFEDiffuseLightingElement]]</code>
*<code>[[svg/elements/feDisplacementMap|SVGFEDisplacementMapElement]]</code>
*<code>[[svg/elements/feGaussianBlur|SVGFEGaussianBlurElement]]</code>
*<code>[[svg/elements/feMergeNode|SVGFEMergeNodeElement]]</code>
*<code>[[svg/elements/feMorphology|SVGFEMorphologyElement]]</code>
*<code>[[svg/elements/feOffset|SVGFEOffsetElement]]</code>
*<code>[[svg/elements/feSpecularLighting|SVGFESpecularLightingElement]]</code>
*<code>[[svg/elements/feTile|SVGFETileElement]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}
[[Category:SVG]]