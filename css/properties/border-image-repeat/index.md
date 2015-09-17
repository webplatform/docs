---
title: 'border-image-repeat'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/CSS/border-image-repeat)'
code_samples:
  - 'http://gist.github.com/5620804'
compatibility:
  feature: border-image-repeat
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`stretch`'
  'Applies to': 'all elements, except table elements when border-collapse is collapse'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`borderImageRepeat`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The border-image-repeat CSS property defines how the middle part of a border image is handled to match the size of the border. It has a one-value syntax which describes the behavior for all sides, and a two-value syntax that sets a different value for the horizontal and vertical behavior.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/border-image-repeat

---
## Summary

The border-image-repeat CSS property defines how the middle part of a border image is handled to match the size of the border. It has a one-value syntax which describes the behavior for all sides, and a two-value syntax that sets a different value for the horizontal and vertical behavior.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `stretch`

Applies to
:   all elements, except table elements when border-collapse is collapse

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   as specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `borderImageRepeat`

Percentages
:   N/A

## Syntax

-   `border-image-repeat: inherit`
-   `border-image-repeat: repeat`
-   `border-image-repeat: round`
-   `border-image-repeat: space`
-   `border-image-repeat: stretch`

## Values

stretch
:   Is a keyword indicating that the image will be stretched to fit the gap between the borders.

repeat
:   Is a keyword indicating that the image will be repeated until it fit the gap between the borders

round
:   Is a keyword indicating that the image will be repeated until it fit the gap between the borders. If it doesn't fit after having being repeated an integer number of times, it is rescaled to do so.

space
:   Is a keyword indicating that the image will be repeated until it fit the gap between the borders. If it doesn't fit after having being repeated a whole number of times, the white space is distributed around the tiles.

inherit
:   Is a keyword indicating that all four values are inherited from their parent's element calculated value.

## Examples

A simple example showing multiple \<div\>s, identical in style except that they have different border-image-repeat properties applied to them.

``` html
<div class="pattern repeat">Repeat</div>
<div class="pattern stretch">Stretch</div>
<div class="pattern round">Round</div>
<div class="pattern space">Space</div>
```

[View live example](http://gist.github.com/5620804)

``` css
/* This general class will apply the pattern to the containers */
.pattern {
    border-image-source: url(http://docs.webplatform.org/w/images/d/d8/border-image.png);
    border-image-slice: 30;
    border-image-width: 6;
    border-image-outset: 3;
}

/* Repeat Pattern */
.pattern.repeat{
    border-image-repeat: repeat;
}

/* Stretch Pattern */
.pattern.stretch{
    border-image-repeat: stretch;
}

/* Round Pattern
   Currently available on Gecko browsers (eg: Firefox) */
.pattern.round{
    border-image-repeat: round;
}

/* Space Repeat Setting
   Currently unavailable on all browsers */
.pattern.space{
    border-image-repeat: space;
}
```

[View live example](http://gist.github.com/5620804)

``` html
[[File:border-image.png|border-image demo image]]

<code>border-image-repeat: stretch;</code>
[[File:bi-stretch.png|border-image stretch demo]]

<code>border-image-repeat: repeat;</code>
[[File:bi-repeat.png|border-image repeat demo]]

<code>border-image-repeat: round;</code>
[[File:bi-round.png|border-image round demo]]
/* Round is supported by Gecko-based browsers only, like Firefox */

<code>border-image-repeat: space;</code>
[[File:bi-space.png|border-image space demo]]

/* Space is not supported by any browser */
```

## Usage

     If one velue is specified, it is used for all four sides. If two values are specified, the first is used for the horizontal sides, and the second is used for vertical ones.

## Related specifications

[CSS Level 3 - Backgrounds and Borders Module](http://www.w3.org/TR/css3-background/#the-border-image-repeat)
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

-   **border-image-repeat**

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
