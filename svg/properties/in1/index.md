---
title: in1
tags:
  - SVG
readiness: 'Not Ready'
standardization_status: Unknown
notes:
  - 'Unreviewed MSDN import'
uri: svg/properties/in1

---
# in1

## Notes

### Remarks

Identifies input for the given filter primitive. The value can be either one of six keywords (see above) or can be a string which matches a previous **result** attribute value within the same [**filter**](/svg/elements/filter) element. If no value is provided and this is the first filter primitive, then this filter primitive will use **SourceGraphic** as its input. If no value is provided and this is a subsequent filter primitive, then this filter primitive will use the result from the previous filter primitive as its input.

If the value for **result** appears multiple times within a given [**filter**](/svg/elements/filter) element, then a reference to that result will use the closest preceding filter primitive with the given value for attribute **result**. Forward references to results are an error.

### Syntax

### Standards information

-   [Scalable Vector Graphics: Filter Effects](http://go.microsoft.com/fwlink/p/?linkid=226062), Section 15.7.2

## See also

### Related pages (MSDN)

-   [**SVGFEBlendElement**](/svg/elements/feBlend)
-   [**SVGFEColorMatrixElement**](/svg/elements/feColorMatrix)
-   [**SVGFEComponentTransferElement**](/svg/elements/feComponentTransfer)
-   [**SVGFECompositeElement**](/svg/elements/feComposite)
-   [**SVGFEConvolveMatrixElement**](/svg/elements/feConvolveMatrix)
-   [**SVGFEDiffuseLightingElement**](/svg/elements/feDiffuseLighting)
-   [**SVGFEDisplacementMapElement**](/svg/elements/feDisplacementMap)
-   [**SVGFEGaussianBlurElement**](/svg/elements/feGaussianBlur)
-   [**SVGFEMergeNodeElement**](/svg/elements/feMergeNode)
-   [**SVGFEMorphologyElement**](/svg/elements/feMorphology)
-   [**SVGFEOffsetElement**](/svg/elements/feOffset)
-   [**SVGFESpecularLightingElement**](/svg/elements/feSpecularLighting)
-   [**SVGFETileElement**](/svg/elements/feTile)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

