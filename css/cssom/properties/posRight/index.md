---
title: posRight
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
summary: 'Reflects the value of the Cascading Style Sheets (CSS) right attribute for positioned items.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: css/cssom/properties/posRight

---
## <span>Summary</span>

Reflects the value of the Cascading Style Sheets (CSS) right attribute for positioned items.

Property of [css/cssom/properties](/css/cssom/properties)[css/cssom/properties](/css/cssom/properties)

## <span>Syntax</span>

``` js
var result = element.posRight;
element.posRight = value;
```

## <span>Examples</span>

This example uses the **posRight** property to set a positioned **div** 10 pixels from the right of the client area.

``` js
oDiv.style.posRight = 10;
```

## <span>Notes</span>

### <span>Remarks</span>

This property reflects the value of the Cascading Style Sheets (CSS) [**right**](/css/properties/right) attribute for positioned items. This property always returns zero for nonpositioned items because "right" has meaning only when the object is positioned. If the **right** attribute is not set, the **posRight** property returns zero. Setting this property changes the value of the right position but leaves the units designator for the property unchanged. Unlike the [**right**](/css/properties/right) property, the **posRight** property value is a floating-point number, not a string. For more information about how to access the dimension and location of elements on the page through the Dynamic HTML (DHTML) Document Object Model (DOM), see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `runtimeStyle`
-   `style`
-   `pixelRight`
