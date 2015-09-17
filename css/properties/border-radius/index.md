---
title: 'border-radius'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Border-radius](https://developer.mozilla.org/en-US/docs/CSS/border-radius) Article]'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5495188'
compatibility:
  feature: border-radius
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`0`'
  'Applies to': 'All elements, except the table element when border-collapse is collapse'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified by individual properties'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`borderRadius`'
  Percentages: 'Refer to the corresponding dimension (width or height) of the border box.'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The border-radius CSS property allows authors to round the corners of an element. The rounding can be different per-corner, and it could have different horizontal and vertical radii, to produce elliptical curves.'
tags:
  - CSS_Properties
  - CSS
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected
uri: css/properties/border-radius

---
## Summary

The border-radius CSS property allows authors to round the corners of an element. The rounding can be different per-corner, and it could have different horizontal and vertical radii, to produce elliptical curves.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `0`

Applies to
:   All elements, except the table element when border-collapse is collapse

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As specified by individual properties

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `borderRadius`

Percentages
:   Refer to the corresponding dimension (width or height) of the border box.

## Syntax

-   `border-radius: length`
-   `border-radius: length / length`
-   `border-radius: percentage`
-   `border-radius: percentage / percentage`

## Values

length
:   Denotes the size of the circle radius or the horizontal and vertical radii, for elliptical curves. It can be expressed in any unit allowed in [CSS \<length\> data types](/css/data_types/length). em units are useful for controls that scale proportionally with the font-size. Viewport-relative units (vw, vh, vmin, vmax) can be useful for controls that scale with the viewport size. Negative values are invalid. You can specify a single length for all four corners, or two, three or four lengths to specify different lengths for different corners: see the syntax section for more details.

percentage
:   Denotes the size of the corner radius, in percentages of the box’s border-box dimensions. Specifically, percentages for the horizontal axis refer to the width of the border-box, percentages for the vertical axis refer to the height of the border-box. Negative values are invalid. You can specify a single percentage for all four corners, or two, three or four percentages to specify different percentages for different corners: see the syntax section for more details.

length / length
:   Specifying two sets of length values separated by a forward slash equates to specifying separate lengths for the X and Y radii of the corners, resulting in elliptical corners if the X and Y radii have different lengths. Each set can consist of one, two, three or four values.

percentage / percentage
:   Specifying two sets of percentage values separated by a forward slash equates to specifying separate percentages for the X and Y radii of the corners, resulting in elliptical corners if the X and Y radii have percentages resulting in different computed values (depending on the width and height of the element, different percentages might result in the same computed values; see the remarks section for more). Each set can consist of one, two, three or four values.

## Examples

One value example

``` css
border-radius: 1em;

/* is equivalent to: */

border-top-left-radius: 1em;
border-top-right-radius: 1em;
border-bottom-right-radius: 1em;
border-bottom-left-radius: 1em;
```

[View live example](http://gist.github.com/5495188)

Multi value example

``` css
border-radius: 20px 1em 1vw / 0.5em 3em;

/* is equivalent to: */

border-top-left-radius: 20px 0.5em;
border-top-right-radius: 1em 3em;
border-bottom-right-radius: 1vw 0.5em;
border-bottom-left-radius: 1em 3em;
```

[View live example](http://gist.github.com/5495188)

Create an ellipse, unless the

``` css
border-radius: 50%;

/* Will be a circle if the element’s width is equal to its height */
```

[View live example](http://gist.github.com/5495188)

Shrinking curves to avoid overlapping

``` css
border-radius: 100% 150%;

/* is equivalent to: */

border-radius: 40% 60%;

/* The values shrink proportionally, all multiplied by the same factor, until there is no overlap */
```

[View live example](http://gist.github.com/5495188)

## Usage

     As with any shorthand property, individual inherited values are not possible, that is border-radius:0 0 inherit inherit, which would override existing definitions partially. In that case, the individual longhand properties have to be used.

### Syntax

`border-radius` can take between one and four values:

-   one value will be applied to all four corners
-   two values will be applied to top-left + bottom-right, and top-right + bottom-left, respectively
-   three values will be applied to top-left, top-right + bottom-left, and bottom-right, respectively
-   four values will be applied to the four corners separately, in the order of top-left, top-right, bottom-right, bottom-left

## Notes

### Remarks

-   The **border-radius** property is a composite property that specifies up to four **border-\*-radius** properties. If values are given before and after the slash, the values before the slash set the horizontal radius and the values after the slash set the vertical radius. If there is no slash ("/"), the values set both radii equally. The four values for each radii are given in clockwise order, starting from the top left corner. If less than four values are provided, they are repeated until we get four values, similarly to other CSS properties, such as border-width.
-   It’s possible to end up with elliptical corners, even by specifying one radius. This occurs when you are using percentages, since they resolve to a different number for each axis (horizontally they are percentages of the border box width, vertically of the height). For a demonstration, refer to the ellipse example above (example \#3)
-   Since border-radius rounds the border box of the element, the inner (padding box) corners will have smaller radii (specifically border-radius - border-width), or even no rounding, if the border is thicker than the border-radius value. Another consequence of this is that when there are different border widths on adjacent sides, the curves of the padding box will be elliptical.
-   Note that although in the border-radius shorthand, there is a slash (/) to separate horizontal from vertical radii, they are space separated in the longhands.

## Related specifications

[CSS Backgrounds and Borders Module Level 3: Rounded Corners:](http://www.w3.org/TR/css3-background/#the-border-radius)
:   Candidate Recommendation

[CSS Backgrounds and Borders Module Level 4: Rounded Corners:](http://dev.w3.org/csswg/css4-background/#corners)
:   Editor’s Draft

## See also

### Related articles

#### Border

-   [border](/css/properties/border)

-   [border-bottom](/css/properties/border-bottom)

-   [border-bottom-color](/css/properties/border-bottom-color)

-   [border-bottom-left-radius](/css/properties/border-bottom-left-radius)

-   [border-bottom-style](/css/properties/border-bottom-style)

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

-   **border-radius**

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

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   style[style](/css/cssom/style)
-   defaults[defaults](/w/index.php?title=dom/defaultSelected&action=edit&redlink=1)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   `Reference`
-   border-top-left-radius[border-top-left-radius](/css/properties/border-top-left-radius)
-   border-top-right-radius[border-top-right-radius](/css/properties/border-top-right-radius)
-   border-bottom-right-radius[border-bottom-right-radius](/css/properties/border-bottom-right-radius)
-   border-bottom-left-radius[border-bottom-left-radius](/css/properties/border-bottom-left-radius)
