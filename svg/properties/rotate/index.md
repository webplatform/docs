---
title: 'rotate'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/properties/rotate

---
## Examples

The following code example shows how to rotate individual characters. Because the number of rotate values is less than the number of characters in the string, all characters after the fourth character are rendered at 30°.

``` html


<?xml version="1.0" standalone="no"?>
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN"
"http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">
<svg width="100%" height="100%" version="1.1" xmlns="http://www.w3.org/2000/svg"
     xmlns:xlink="http://www.w3.org/1999/xlink">
  <text font-family="Verdana" font-size="55" fill="blue" >
    <!--  -->
    <tspan x="250" y="150" rotate="-30, -15, 0, 15, 30">
      Hello World!
    </tspan>
  </text>
</svg>
```

</pre>

## Notes

### Remarks

The **rotate** property gets or sets the supplemental rotation about the current text position that is applied to all of the glyphs that correspond to each character within this element.

If you provide a comma-separated or space-separated list of numbers, the first number represents the supplemental rotation for the glyphs that correspond to the first character within this element or any of its descendants, the second number represents the supplemental rotation for the glyphs that correspond to the second character, and so on.

If you provide more numbers than there are characters, the extra numbers are ignored.

If more characters are provided than numbers, for each of these extra characters, the rotation value that is specified by the last number is used for these remaining characters.

If you do not specify the **rotate** attribute and if an ancestor [**text**](/svg/elements/text) or [**tSpan**](/svg/elements/tspan) element specifies a supplemental rotation for a given character through a **rotate** attribute, the specified supplemental rotation is applied to the given character (the nearest ancestor has precedence). If there are more characters than numbers that are specified in the ancestor's **rotate** attribute, for each of these extra characters, the rotation value that is specified by the last number is used.

This supplemental rotation does not impact how the current text position is modified as glyphs get rendered and is supplemental to any rotation because of text on a path and to **glyph-orientation-horizontal** or **glyph-orientation-vertical**.

**Note:** If you do not specify the **rotate** attribute on an element or any of its descendants, no supplemental rotations occur.

### Syntax

### Standards information

-   [Scalable Vector Graphics (SVG) 1.1](http://go.microsoft.com/fwlink/p/?linkid=190918), Appendix M

## See also

### Related pages

-   [**SVGTextElement**](/svg/elements/text)
-   [**SVGTextPositioningElement**](/svg/elements/textPositioning)
-   [**SVGTSpanElement**](/svg/elements/tspan)
