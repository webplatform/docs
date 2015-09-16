---
title: 'values'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'No editing form'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/properties/values

---
**Needs Examples**: This section should include examples.

## Notes

### Remarks

The contents of **values** depends on the value of attribute [**type**](/svg/properties/type_(SVGFEColorMatrixElement)), as indicated in the following:

For **type="matrix"**, **values** is a list of 20 matrix values (a00 a01 a02 a03 a04 a10 a11 ... a34), separated by whitespace and/or a comma. For example, the identity matrix could be expressed as:

For **type="saturate"**, **values** is a single real number value (0 to 1). A saturate operation is equivalent to the following matrix operation: For **type="hueRotate"**, **values** is a single real number value (degrees). A hueRotate operation is equivalent to the following matrix operation: where the terms a00, a01, ..., a22 are calculated as follows: Thus, the upper-left term of the hue matrix turns out to be: For **type="luminanceToAlpha"**, **values** is not applicable. A luminanceToAlpha operation is equivalent to the following matrix operation:

If the **values** attribute is not specified, then the default behavior depends on the value of attribute [**type**](/svg/properties/type_(SVGFEColorMatrixElement)). If **type="matrix"**, then this attribute defaults to the identity matrix. If **type="saturate"**, then this attribute defaults to the value 1, which results in the identity matrix. If **type="hueRotate"**, then this attribute defaults to the value 0, which results in the identity matrix.

### Syntax

### Standards information

-   [Scalable Vector Graphics: Filter Effects](http://go.microsoft.com/fwlink/p/?linkid=226062), Section 15.25.4

## See also

### Related pages

-   [**SVGFEColorMatrixElement**](/svg/elements/feColorMatrix)
