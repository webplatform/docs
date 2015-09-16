---
title: posBottom
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs spec reference, standardization status'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/cssom/properties
    href: /css/cssom/properties
summary: 'Reflects the value of the Cascading Style Sheets (CSS) bottom attribute for positioned items.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: css/cssom/properties/posBottom

---
## Summary

Reflects the value of the Cascading Style Sheets (CSS) bottom attribute for positioned items.

Property of [css/cssom/properties](/css/cssom/properties)[css/cssom/properties](/css/cssom/properties)

## Syntax

``` js
var result = element.posBottom;
element.posBottom = value;
```

## Examples

This example uses the **posBottom** property to set a positioned **div** to the bottom of the client area.

``` js
oDiv.style.posBottom = 0;
```

## Notes

### Remarks

This property reflects the value of the Cascading Style Sheets (CSS) [**bottom**](/css/properties/bottom) attribute for positioned items. This property always returns zero for nonpositioned items because "bottom" has meaning only when the object is positioned. If the **bottom** attribute is not set, the **posBottom** property returns zero. Setting this property changes the value of the bottom position but leaves the CSS Values and Units Reference designator for the property unchanged. Unlike the [**bottom**](/css/properties/bottom) property, the **posBottom** property value is a floating-point number, not a string. For more information about how to access the dimension and location of elements on the page through the Dynamic HTML (DHTML) Document Object Model (DOM), see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.

## See also

### Related pages (MSDN)

-   `runtimeStyle`
-   `style`
-   `pixelBottom`
