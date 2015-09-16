---
title: bias
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/properties/bias

---
## Notes

### Remarks

After applying the [**kernelMatrix**](/svg/properties/kernelMatrix) to the input image to yield a number and applying the [**divisor**](/svg/properties/divisor), the **bias** attribute is added to each component. One application of **bias** is when it is desirable to have 0.5 gray value be the zero response of the filter. The **bias** property shifts the range of the filter. This allows representation of values that would otherwise be clamped to 0 or 1. If **bias** is not specified, then the effect is as if a value of 0 were specified.

### Syntax

### Standards information

-   [Scalable Vector Graphics: Filter Effects](http://go.microsoft.com/fwlink/p/?linkid=226062), Section 15.25.12

## See also

### Related pages

-   [**SVGFEConvolveMatrixElement**](/svg/elements/feConvolveMatrix)
