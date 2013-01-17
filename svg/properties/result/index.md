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

If supplied, the output of the current  filter primitive can be referenced by an [[svg/properties/in1|'''in1''']] attribute on a subsequent filter primitive within the same element. If no value is provided, the output will only be available for re-use as the implicit input into the next filter primitive if that filter primitive provides no value for its '''in1''' attribute.

If an output reference occurs in several filter primitives in the same filter, only the closest filter primitive will be used.
Note that this is not an XML ID. The scope of this value is local to the filter.
|Import_Notes=

===Syntax===

}}
{{See_Also_Section
|Manual_sections=

===Related pages (MSDN)===

*[[svg/elements/feTile|'''SVGFETileElement''']]
*[[svg/elements/feBlend|'''SVGFEBlendElement''']]
*[[svg/elements/feMorphology|'''SVGFEMorphologyElement''']]
*[[svg/elements/feTurbulence|'''SVGFETurbulenceElement''']]
*[[svg/elements/feColorMatrix|'''SVGFEColorMatrixElement''']]
*[[svg/elements/feComposite|'''SVGFECompositeElement''']]
*[[svg/elements/feDiffuseLighting|'''SVGFEDiffuseLightingElement''']]
*[[svg/elements/feComponentTransfer|'''SVGFEComponentTransferElement''']]
*[[svg/elements/feFlood|'''SVGFEFloodElement''']]
*[[svg/elements/feMerge|'''SVGFEMergeElement''']]
*[[svg/elements/feSpecularLighting|'''SVGFESpecularLightingElement''']]
*[[svg/elements/feConvolveMatrix|'''SVGFEConvolveMatrixElement''']]
*[[svg/elements/feImage|'''SVGFEImageElement''']]
*[[svg/elements/feGaussianBlur|'''SVGFEGaussianBlurElement''']]
*[[svg/elements/feDisplacementMap|'''SVGFEDisplacementMapElement''']]
*[[svg/elements/feOffset|'''SVGFEOffsetElement''']]
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}
[[Category:SVG]]