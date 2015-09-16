---
title: type (SVGComponentTransferFunctionElement)
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: 'svg/properties/type (SVGComponentTransferFunctionElement)'

---
## Notes

### Remarks

For a type of **table** and a value C \< 1, find k such that: k/*n* \<= C \< (k+1)/*n* The result C' is given by: C' = v<sub>k</sub> + (C - k/*n*)\**n* \* (v<sub>k+1</sub> - v<sub>k</sub>) If C = 1 then: C' = v*<sub>n</sub>* For a type of **discrete** and a value C \< 1 find k such that: k/*n* \<= C \< (k+1)/*n* The result C' is given by: C' = v<sub>k</sub> If C = 1 then: C' = v<sub>n-1</sub>

### Syntax

### String format

    identity | table | discrete | linear | gamma

### Standards information

-   [Scalable Vector Graphics: Filter Effects](http://go.microsoft.com/fwlink/p/?linkid=226062), Section 15.11

## See also

### Related pages

-   [**SVGComponentTransferFunctionElement**](/svg/objects/SVGComponentTransferFunctionElement)
-   [**SVGFEFuncRElement**](/svg/elements/feFuncR)
-   [**SVGFEFuncGElement**](/svg/elements/feFuncGelement)
-   [**SVGFEFuncBElement**](/svg/elements/feFuncB)
-   [**SVGFEFuncAElement**](/svg/elements/feFuncA)
