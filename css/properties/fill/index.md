---
title: fill
tags:
  - CSS
  - Properties
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
notes:
  - "Add example and compatibility.\nThe SVG property pages will be linked to here. Needs good examples."
summary: 'The ‘fill’ property paints the interior of the given graphical element. The area to be painted consists of any areas inside the outline of the shape. To determine the inside of the shape, all subpaths are considered, and the interior is determined according to the rules associated with the current value of the ‘fill-rule’ property. The zero-width geometric outline of a shape is included in the area to be painted.'
uri: css/properties/fill

---
# fill

## Summary

The ‘fill’ property paints the interior of the given graphical element. The area to be painted consists of any areas inside the outline of the shape. To determine the inside of the shape, all subpaths are considered, and the interior is determined according to the rules associated with the current value of the ‘fill-rule’ property. The zero-width geometric outline of a shape is included in the area to be painted.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `black`
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
:   ``
Percentages
:   n/a

## Syntax

-   `fill: <paint>`

## Values

\<paint\>
:   Properties ‘fill’ and ‘stroke’ take on a value of type \<paint\>

**Needs Examples**: This section should include examples.

## Usage

     The fill operation fills open subpaths by performing the fill operation as if an additional "closepath" command were added to the path to connect the last point of the subpath with the first point of the subpath. Thus, fill operations apply to both open subpaths within ‘path’ elements (i.e., subpaths without a closepath command) and ‘polyline’ elements.

## Related specifications

Specification
:   Status
[SVG](http://www.w3.org/TR/SVG/painting.html#FillProperties)
:   W3C Recommendation

