---
title: 'fill-rule'
code_samples:
  - 'http://www.w3.org/TR/SVG/images/painting/fillrule-nonzero.svg'
  - 'http://www.w3.org/TR/SVG/images/painting/fillrule-evenodd.svg'
compatibility:
  feature: fill-rule
  topic: css
notes:
  - "Complete values, add compatibility.\nThe SVG property pages will be linked to here."
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`nonzero`'
  'Applies to': 'shapes and text content elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': ''
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: n/a
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: "The ‘fill-rule’ property indicates the algorithm which is to be used to determine what parts of the canvas are included inside the shape. For a simple, non-intersecting path, it is intuitively clear what region lies &quot;inside&quot;; however, for a more complex path, such as a path that intersects itself or where one subpath encloses another, the interpretation of &quot;inside&quot; is not so obvious.\n"
tags:
  - CSS_Properties
uri: css/properties/fill-rule

---
## Summary

The ‘fill-rule’ property indicates the algorithm which is to be used to determine what parts of the canvas are included inside the shape. For a simple, non-intersecting path, it is intuitively clear what region lies &quot;inside&quot;; however, for a more complex path, such as a path that intersects itself or where one subpath encloses another, the interpretation of &quot;inside&quot; is not so obvious.

The ‘fill-rule’ property provides two options for how the inside of a shape is determined:

## Overview table

[Initial value](/css/concepts/initial_value)
:   `nonzero`

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

-   `fill-rule: evenodd`
-   `fill-rule: inherit`

## Values

evenodd
:

inherit
:

## Examples

nonzero

This rule determines the "insideness" of a point on the canvas by drawing a ray from that point to infinity in any direction and then examining the places where a segment of the shape crosses the ray. Starting with a count of zero, add one each time a path segment crosses the ray from left to right and subtract one each time a path segment crosses the ray from right to left. After counting the crossings, if the result is zero then the point is outside the path. Otherwise, it is inside.

``` css
The following drawing illustrates the nonzero rule:
```

[View live example](http://www.w3.org/TR/SVG/images/painting/fillrule-nonzero.svg)

evenodd

This rule determines the "insideness" of a point on the canvas by drawing a ray from that point to infinity in any direction and counting the number of path segments from the given shape that the ray crosses. If this number is odd, the point is inside; if even, the point is outside.

``` css
The following drawing illustrates the evenodd rule:
```

[View live example](http://www.w3.org/TR/SVG/images/painting/fillrule-evenodd.svg)

## Usage

     The ‘fill-rule’ property indicates the algorithm which is to be used to determine what parts of the canvas are included inside the shape. For a simple, non-intersecting path, it is intuitively clear what region lies "inside"; however, for a more complex path, such as a path that intersects itself or where one subpath encloses another, the interpretation of "inside" is not so obvious.

## Notes

(Note: the above explanations do not specify what to do if a path segment coincides with or is tangent to the ray. Since any ray will do, one may simply choose a different ray that does not have such problem intersections.)

## Related specifications

[SVG](http://www.w3.org/TR/SVG/painting.html#FillProperties)
:   W3C Recommendation

