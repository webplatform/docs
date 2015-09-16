---
title: 'background-image'
code_samples:
  - 'http://chrisdavidmills.github.com/background-image/background-image.html'
compatibility:
  feature: background-image
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified, but with URIs made absolute'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`backgroundImage`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Applies one or more background images to an element. These can be any valid CSS image, including url() paths to image files or CSS gradients.'
tags:
  - CSS
  - Properties
uri: css/properties/background-image

---
## Summary

Applies one or more background images to an element. These can be any valid CSS image, including url() paths to image files or CSS gradients.

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
:   As specified, but with URIs made absolute

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `backgroundImage`

Percentages
:   N/A

## Syntax

-   `background-image: <image>`
-   `background-image: <image>, <image>, …`
-   `background-image: none`

## Values

none
:   Default. Color of the next parent through which the background is visible.

\<image\>
:   Any valid CSS image value, including image files through [CSS images: url()](/css/functions/url()) or CSS gradients.

\<image\>, \<image\>, …
:   You can apply multiple background images to a single element (image files, gradients, or a mixture) by including all the image references in the property value, with each one separated by a comma. Images referenced earlier in the property value appear in front of images referenced later.

## Examples

Three simple div elements

``` html
<!DOCTYPE HTML>
<html lang="en-US">
<head>
  <meta charset="UTF-8">
  <title>Background-image example</title>
  <link href="background-image.css" type="text/css" rel="stylesheet">
</head>
<body>

  <div class="one">One</div>
  <div class="two">Two</div>
  <div class="three">Three</div>

</body>
</html>
```

The first div has a simple image file applied to it, the second div has a background gradient applied to it, and the third div has both applied simultaneously.

``` css
.one {
  background-image: url(images/icon.png);
  /* here we are applying a single background image to our first block level container element */
  /* (could be anything, but it is a div in the live example. */
}

.two {
  background-image: linear-gradient(to bottom, #aaa, #eee);
  /* Here we are applying a linear gradient to our second block level container. */
}

.three {
  background-image: url(images/icon.png), linear-gradient(to bottom, #aaa, #eee);
  /* In this case we are applying both the background image and the gradient to our third block level container. */
}
```

[View live example](http://chrisdavidmills.github.com/background-image/background-image.html)

## Usage

     Background images in general have good support across browsers; there are a few things to take note of, however:

-   Older browsers do not support multiple background images, SVG as background images or CSS gradients, so be careful when using these options to make sure that a fallback is provided that will make content readable on older browsers, such as a simple solid colour.
-   When using multiple background images, the image at the start of the comma delimited list appears on top of ones later on. This might seem contrary to how CSS is expected to behave.
-   Because gradients are still supported in some browsers with prefixes and some not, and some with a slightly older syntax, you should use multiple background gradient properties with different syntaxes, as shown in the below examples.

## Notes

Internationalization topics related to the `background-image` property:

-   [Preparing for text expansion](http://localhost/International/techniques/authoring-html#textexpansion)

## Related specifications

[CSS 2.1](http://www.w3.org/TR/CSS2/colors.html#propdef-background-image)
:   W3C Recommendation

[CSS Backgrounds and Borders Module Level 3](http://www.w3.org/TR/css3-background/#the-background-image)
:   W3C Candidate Recommendation

## See also

### Related articles

#### Background

-   [background](/css/cssom/properties/background)

-   [background](/css/properties/background)

-   [background-attachment](/css/properties/background-attachment)

-   [background-blend-mode](/css/properties/background-blend-mode)

-   [background-clip](/css/properties/background-clip)

-   [background-color](/css/properties/background-color)

-   **background-image**

-   [background-origin](/css/properties/background-origin)

-   [background-position](/css/properties/background-position)

-   [background-position-x](/css/properties/background-position-x)

-   [background-position-y](/css/properties/background-position-y)

-   [background-repeat](/css/properties/background-repeat)

-   [background-size](/css/properties/background-size)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

### Other articles

-   [Using CSS background images](/tutorials/using_css_background_images)
-   [Creating gradients in CSS](/tutorials/creating_gradients_in_css)

### External resources

-   [Get to grips with CSS3 multiple background images](http://www.netmagazine.com/tutorials/get-grips-css3-multiple-background-images), by Prisca Schmarsow
