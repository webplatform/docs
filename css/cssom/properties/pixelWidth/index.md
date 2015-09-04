---
title: pixelWidth
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
notes:
  - 'Needs spec reference, standardization status'
summary: 'Changes the value of the width without changing the units designator.'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/pixelWidth.htm'
uri: css/cssom/properties/pixelWidth

---
# pixelWidth

## Summary

Changes the value of the width without changing the units designator.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[css/cssom/properties](/css/cssom/properties)</span></span>

## Syntax

``` {.js}
var result = element.pixelWidth;
element.pixelWidth = value;
```

## Examples

This example uses a timer to increment the **pixelWidth** property.

``` {.js}
<SCRIPT>
function scaleThis()
{
    if (sphere.style.pixelWidth <900) {
        sphere.style.pixelWidth += 4;
        sphere.style.pixelHeight +=4;
        window.setTimeout("scaleThis();", 1);
    }
}
:
</SCRIPT>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/pixelWidth.htm)

## Notes

### Remarks

Setting this property changes the value of the width without changing the units designator. Unlike the [**width**](/css/properties/width) property, the **pixelWidth** value is an integer, not a string, and is always interpreted in pixels.

## See also

### Related pages (MSDN)

-   `runtimeStyle`
-   `style`
-   `posWidth`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

