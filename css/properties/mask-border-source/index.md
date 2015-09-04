---
title: mask-border-source
tags:
  - CSS
  - Properties
readiness: 'In Progress'
standardization_status: 'W3C Last Call Working Draft'
notes:
  - "Add description and compatibility.\nAs of time of writing, this property is not yet implemented in most browsers."
summary: 'Specifies an image to be used as a mask. An image that is empty, fails to download, is non-existent, or cannot be displayed is ignored and does not mask the element.'
uri: css/properties/mask-border-source

---
# mask-border-source

## Summary

Specifies an image to be used as a mask. An image that is empty, fails to download, is non-existent, or cannot be displayed is ignored and does not mask the element.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `none`
Applies to
:   All elements. In SVG, it applies to container elements and graphics elements.
[Inherited](/css/concepts/inherited)
:   No
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   "none" or the image with its URI made absolute.
Animatable
:   No
[CSS Object Model Property](/css/concepts/cssom)
:   ``
Percentages
:   N/A

## Syntax

-   `mask-border-source: <image>`
-   `mask-border-source: none`

## Values

none
:   Counts as an image layer but does not mask the element.

\<image\>
:   A CSS image.

## Examples

``` {.css}
/* none */
p { mask-border-source: none; }

/* image */
div { mask-border-source: url(#someMask); }
```

## Related specifications

Specification
:   Status
[CSS Masking Level 1](http://www.w3.org/TR/css-masking-1/)
:   W3C Last Call Working Draft
[CSS Masking Level 1](http://dev.w3.org/fxtf/css-masking-1/)
:   W3C Editor’s Draft

