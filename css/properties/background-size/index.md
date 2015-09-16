---
title: background-size
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/CSS/background-size)'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://jsbin.com/ejulex/2/edit'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'for \<length\> the absolute value, otherwise a percentage'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`backgroundSize`'
  Percentages: 'see text'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Specifies the size of the background images.'
tags:
  - CSS
  - Properties
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected
uri: css/properties/background-size

---
## Summary

Specifies the size of the background images.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `auto`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   for \<length\> the absolute value, otherwise a percentage

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `backgroundSize`

Percentages
:   see text

## Syntax

-   `background-size: auto`
-   `background-size: contain`
-   `background-size: cover`
-   `background-size: length`
-   `background-size: percentage`

## Values

auto
:   Default. See Remarks.

contain
:   Scale the image, while preserving its intrinsic aspect ratio (if any), to the largest size such that both its width and its height can fit inside the background positioning area.

cover
:   Scale the image, while preserving its intrinsic aspect ratio (if any), to the smallest size such that both its width and its height can completely cover the background positioning area.

length
:   A floating-point number, followed by an absolute units designator (`cm`, `mm`, `in`, `pt`, or `pc`) or a relative units designator (`em`, `ex`, or `px`).

For more information about the supported length units, see the CSS Values and Units Reference.

percentage
:   An integer, followed by a percent (%). A percentage value is relative to the background positioning area.

## Examples

Basic list of syntax examples for background-size.

``` css
/* Keywords syntax */
background-size: cover
background-size: contain

/* One-value syntax: the value defines the width of the image, the height is implicitly set to 'auto' */
background-size: 50%
background-size: 3em
background-size: 12px
background-size: auto

/* Two-value syntax: the first value defines the width of the image, the second its height */
background-size: 50% auto
background-size: 3em 25%
background-size: auto 6px
background-size: auto auto

/* Values for the multiple backgrounds, defined by background-image, may be listed separated by commas */
background-size: auto, auto     /* Do not confuse this with background-size: auto auto */
background-size: 50%, 25%, 25%
background-size: 6px, auto, contain

background-size: inherit
```

HTML structure of a series of `<div>`s that are identical except that they have different `background-size` values applied to the background image.

``` html
<p>Original image is 273 x 286 px, and has a transparent area around the outside of roughly 45px.</p>

<div class="one"><code>background-size: auto auto;</code></div>
<div class="two"><code>background-size: contain;</code></div>
<div class="three"><code>background-size: cover;</code></div>
<div class="four"><code>background-size: 20% 25%;</code></div>
<div class="five"><code>background-size: 100px 400px;</code></div>
<div class="six"><code>background-size: 100% 250px;</code></div>
<div class="seven"><code>background-size: 100% 250px, 20% 25%;</code></div>
```

CSS applied to the HTML example seen above.

``` css
div {
   width: 17%;
   height: 200px;
   padding: 10px;
   border-radius: 20px;
   box-shadow: 2px 2px 10px rgba(0,0,0,0.75);
   float: left;
   margin: 0 20px 20px 0;
   background-color: rgba(0,0,0,0.25);
   background-image: url(http://www.webplatform.org/logo/wplogo_transparent_xlg.png);
 }

 code {
   background-color: rgba(255,255,255,0.7);
   padding: 2px;
   border-radius: 5px
 }

.one {
  background-size: auto auto;
}

.two {
  background-size: contain;
}

.three {
  background-size: cover;
}

.four {
  background-size: 20% 25%;
}

.five {
  background-size: 100px 400px;
}

.six {
  background-size: 100% 250px;
}

.seven {
  background-image: url(http://www.webplatform.org/logo/wplogo_transparent_xlg.png), url(http://www.webplatform.org/logo/wplogo_transparent_xlg.png);
  background-size: 100% 250px, 20% 25%;
}
```

[View live example](http://jsbin.com/ejulex/2/edit)

## Notes

### Remarks

An `auto` value for one dimension is resolved by using the image's intrinsic ratio and the size of the other dimension. If either of these values is not available, the image's intrinsic size is used. If the image's intrinsic size is not available, it is assigned the value of 100%. If both values are `auto`, use the intrinsic width, height, or both, of the image. If the image has neither an intrinsic width nor an intrinsic height, its size is determined as for `contain`. Negative values are not allowed. In Windows Internet Explorer 9, the background of a box can have multiple layers. The number of layers is determined by the number of comma-separated values in the [**background-image**](/css/properties/background-image) property. Each of the images is sized, positioned, and tiled according to the corresponding value in the other background properties ([**background-attachment**](/css/properties/background-attachment), [**background-clip**](/css/properties/background-clip), [**background-origin**](/css/properties/background-origin), [**background-position**](/css/properties/background-position), [**background-repeat**](/css/properties/background-repeat), and **background-size**). The first image in the list is the layer closest to the user, the next one is painted behind the first, and so on.

## Related specifications

[CSS Backgrounds and Borders Module Level 3](http://www.w3.org/TR/css3-background/#the-background-size)
:   Candidate Recommendation

## See also

### Related articles

#### Background

-   [background](/css/cssom/properties/background)

-   [background](/css/properties/background)

-   [background-attachment](/css/properties/background-attachment)

-   [background-blend-mode](/css/properties/background-blend-mode)

-   [background-clip](/css/properties/background-clip)

-   [background-color](/css/properties/background-color)

-   [background-image](/css/properties/background-image)

-   [background-origin](/css/properties/background-origin)

-   [background-position](/css/properties/background-position)

-   [background-position-x](/css/properties/background-position-x)

-   [background-position-y](/css/properties/background-position-y)

-   [background-repeat](/css/properties/background-repeat)

-   **background-size**

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

### Related pages (MSDN)

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `defaults`
-   `LayoutRect`
-   `runtimeStyle`
-   `style`
-   `style`
-   `Reference`
-   `background-color`
-   `background-image`
-   `background-repeat`
-   `background-attachment`
-   `background-position`
-   `background-clip`
-   `background-origin`
-   `background`
