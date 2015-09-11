---
title: kernelUnitLengthX
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/properties/kernelUnitLengthX

---
## <span>Notes</span>

### <span>Remarks</span>

For JavaScript, the **kernelUnitLengthX** property represents *dx*. For HTML, the **kernelUnitLength** attribute is used to set both *dx* and *dy*, as described next.

For the attribute **kernelUnitLength = "\<** *number optional-number* **\>"**, the first number is the *dx* value. The second number is the *dy* value. If the *dy* value is not specified, it defaults to the same value as *dx*.

**kernelUnitLength** indicates the intended distance in current filter units (as determined by the value of the [**primitiveUnits**](/svg/properties/primitiveUnits) attribute) for *dx* and *dy*, respectively, in the surface normal calculation formulas. By specifying value(s) for **kernelUnitLength**, the kernel becomes defined in a scalable, abstract coordinate system. If **kernelUnitLength** is not specified, the *dx* and *dy* values should represent very small deltas relative to a given (*x*, *y*) position.

For some level of consistency across display media and browsers, it is necessary that a value be provided for at least one of [**filterRes**](/svg/methods/setFilterRes) and **kernelUnitLength**.

### <span>Syntax</span>

### <span>Standards information</span>

-   [Scalable Vector Graphics: Filter Effects](http://go.microsoft.com/fwlink/p/?linkid=226062), Section 15.25.12

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   [**SVGFEConvolveMatrixElement**](/svg/elements/feConvolveMatrix)
-   [**SVGFEDiffuseLightingElement**](/svg/elements/feDiffuseLighting)
-   [**SVGFESpecularLightingElement**](/svg/elements/feSpecularLighting)
