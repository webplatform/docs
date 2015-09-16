---
title: 'shape-outside'
code_samples:
  - 'http://gist.github.com/5832982'
compatibility:
  feature: shape-outside
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': Floats
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As defined for \<basic-shape\> (with \<shape-box\> following, if supplied), the \<image\> with its URI made absolute, otherwise as specified.'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Declares a shape around which text should be wrapped, with possible modifications from the shape-margin property. The shape defined by shape-outside and shape-margin changes the geometry of a float element''s float area.'
tags:
  - CSS
  - Properties
uri: css/properties/shape-outside

---
## Summary

Declares a shape around which text should be wrapped, with possible modifications from the shape-margin property. The shape defined by shape-outside and shape-margin changes the geometry of a float element's float area.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `none`

Applies to
:   Floats

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As defined for \<basic-shape\> (with \<shape-box\> following, if supplied), the \<image\> with its URI made absolute, otherwise as specified.

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   N/A

## Syntax

-   `shape-outside: <basic-shape>`
-   `shape-outside: <image>`
-   `shape-outside: <shape-box>`
-   `shape-outside: none`

## Values

none
:   The float area is unaffected.

\<basic-shape\>
:   The shape is computed based on the values of one of *inset, circle, ellipse* or *polygon*. If shape-box is not supplied, then the reference box defaults to margin-box.

-   `inset(<shape-arg>{1,4} [round<border-radius>])`. Defines an inset rectangle. The basic syntax for inset is the same as the margin shorthand syntax (see [margin](/css/properties/margin) for details). The optional border-radius argument defines an inset's rounded corners using the border-radius shorthand syntax (see [border-radius](/css/properties/border-radius) for details).

-   `circle([<shape-radius>] [at <position>])` The shape-radius argument is the radius of the circle. The position argument defines the center point of the circle and has the same syntax as background-position (see [background-position](/css/properties/background-position) for details).

-   `ellipse([<shape-radius>{2}] [at <position>])` The shape-radius argument is the radius of the circle. The position argument defines the center point of the circle and has the same syntax as background-position (see [background-position](/css/properties/background-position) for details).

-   `polygon([<fill-rule>,] [<shape-arg> <shape-arg>]# )` The fill-rule is used to determine the interior of the polygon (see the SVG [fill-rule](/svg/attributes/fill-rule) for details). Each pair in the shape-arg represents x and y coordinates of each vertex in the polygon.

\<shape-box\>
:   The shape is defined by the CSS Box Model of the element the shape is applied to:

-   `margin-box`
-   `border-box`
-   `padding-box`
-   `content-box`

\<image\>
:   If \<image\> references an image (fetched using the CORS-enabled fetch method defined by the HTML5 specification), the shape is extracted and computed based on the alpha channel of the image as defined by [shape-image-threshold](/css/properties/shape-image-threshold). If \<image\> does not reference an image or if the fetch attempt results in any error such that there is no fallback image, the effect is as if the value *auto* had been specified.

## Examples

``` css
/* shape used is a rectangle equal to the margin box */
shape-outside: inset(0 0 0 0);
/* Or equivalent: */
shape-outside: inset(0);
/* Or equivalent: */
shape-outside: margin-box;

/* shape used is an inset rectangle 10px smaller than the content box in each dimension */
shape-outside: inset(5px 5px 5px 5px);
/* Or equivalent: */
shape-outside: inset(5px);

/* shape used is a rounded rectangle */
shape-outside: inset(0 round 20px) border-box;
/* Or equivalent: */
border-radius: 20px;
shape-outside: border-box;

/* shape used is a circle filling the content box */
shape-outside:  circle();
/* Or equivalent: */
shape-outside:  circle() at center;
/* Or equivalent: */
shape-outside:  circle(50%);
/* Or equivalent: */
shape-outside:  circle(50% at center);

/* shape used is an ellipse, wider than it is tall */
shape-outside:  ellipse(50% 30%);
/* Or equivalent: */
shape-outside:  ellipse(50% 30% at center);

/* shape used is a diamond, described as a polygon */
shape-outside: polygon(50% 0, 100% 50%, 50% 100%, 0 50%);

/* shape used is the alpha channel of an image file */
shape-outside: url(path/to/image.png);
```

[View live example](http://code.webplatform.org/gist/5832982)

## Usage

     Currently implemented as an experimental feature in WebKit and Blink. This can be used with a -webkit- prefix in WebKit nightly builds and with a -webkit- prefix in Chrome Canary builds with experimental-webkit-features enabled: chrome://flags/#enable-experimental-webkit-features

## Related specifications

[CSS Shapes Module Level 1](http://www.w3.org/TR/css-shapes/)
:   W3C Candidate Recommendation

## See also

### Other articles

[shape-margin](/css/properties/shape-margin) [shape-image-threshold](/css/properties/shape-image-threshold)
