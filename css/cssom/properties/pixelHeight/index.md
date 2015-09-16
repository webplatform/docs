---
title: 'pixelHeight'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/pixelWidth.htm'
notes:
  - 'Needs spec reference, standardization status'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/cssom/properties
    href: /css/cssom/properties
summary: 'Changes the value of the height without changing the units designator.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: css/cssom/properties/pixelHeight

---
## Summary

Changes the value of the height without changing the units designator.

Property of [css/cssom/properties](/css/cssom/properties)[css/cssom/properties](/css/cssom/properties)

## Syntax

``` js
var result = element.pixelHeight;
element.pixelHeight = value;
```

## Examples

This example uses a timer to increment the **pixelHeight** property.

``` js
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

Setting this property changes the value of the height without changing the units designator. Unlike the [**height**](/css/properties/height) property, this property's value is an integer, not a string, and is always interpreted in pixels.

## See also

### Related pages

-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
-   posHeight[posHeight](/css/cssom/properties/posHeight)
