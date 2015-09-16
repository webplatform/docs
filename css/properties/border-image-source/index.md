---
title: border-image-source
code_samples:
  - 'http://gist.github.com/5621011'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'all elements, except table elements where `border-collapse: collapse` is applied'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': '‘none’ or the image with its URI made absolute'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`borderImageSource`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The property border-image-source is used to set the image to be used instead of the border style. If this is set to none the border-style is used instead.'
tags:
  - CSS
  - Properties
uri: css/properties/border-image-source

---
## Summary

The property border-image-source is used to set the image to be used instead of the border style. If this is set to none the border-style is used instead.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `none`

Applies to
:   all elements, except table elements where `border-collapse: collapse` is applied

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   ‘none’ or the image with its URI made absolute

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `borderImageSource`

Percentages
:   N/A

## Syntax

-   `border-image-source: none`
-   `border-image-source: url(path/to/image.png)`

## Values

none
:   Default. `border-style` is used instead.

url(path/to/image.png)
:   This value contains a path to an image that you want to apply to the element in question as a background image, using the CSS images syntax, as described at ["CSS images: url()"](/css/functions/url()).

## Examples

A simple example showing a \<div\> that has border-image-source property and other border-image properties.

``` html
<div class="pattern">border-image</div>
```

[View live example](http://code.webplatform.org/gist/5621011)

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

/* This general class will apply the pattern to the containers */
.pattern {
    border-image-source: url(http://docs.webplatform.org/w/images/d/d8/border-image.png);
    border-image-slice: 30;
    border-image-width: 6;
    border-image-outset: 3;
}
```

[View live example](http://code.webplatform.org/gist/5621011)

## Related specifications

[CSS Level 3 - Backgrounds and Borders Module](http://www.w3.org/TR/css3-background/#the-border-image-source)
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

-   [border-image](/css/properties/border-image)

-   [border-image-outset](/css/properties/border-image-outset)

-   [border-image-repeat](/css/properties/border-image-repeat)

-   [border-image-slice](/css/properties/border-image-slice)

-   **border-image-source**

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
