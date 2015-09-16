---
title: result
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/properties/result

---
## Notes

### Remarks

If supplied, the output of the current filter primitive can be referenced by an [**in1**](/svg/properties/in1) attribute on a subsequent filter primitive within the same element. If no value is provided, the output will only be available for re-use as the implicit input into the next filter primitive if that filter primitive provides no value for its **in1** attribute.

If an output reference occurs in several filter primitives in the same filter, only the closest filter primitive will be used. Note that this is not an XML ID. The scope of this value is local to the filter.

### Syntax

## See also

### Related pages

-   [**SVGFETileElement**](/svg/elements/feTile)
-   [**SVGFEBlendElement**](/svg/elements/feBlend)
-   [**SVGFEMorphologyElement**](/svg/elements/feMorphology)
-   [**SVGFETurbulenceElement**](/svg/elements/feTurbulence)
-   [**SVGFEColorMatrixElement**](/svg/elements/feColorMatrix)
-   [**SVGFECompositeElement**](/svg/elements/feComposite)
-   [**SVGFEDiffuseLightingElement**](/svg/elements/feDiffuseLighting)
-   [**SVGFEComponentTransferElement**](/svg/elements/feComponentTransfer)
-   [**SVGFEFloodElement**](/svg/elements/feFlood)
-   [**SVGFEMergeElement**](/svg/elements/feMerge)
-   [**SVGFESpecularLightingElement**](/svg/elements/feSpecularLighting)
-   [**SVGFEConvolveMatrixElement**](/svg/elements/feConvolveMatrix)
-   [**SVGFEImageElement**](/svg/elements/feImage)
-   [**SVGFEGaussianBlurElement**](/svg/elements/feGaussianBlur)
-   [**SVGFEDisplacementMapElement**](/svg/elements/feDisplacementMap)
-   [**SVGFEOffsetElement**](/svg/elements/feOffset)
