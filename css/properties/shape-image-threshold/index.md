---
title: shape-image-threshold
code_samples:
  - 'http://gist.github.com/5833790'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`0.0`'
  'Applies to': Floats
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified, clamped to a 0.0-1.0 range'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: '[[CSS percentages::Alpha channel of the image specified by [shape-outside](/css/properties/shape-outside).]]'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Defines the alpha channel threshold used to extract a shape from an image. Can be thought of as a &quot;minimum opacity&quot; threshold; that is, a value of 0.5 means that the shape will enclose all the pixels that are more than 50% opaque.'
tags:
  - CSS
  - Properties
uri: css/properties/shape-image-threshold

---
## Summary

Defines the alpha channel threshold used to extract a shape from an image. Can be thought of as a &quot;minimum opacity&quot; threshold; that is, a value of 0.5 means that the shape will enclose all the pixels that are more than 50% opaque.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `0.0`

Applies to
:   Floats

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As specified, clamped to a 0.0-1.0 range

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   [[CSS percentages::Alpha channel of the image specified by [shape-outside](/css/properties/shape-outside).]]

## Syntax

-   `shape-image-threshold: <number>`

## Values

\<number\>
:   A numeric value used to set the opacity threshold used for extracting a shape from an image. Any values outside the range 0.0 (fully transparent) to 1.0 (fully opaque) will be clamped to this range.

## Examples

Note: Depends upon an image previously specified by [shape-outside](/css/properties/shape-outside).

``` css
/*
Extract a shape from an image by enclosing all pixels greater than 25% opacity
*/
#myimg {
  shape-image-threshold: 0.25;
}
```

[View live example](http://code.webplatform.org/gist/5833790)

## Usage

     Currently implemented as an experimental feature in WebKit and Blink. This can be used with a -webkit- prefix in WebKit nightly builds and with a -webkit- prefix in Chrome Canary builds with experimental-webkit-features enabled: chrome://flags/#enable-experimental-webkit-features

## Related specifications

[CSS Shapes Module Level 1](http://www.w3.org/TR/css-shapes/)
:   W3C Candidate Recommendation

## See also

### Other articles

[shape-outside](/css/properties/shape-outside) [shape-margin](/css/properties/shape-margin)
