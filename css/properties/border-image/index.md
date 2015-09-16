---
title: 'border-image'
code_samples:
  - 'http://gist.github.com/5622521'
compatibility:
  feature: border-image
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`based on individual properties`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'based on individual properties'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`borderImage`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Shorthand property that defines an image to be displayed and its positioning, instead of a solid color, for ''border'' property. It can be used to set border-image-source, border-image-slice, border-image-width, border-image-outset and border-image-repeat, or a subset of these.'
tags:
  - CSS
  - Properties
uri: css/properties/border-image

---
## Summary

Shorthand property that defines an image to be displayed and its positioning, instead of a solid color, for 'border' property. It can be used to set border-image-source, border-image-slice, border-image-width, border-image-outset and border-image-repeat, or a subset of these.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `based on individual properties`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   based on individual properties

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `borderImage`

Percentages
:   N/A

## Syntax

-   `border-image: border-image-source border-image-slice border-image-width border-image-outset border-image-repeat`

## Values

border-image-source border-image-slice border-image-width border-image-outset border-image-repeat
:   The `border-image` property can contain up to five components:

-   `border-image-source`: This can take a valid ["CSS images: url()"](/css/functions/url()) as its value.
-   `border-image-slice`: This takes any of the values available to the [**border-image-slice**](/css/properties/border-image-slice) property, which includes \<number\>, \<percentage\> and `fill`. For more details about each, see the [**border-image-slice**](/css/properties/border-image-slice) page.
-   `border-image-width`: This takes a numeric value with any of the standard length units.
-   `border-image-outset`: This takes a numeric value with any of the standard length units.
-   `border-image-repeat`: This takes any of the type of values available to the [**border-image-repeat**](/css/properties/border-image-repeat) property, which includes `stretch`, `repeat`, `round` and `space`. For more details about each, see the [**border-image-repeat**](/css/properties/border-image-repeat) page.

## Examples

A simple example showing a \<div\>.

``` css
<div class="pattern">one</div>
```

[View live example](http://code.webplatform.org/gist/5622521)

``` css
/* General setup of the containers */
div {
    height: 100px;
    width: 100px;
    margin: 25px;
    text-align: center;
    line-height: 100px;
    font-family: sans-serif;
}

.pattern {
    border: 30px solid transparent;
    border-image: url(http://docs.webplatform.org/w/images/d/d8/border-image.png) 30 repeat;
}
```

[View live example](http://code.webplatform.org/gist/5622521)

## Notes

[**border-image-slice: fill**](/css/properties/border-image-slice) was introduced in latest recommendation and breaks backwards compatibility. If you want border-image to fill an inner area of your block you have to use this property.

### Compatibility with other properties

[**border-radius**](/css/properties/border-radius) has no effect on border-image.

## Related specifications

[CSS Backgrounds and Borders Module Level 3](http://www.w3.org/TR/css3-background/)
:   W3C Candidate Recommendation

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

-   **border-image**

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

### Other articles

-   [Decorating fancy borders with CSS border-image](/tutorials/css_border_image)
