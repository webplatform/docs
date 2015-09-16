---
title: fill-opacity
notes:
  - "Complete values, add example and compatibility.\nThe SVG property pages will be linked to here."
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`1`'
  'Applies to': 'shapes and text content elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': ''
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: n/a
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: '‘fill-opacity’ specifies the opacity of the painting operation used to paint the interior the current object. (See Painting shapes and text.)'
tags:
  - CSS
  - Properties
uri: css/properties/fill-opacity

---
## Summary

‘fill-opacity’ specifies the opacity of the painting operation used to paint the interior the current object. (See Painting shapes and text.)

## Overview table

[Initial value](/css/concepts/initial_value)
:   `1`

Applies to
:   shapes and text content elements

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   n/a

## Syntax

-   `fill-opacity: inherit`

## Values

inherit
:

**Needs Examples**: This section should include examples.

## Usage

     <opacity-value>

The opacity of the painting operation used to fill the current object, as a \<number\>. Any values outside the range 0.0 (fully transparent) to 1.0 (fully opaque) will be clamped to this range. (See Clamping values which are restricted to a particular range.)

## Related specifications

[stroke-opacity](http://www.w3.org/TR/SVG/painting.html#StrokeOpacityProperty)
:   W3C Recommendation

[opacity](http://www.w3.org/TR/SVG/masking.html#OpacityProperty)
:   W3C Recommendation

## See also

### Other articles

<http://www.w3.org/TR/SVG/render.html#PaintingShapesAndText>
