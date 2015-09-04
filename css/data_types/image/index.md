---
title: image
tags:
  - Data
  - Type
  - CSS
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The <image> CSS data type represents graphical content.  Images are usually specified with the url() function, but may also be created with a gradient function.  Other syntaxes are defined but not widely implemented.'
uri: 'css/data types/image'

---
# \<image\>

## Summary

The \<image\> CSS data type represents graphical content. Images are usually specified with the url() function, but may also be created with a gradient function. Other syntaxes are defined but not widely implemented.

 In CSS, images may be used as property values for backgrounds, borders, custom list bullets and for pseudo-element content. The `<image>` data type is introduced in CSS3; in CSS 2.1 and earlier the only way to specify an image was with the [`url()` function](/css/functions/url()) and so the `<uri>` data type was sufficient.

The [CSS Image Values and Replaced Content Module](http://www.w3.org/TR/css3-images) defines four ways in which an image may be specified:

-   As a reference to an image file (or SVG file fragment), specified using the same syntax as the [`<url>`](/css/data_types/url) data type.

-   As a gradient, using one of the four CSS gradient functions: [`linear-gradient()`](/css/functions/linear-gradient), [`radial-gradient()`](/css/functions/radial-gradient), [`repeating-linear-gradient()`](/css/functions/repeating-linear-gradient), or [`repeating-radial-gradient()`](/css/functions/repeating-radial-gradient).

-   As a reference to a mark-up element on the page, specified using the `element(#id)` function; the "live" displayed state of that element would be copied into the property referencing this image. (This function has been removed from the current (level 3) recommendation.)

-   As a list of one or more image options, specified with the `image()` function. The parameters to the function are a list of comma-separated values, starting with the value preferred image and (optionally) followed by various fallback alternatives. Each image value could be given as absolute or relative file paths, possibly including [media fragment identifiers](http://www.w3.org/TR/media-frags/#naming-space) to clip the image, or an element or gradient function. As a final fallback, the last parameter to the `image()` function could be a solid [`<color>`](/css/data_types/color) value.

Only the first two options are commonly implemented, and even browsers that support gradients as images may not support them for all image properties.

## Examples

``` {.css}
div.feature {
   /* a list of images to layer in the background */
   background-image: url("images/logo.svg"),
         linear-gradient(to left, lightblue 30%, midnightblue);
}
```

## Related specifications

Specification
:   Status
[CSS Values and Units Module Level 3](http://www.w3.org/TR/css3-values/#images)
:   Candidate Recommendation
[CSS Image Values and Replaced Content Module Level 3](http://www.w3.org/TR/css3-images/#image-values)
:   Candidate Recommendation
[CSS Image Values and Replaced Content Module Level 3](http://www.w3.org/TR/2012/WD-css3-images-20120112/)
:   Working Draft

