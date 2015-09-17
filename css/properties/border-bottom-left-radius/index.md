---
title: 'border-bottom-left-radius'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Border-bottom-left-radius](https://developer.mozilla.org/es/docs/CSS/border-bottom-left-radius) Article]'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: border-bottom-left-radius
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`0`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'two absolute \<length\> or percentages'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`borderBottomLeftRadius`'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Defines the shape of the border of the bottom-left corner.'
tags:
  - CSS_Properties
  - CSS
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected
uri: css/properties/border-bottom-left-radius

---
## Summary

Defines the shape of the border of the bottom-left corner.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `0`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   two absolute \<length\> or percentages

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `borderBottomLeftRadius`

## Syntax

-   `border-bottom-left-radius: length`
-   `border-bottom-left-radius: percentage`

## Values

length
:   Denotes the size of the circle radius or the semi-major and semi-minor axes of the ellipsis. It can be expressed in any unit allowed by the [CSS \<length\> data types](/css/data_types/length). Negative values are invalid.

percentage
:   Denotes the size of the circle radius, or the semi-major and semi-minor axes of the ellipsis, using percentage values. Percentages for the horizontal axis refer to the width of the box, percentages for the vertical axis refer to the height of the box. Negative values are invalid.

## Examples

One value example to use an arc of circle as the border on the top left corner.

``` css
border-bottom-left-radius: 10px;

/* is equivalent to: */
border-bottom-left-radius: 10px 10px;
```

Two value example to use an arc of ellipse as the border on the top left corner.

``` css
border-bottom-left-radius: 10px 5px;
```

One value percentage example on the top left corner. If the box is a square an arc of circle is used as the border, if the box is not a square an arc of ellipse is used as the border.

``` css
border-bottom-left-radius: 30%;
```

## Notes

### Remarks

The **border-bottom-left-radius** property specifies the horizontal and vertical radii of the ellipse that defines the rounded lower-left corner of a border box. If there is only one value given, then that value specifies both horizontal and vertical radii of the ellipse. If there are two values given, then the first value sets the horizontal radius and the second value sets the vertical radius.

## Related specifications

[CSS Backgrounds and Borders Module Level 3: Rounded Corners:](http://www.w3.org/TR/css3-background/#border-bottom-left-radius)
:   Candidate Recommendation

## See also

### Related articles

#### Border

-   [border](/css/properties/border)

-   [border-bottom](/css/properties/border-bottom)

-   [border-bottom-color](/css/properties/border-bottom-color)

-   **border-bottom-left-radius**

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

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   style[style](/css/cssom/style)
-   defaults[defaults](/w/index.php?title=dom/defaultSelected&action=edit&redlink=1)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   `Reference`
-   border-radius[border-radius](/css/properties/border-radius)
-   border-top-left-radius[border-top-left-radius](/css/properties/border-top-left-radius)
-   border-top-right-radius[border-top-right-radius](/css/properties/border-top-right-radius)
-   border-bottom-right-radius[border-bottom-right-radius](/css/properties/border-bottom-right-radius)
