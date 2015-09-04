---
title: posRight
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
notes:
  - 'Needs spec reference, standardization status'
summary: 'Reflects the value of the Cascading Style Sheets (CSS) right attribute for positioned items.'
uri: css/cssom/properties/posRight

---
# posRight

## Summary

Reflects the value of the Cascading Style Sheets (CSS) right attribute for positioned items.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[css/cssom/properties](/css/cssom/properties)</span></span>

## Syntax

``` {.js}
var result = element.posRight;
element.posRight = value;
```

## Examples

This example uses the **posRight** property to set a positioned **div** 10 pixels from the right of the client area.

``` {.js}
oDiv.style.posRight = 10;
```

## Notes

### Remarks

This property reflects the value of the Cascading Style Sheets (CSS) [**right**](/css/properties/right) attribute for positioned items. This property always returns zero for nonpositioned items because "right" has meaning only when the object is positioned. If the **right** attribute is not set, the **posRight** property returns zero. Setting this property changes the value of the right position but leaves the units designator for the property unchanged. Unlike the [**right**](/css/properties/right) property, the **posRight** property value is a floating-point number, not a string. For more information about how to access the dimension and location of elements on the page through the Dynamic HTML (DHTML) Document Object Model (DOM), see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.

## See also

### Related pages (MSDN)

-   `runtimeStyle`
-   `style`
-   `pixelRight`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

