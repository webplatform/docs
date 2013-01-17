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

Identifies input for the given filter primitive. The value can be either one of six keywords (see above) or can be a string which matches a previous '''result''' attribute value within the same [[svg/elements/filter|'''filter''']] element. If no value is provided and this is the first filter primitive, then this filter primitive will use '''SourceGraphic''' as its input. If no value is provided and this is a subsequent filter primitive, then this filter primitive will use the result from the previous filter primitive as its input.

If the value for '''result''' appears multiple times within a given [[svg/elements/filter|'''filter''']] element, then a reference to that result will use the closest preceding filter primitive with the given value for attribute '''result'''. Forward references to results are an error.
|Import_Notes=

===Syntax===

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}226062 Scalable Vector Graphics: Filter Effects], Section 15.7.2

}}
{{See_Also_Section
|Manual_sections=

===Related pages (MSDN)===

*[[svg/elements/feBlend|'''SVGFEBlendElement''']]
*[[svg/elements/feColorMatrix|'''SVGFEColorMatrixElement''']]
*[[svg/elements/feComponentTransfer|'''SVGFEComponentTransferElement''']]
*[[svg/elements/feComposite|'''SVGFECompositeElement''']]
*[[svg/elements/feConvolveMatrix|'''SVGFEConvolveMatrixElement''']]
*[[svg/elements/feDiffuseLighting|'''SVGFEDiffuseLightingElement''']]
*[[svg/elements/feDisplacementMap|'''SVGFEDisplacementMapElement''']]
*[[svg/elements/feGaussianBlur|'''SVGFEGaussianBlurElement''']]
*[[svg/elements/feMergeNode|'''SVGFEMergeNodeElement''']]
*[[svg/elements/feMorphology|'''SVGFEMorphologyElement''']]
*[[svg/elements/feOffset|'''SVGFEOffsetElement''']]
*[[svg/elements/feSpecularLighting|'''SVGFESpecularLightingElement''']]
*[[svg/elements/feTile|'''SVGFETileElement''']]
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}
[[Category:SVG]]