---
title: 'border-image-width'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/CSS/border-image-width)'
code_samples:
  - 'http://gist.github.com/5621387'
compatibility:
  feature: border-image-width
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'all elements, except internal table elements when `border-collapse` is set to `collapse`.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'all length made absolute, or as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`borderImageWidth`'
  Percentages: 'Relative to the width, for horizontal effects, or the height, for vertical effects, of the border image area.'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The border-image-width CSS property defines the offset to use for dividing the border image in nine parts, the top-left corner, central top edge, top-right-corner, central right edge, bottom-right corner, central bottom edge, bottom-left corner, and central right edge. They represent inward distance from the top, right, bottom, and left edges.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/border-image-width

---
## Summary

The border-image-width CSS property defines the offset to use for dividing the border image in nine parts, the top-left corner, central top edge, top-right-corner, central right edge, bottom-right corner, central bottom edge, bottom-left corner, and central right edge. They represent inward distance from the top, right, bottom, and left edges.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `none`

Applies to
:   all elements, except internal table elements when `border-collapse` is set to `collapse`.

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   all length made absolute, or as specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `borderImageWidth`

Percentages
:   Relative to the width, for horizontal effects, or the height, for vertical effects, of the border image area.

## Syntax

-   `border-image-width: <length>`
-   `border-image-width: <number>`
-   `border-image-width: <percentage>`
-   `border-image-width: auto`

## Values

\<length\>
:   Represents the length of the image slice. It can be an absolute or relative length. This length must not be negative.

\<percentage\>
:   Represents the percentage of the image slice relative to the height, or width, of the border image area. The percentage must not be negative.

\<number\>
:   Represents a multiple of the computed value of the element's `border-width` property to be used as the image slice size. The number must not be negative.

auto
:   Indicates that the width, or height, of the image size must be the intrinsic size of that dimension.

## Examples

A simple example showing multiple \<div\>s, identical in style except that they have different border-image-width properties applied to them.

``` html
<div class="pattern one">one</div>
<div class="pattern two">two</div>
<div class="pattern three">three</div>
<div class="pattern four">four</div>
```

[View live example](http://gist.github.com/5621387)

``` css
/* This general class will apply the pattern to the containers */
.pattern {
    border-image-source: url(http://docs.webplatform.org/w/images/d/d8/border-image.png);
    border-image-slice: 30;
    border-image-repeat: repeat;
    border-image-outset: 3;
}

/* One-value syntax */
.pattern.one{
    border-image-width: 3;
}

/* Two-value syntax */
.pattern.two{
    border-image-width: 1.2em 1.8em;
}

/* Three-value syntax */
.pattern.three{
    border-image-width: 5% 15% 10%;
}

/* Four-value syntax */
.pattern.four{
    border-image-width: 5% 2em 10% auto;
}
```

[View live example](http://gist.github.com/5621387)

## Usage

     * Up to four different widths can be specified, in the following order: top, right, bottom, left.

-   If one width is specified, it is used for all four sides. If two widths are specified, the first is used for the top and bottom borders, and the second is used for left and right borders. If three widths are specified, they are used for top, right/left, and bottom borders, respectively. If left is missing, it is the same as right; if bottom is missing, it is the same as top; if right is missing, it is the same as top.

## Related specifications

[CSS Level 3 - Backgrounds and Borders Module](http://www.w3.org/TR/css3-background/#the-border-image-width)
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

-   [border-image-source](/css/properties/border-image-source)

-   **border-image-width**

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
