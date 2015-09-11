---
title: setStdDeviation
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'No editing form'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/methods/setStdDeviation

---
## <span>Notes</span>

### <span>Remarks</span>

If two values are provided, the first value represents a standard deviation value along the x-axis of the coordinate system established by the [**primitiveUnits**](/svg/properties/primitiveUnits) attribute on the [**filter**](/svg/elements/filter) element. The second value represents a standard deviation along the y-axis.

If one number is provided, then that value is used for both *stdDeviationX* and *stdDeviationY*. Negative values are not allowed.

A value of zero disables the effect of the given filter primitive (that is, the result is the filter input image). If the **stdDeviation** method is zero in only one of *stdDeviationX* or *stdDeviationY*, then the effect is that the blur is applied only in the direction that has a non-zero value.

If the **stdDeviation** method is not specified, then the effect is as if a value of zero were specified.

### <span>Syntax</span>

### <span>Standards information</span>

-   [Scalable Vector Graphics: Filter Effects](http://go.microsoft.com/fwlink/p/?linkid=226062), Section 15.25.19

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   [**SVGFEGaussianBlurElement**](/svg/elements/feGaussianBlur)
