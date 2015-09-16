---
title: orderX
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/properties/orderX

---
## Notes

### Remarks

For JavaScript, the **orderX** property indicates the number of columns in the [**kernelMatrix**](/svg/properties/kernelMatrix). For HTML, the **order** attribute is used to set both *orderX* and *orderY*, as described next.

Indicates the number of cells in each dimension for [**kernelMatrix**](/svg/properties/kernelMatrix). The values provided must be integers greater than zero. The first number, *orderX*, indicates the number of columns in the matrix. The second number, *orderY*, indicates the number of rows in the matrix. If *orderY* is not provided, it defaults to *orderX*.

A typical value is **order="3"**. It is recommended that only small values (such as 3) be used; higher values may result in very high CPU overhead and usually do not produce results that justify the impact on performance.

If the **order** attribute is not specified, the effect is as if a value of 3 were specified.

### Syntax

### Standards information

-   [Scalable Vector Graphics: Filter Effects](http://go.microsoft.com/fwlink/p/?linkid=226062), Section 15.25.12

## See also

### Related pages

-   [**SVGFEConvolveMatrixElement**](/svg/elements/feConvolveMatrix)
