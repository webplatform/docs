---
title: posLeft
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
notes:
  - 'Needs spec reference, standardization status'
summary: 'Reflects the value of the Cascading Style Sheets (CSS) left attribute for positioned items.'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/pixelWidth.htm'
uri: css/cssom/properties/posLeft

---
# posLeft

## Summary

Reflects the value of the Cascading Style Sheets (CSS) left attribute for positioned items.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[css/cssom/properties](/css/cssom/properties)</span></span>

## Syntax

``` {.js}
var result = element.posLeft;
element.posLeft = value;
```

## Examples

This example uses the **posLeft** property to move the first **img** object left by 10 units.

``` {.js}
<SCRIPT LANGUAGE="JScript">
document.all.tags("IMG").item(0).style.posLeft -= 10;
</SCRIPT>
```

This example uses a timer to change the value of the **posLeft** in increments of 10.

``` {.js}
<SCRIPT LANGUAGE="JScript">
function moveThis()
{
:
    if (sphere.style.posLeft<900) {
        sphere.style.posTop += 2;
        sphere.style.posLeft += 2;
        window.setTimeout("moveThis();", 1);
        }
}
:
</SCRIPT>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/pixelWidth.htm)

## Notes

### Remarks

This property reflects the value of the Cascading Style Sheets (CSS) [**left**](/css/properties/left) attribute for positioned items. This property always returns zero for nonpositioned items because "left" has meaning only when the object is positioned. If the **left** attribute is not set, the **posLeft** property returns zero. Use the [**offsetLeft**](/dom/HTMLElement/offsetLeft) property to calculate actual positions within the document area. Setting this property changes the value of the left position but leaves the units designator for the property unchanged. Unlike the [**left**](/css/properties/left) property, the **posLeft** property value is a floating-point number, not a string.

## See also

### Related pages (MSDN)

-   `runtimeStyle`
-   `style`
-   `pixelLeft`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

