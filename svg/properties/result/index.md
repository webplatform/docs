{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
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
*<code>[[svg/elements/feTile|SVGFETileElement]]</code>
*<code>[[svg/elements/feBlend|SVGFEBlendElement]]</code>
*<code>[[svg/elements/feMorphology|SVGFEMorphologyElement]]</code>
*<code>[[svg/elements/feTurbulence|SVGFETurbulenceElement]]</code>
*<code>[[svg/elements/feColorMix|SVGFEColorMatrixElement]]</code>
*<code>[[svg/elements/feComposite|SVGFECompositeElement]]</code>
*<code>[[svg/elements/feDiffuseLighting|SVGFEDiffuseLightingElement]]</code>
*<code>[[svg/elements/feComponentTransfer|SVGFEComponentTransferElement]]</code>
*<code>[[svg/elements/feFlood|SVGFEFloodElement]]</code>
*<code>[[svg/elements/feMerge|SVGFEMergeElement]]</code>
*<code>[[svg/elements/feSpecularLighting|SVGFESpecularLightingElement]]</code>
*<code>[[svg/elements/feConvolveMatrix|SVGFEConvolveMatrixElement]]</code>
*<code>[[svg/elements/feImage|SVGFEImageElement]]</code>
*<code>[[svg/elements/feGaussianBlur|SVGFEGaussianBlurElement]]</code>
*<code>[[svg/elements/feDisplacementMap|SVGFEDisplacementMapElement]]</code>
*<code>[[svg/elements/feOffset|SVGFEOffsetElement]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}
[[Category:SVG]]