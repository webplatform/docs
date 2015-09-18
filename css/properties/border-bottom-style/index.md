---
title: 'border-bottom-style'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://code.webplatform.org/gist/5549378'
compatibility:
  feature: border-bottom-style
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'specified value'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`borderStyleTop`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Sets the style of an element''s bottom border. To set all four borders, use the shorthand property,  border-style. Otherwise, you can set the borders individually with border-top-style, border-right-style, border-bottom-style, border-left-style.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/border-bottom-style

---
## Summary

Sets the style of an element's bottom border. To set all four borders, use the shorthand property, border-style. Otherwise, you can set the borders individually with border-top-style, border-right-style, border-bottom-style, border-left-style.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `none`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   specified value

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `borderStyleTop`

Percentages
:   N/A

## Syntax

-   `border-bottom-style: dashed`
-   `border-bottom-style: dotted`
-   `border-bottom-style: double`
-   `border-bottom-style: groove`
-   `border-bottom-style: hidden`
-   `border-bottom-style: inset`
-   `border-bottom-style: none`
-   `border-bottom-style: outset`
-   `border-bottom-style: ridge`
-   `border-bottom-style: solid`

## Values

none
:   Default. Border is not drawn, color and width are ignored. If the border is an image, the image layer counts but is not drawn. See [background-image](/css/properties/background-image).

hidden
:   Same as `none`, except in terms of conflict resolution of collapsed borders. Any element with a `hidden` border suppresses all shared borders at that location. Borders with a style of none have the lowest priority.

dotted
:   A series of round or square dots.

dashed
:   A series of square-ended dashes.

solid
:   A single line segment.

double
:   Border is a double line drawn on top of the background of the object. The sum of the two single lines and the space between equals the [border-width](/css/properties/border-width) value. The border width must be at least 3 pixels wide to draw a double border.

groove
:   Looks as if it were carved in the canvas. (This is typically achieved by creating a “shadow” from two colors that are slightly lighter and darker than the [border-color](/css/properties/border-color).)

ridge
:   Looks as if it were coming out of the canvas.

inset
:   Looks as if the content on the inside of the border is sunken into the canvas.

outset
:   Looks as if the content on the inside of the border is coming out of the canvas.

## Examples

Border styles in CSS.

``` css
.one {
  border-bottom-style: none;
}

.two {
  border-bottom-style: outset;
}

.three {
  border-bottom-style: hidden;
}

.four {
  border-bottom-style: dotted;
}

.five {
  border-bottom-style: dashed;
}

.six {
  border-bottom-style: solid;
}

.seven {
  border-bottom-style: double;
}

.eight {
  border-bottom-style: groove;
}

.nine {
  border-bottom-style: ridge;
}

.ten {
  border-bottom-style: inset;
}
```

[View live example](http://code.webplatform.org/gist/5549378)

## Notes

-   Borders are drawn in front of the element's background, but behind the element's content (in case it overlaps).
-   There is no control over the spacing of the dots and dashes, nor over the length of the dashes.
-   How borders of different styles are joined in the corner may vary.
-   Rounded corners may cause the corners and the contents to overlap, if the padding is less than the radius of the corner.

## Related specifications

[CSS Level 3 - Backgrounds and Borders Module](http://www.w3.org/TR/css3-background/#border-style)
:   Candidate Recommendation

## See also

### Related articles

#### Border

-   [border](/css/properties/border)

-   [border-bottom](/css/properties/border-bottom)

-   [border-bottom-color](/css/properties/border-bottom-color)

-   [border-bottom-left-radius](/css/properties/border-bottom-left-radius)

-   **border-bottom-style**

-   [border-bottom-width](/css/properties/border-bottom-width)

-   [border-color](/css/properties/border-color)

-   [border-image](/css/properties/border-image)

-   [border-image-outset](/css/properties/border-image-outset)

-   [border-image-repeat](/css/properties/border-image-repeat)

-   [border-image-slice](/css/properties/border-image-slice)

-   [border-image-source](/css/properties/border-image-source)

-   [border-image-width](/css/properties/border-image-width)

-   [border-left](/css/properties/border-left)

-   [border-left-color](/css/properties/border-left-color)

-   [border-left-style](/css/properties/border-left-style)

-   [border-left-width](/css/properties/border-left-width)

-   [border-radius](/css/properties/border-radius)

-   [border-right](/css/properties/border-right)

-   [border-right-color](/css/properties/border-right-color)

-   [border-right-style](/css/properties/border-right-style)

-   [border-right-width](/css/properties/border-right-width)

-   [border-top](/css/properties/border-top)

-   [border-top-color](/css/properties/border-top-color)

-   [border-top-left-radius](/css/properties/border-top-left-radius)

-   [border-top-right-radius](/css/properties/border-top-right-radius)

-   [border-top-style](/css/properties/border-top-style)

-   [border-top-width](/css/properties/border-top-width)

-   [border-width](/css/properties/border-width)
