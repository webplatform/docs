---
title: 'border-style'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5544029'
compatibility:
  feature: border-style
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'specified value'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`borderStyle`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Sets the style of an element''s four borders. This property can have from one to four values. With only one value, the value will be applied to all four borders; otherwise, this works as a shorthand property for each of border-top-style, border-right-style, border-bottom-style, border-left-style, where each border style may be assigned a separate value.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/border-style

---
## Summary

Sets the style of an element's four borders. This property can have from one to four values. With only one value, the value will be applied to all four borders; otherwise, this works as a shorthand property for each of border-top-style, border-right-style, border-bottom-style, border-left-style, where each border style may be assigned a separate value.

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
:   `borderStyle`

Percentages
:   N/A

## Syntax

-   `border-style: <border-top-style> <border-right-style> <border-bottom-style> <border-left-style>`
-   `border-style: dashed`
-   `border-style: dotted`
-   `border-style: double`
-   `border-style: groove`
-   `border-style: hidden`
-   `border-style: inset`
-   `border-style: none`
-   `border-style: outset`
-   `border-style: ridge`
-   `border-style: solid`

## Values

none
:   Default. Border is not drawn, color and width are ignored. If the border is an image, the image layer counts but is not drawn. See [background-image](/css/properties/background-image).

hidden
:   Same as `none`, except in terms of conflict resolution of collapsed borders. Any element with a `hidden` border suppresses all shared borders at that location. Borders with a style of none have the lowest priority.

dotted
:   A series of round dots.

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

\<border-top-style\> \<border-right-style\> \<border-bottom-style\> \<border-left-style\>
:   Shorthand values syntax.

## Examples

Border styles in CSS.

``` css
.one {
  border-style: none;
}

.two {
  border-style: outset;
}

.three {
  border-style: hidden;
}

.four {
  border-style: dotted;
}

.five {
  border-style: dashed;
}

.six {
  border-style: solid;
}

.seven {
  border-style: double;
}

.eight {
  border-style: groove;
}

.nine {
  border-style: ridge;
}

.ten {
  border-style: inset;
}
```

[View live example](http://gist.github.com/5544029)

## Usage

     * Up to four different styles can be specified, in the following order: top, right, bottom, left.

-   If one style is specified, it is used for all four sides. If two styles are specified, the first is used for the top and bottom borders, and the second is used for left and right borders. If three styles are specified, they are used for top, right/left, and bottom borders, respectively. If left is missing, it is the same as right; if bottom is missing, it is the same as top; if right is missing, it is the same as top.

## Notes

-   Borders are drawn in front of the element's background, but behind the element's content (in case it overlaps).
-   There is no control over the spacing of the dots and dashes, nor over the length of the dashes.
-   How borders of different styles are joined in the corner may vary.
-   Rounded corners may cause the corners and the contents to overlap, if the padding is less than the radius of the corner.

## Related specifications

[CSS Level 3 - Backgrounds and Borders Module](http://www.w3.org/TR/css3-background/#border-style)
:   Candidate Recommendation

## See also

### Other articles

Related CSS properties:

-   [border-top-style](/css/properties/border-top-style)
-   [border-right-style](/css/properties/border-right-style)
-   [border-bottom-style](/css/properties/border-bottom-style)
-   [border-left-style](/css/properties/border-left-style)

Related tutorials:

-   [Decorating fancy borders with CSS border-image](/tutorials/css_border_image)

### External resources

-   [CSS border-style property on MDN](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=4&cad=rja&ved=0CE4QFjAD&url=https%3A%2F%2Fdeveloper.mozilla.org%2Fen-US%2Fdocs%2FWeb%2FCSS%2Fborder-style&ei=um2mUb2QC6mliQKE-IHwDg&usg=AFQjCNHuEil-o7WWpH1wxOt_DzFDy_lm-A&sig2=Ifwz1_Fq4GzjkJct0EfFxw&bvm=bv.47244034,d.cGE)
-   [CSS border-style property on SitePoint](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=8&cad=rja&ved=0CHIQFjAH&url=http%3A%2F%2Freference.sitepoint.com%2Fcss%2Fborder-style&ei=um2mUb2QC6mliQKE-IHwDg&usg=AFQjCNGjOxzgETcUxPFZD3txXZ3rgghK8Q&sig2=H8jwjVBXF55U1h_a6E3HsA&bvm=bv.47244034,d.cGE)
