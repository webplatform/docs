---
title: 'border-image-slice'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/CSS/border-image-slice)'
code_samples:
  - 'http://gist.github.com/6949408'
compatibility:
  feature: border-image-slice
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`100%`'
  'Applies to': 'all elements, except internal table elements when `border-collapse` is set to `collapse`.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`borderImageSlice`'
  Percentages: 'refer to size of the border image'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Divides the image specified by border-image-source in nine regions: the four corners, the four edges and the middle. It does this by specifying 4 inward offsets.'
tags:
  - CSS
  - Properties
uri: css/properties/border-image-slice

---
## Summary

Divides the image specified by border-image-source in nine regions: the four corners, the four edges and the middle. It does this by specifying 4 inward offsets.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `100%`

Applies to
:   all elements, except internal table elements when `border-collapse` is set to `collapse`.

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   as specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `borderImageSlice`

Percentages
:   refer to size of the border image

## Syntax

-   `border-image-slice: <number>`
-   `border-image-slice: <percentage>`
-   `border-image-slice: fill`
-   `border-image-slice: inherit`

## Values

\<number\>
:   Represents pixels for raster images and coordinates for vector images.

\<percentage\>
:   Percentages values are relative to the height or width of the image, whichever is adequate.

fill
:   Is a keyword whose presence forces the use of the middle image slice to be displayed over the background image, its size and height are resized like those of the top and left image slices, respectively.

inherit
:   Is a keyword indicating that all four values are inherited from their parent's element calculated value.

## Examples

A simple example showing multiple \<div\>s, identical in style except that they have different border-image-slice properties applied to them.

``` html
<div class="pattern one">one</div>
<div class="pattern two">two</div>
<div class="pattern three">three</div>
<div class="pattern four">four</div>
```

[View live example](http://code.webplatform.org/gist/6949408)

``` css
/**
*   Border-image-slice Live Example
*   @see http://docs.webplatform.org/wiki/css/properties/border-image-slice
*/

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
    border-image-width: 6;
    border-image-outset: 3;
    border-image-repeat: repeat;

}

/* One-value syntax */
.pattern.one{
    border-image-slice: 30;
}

/* Two-value syntax */
.pattern.two{
    border-image-slice: 30 20;
}

/* Three-value syntax */
.pattern.three{
    border-image-slice: 20 15 30;
}

/* Four-value syntax */
.pattern.four{
    border-image-slice: 25 20 30 15;
}
```

[View live example](http://code.webplatform.org/gist/6949408)

## Usage

     * Up to four different values can be specified, in the following order: top, right, bottom, left.

-   If one value is specified, it is used for all four sides. If two values are specified, the first is used for the top and bottom slice-lines, and the second is used for left and right sides. If three values are specified, they are used for top, right/left, and bottom slice-lines, respectively. If left is missing, it is the same as right; if bottom is missing, it is the same as top; if right is missing, it is the same as top.

## Related specifications

[CSS Level 3 - Backgrounds and Borders Module](http://www.w3.org/TR/css3-background/#the-border-image-slice)
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

-   **border-image-slice**

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
