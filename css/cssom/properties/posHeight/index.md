---
title: posHeight
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
notes:
  - 'Needs spec reference, standardization status'
summary: 'Reflects the value of the Cascading Style Sheets (CSS) height attribute for positioned items.'
uri: css/cssom/properties/posHeight

---
# posHeight

## Summary

Reflects the value of the Cascading Style Sheets (CSS) height attribute for positioned items.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[css/cssom/properties](/css/cssom/properties)</span></span>

## Syntax

``` {.js}
var result = element.posHeight;
element.posHeight = value;
```

## Examples

This example uses the **posHeight** property to increase the height of the first **img** element by 10 units.

``` {.js}
<SCRIPT LANGUAGE="JScript">
document.all.tags("IMG").item(0).style.posHeight += 10;
</SCRIPT>
```

## Notes

### Remarks

This property reflects the value of the Cascading Style Sheets (CSS) [**height**](/css/properties/height) attribute for positioned items. This property always returns zero for nonpositioned items because "height" has meaning only when the object is positioned. If the **height** attribute is not set, the **posHeight** property returns zero. Unlike the [**height**](/css/properties/height) property, the **posHeight** property value is a floating-point number, not a string. Setting the **posHeight** property changes the value of the height but leaves the units designator for the property unchanged. For more information about how to access the dimension and location of objects on the page through the Dynamic HTML (DHTML) Document Object Model (DOM), see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.

## See also

### Related pages (MSDN)

-   `runtimeStyle`
-   `style`
-   `pixelHeight`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

