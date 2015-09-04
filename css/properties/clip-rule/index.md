---
title: clip-rule
tags:
  - CSS
  - Properties
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Clipping crops an graphic, so that only a portion of the graphic is rendered, or filled. This clip-rule property, when used with the clip-path property, defines which clip rule, or algorithm, to use when filling the different parts of a graphics.'
code_samples:
  - 'http://gist.github.com/7037715'
uri: css/properties/clip-rule
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - css/properties/clipPath

---
# clip-rule

## Summary

Clipping crops an graphic, so that only a portion of the graphic is rendered, or filled. This clip-rule property, when used with the clip-path property, defines which clip rule, or algorithm, to use when filling the different parts of a graphics.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `nonzero`
Applies to
:   Graphics elements that are contained within a \<clipPath\> element.
[Inherited](/css/concepts/inherited)
:   Yes
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   As specified
Animatable
:   No
[CSS Object Model Property](/css/concepts/cssom)
:   ``
Percentages
:   N/A

## Syntax

-   `clip-rule: evenodd`
-   `clip-rule: nonzero`

## Values

nonzero
:   This value defines whether a point is inside or outside the path by drawing a ray from that point to infinity in any direction and counting the places where a shape segment crosses the ray in a specific direction. When a segment crosses the ray from left to right, the count is incremented; when a segment crosses the ray from right to left, the count is decremented. If the count is zero, the point is outside; if non-zero, it is inside.

See [SVG fill-rule property](http://www.w3.org/TR/2011/REC-SVG11-20110816/painting.html#FillRuleProperty) for details.

evenodd
:   This value defines whether a point is inside or outside the path by drawing a ray from that point to infinity in any direction and counting the number of shape segments that the ray crosses. If the count is odd, the point is inside; if even, the point is outside.

See [SVG fill-rule property](http://www.w3.org/TR/2011/REC-SVG11-20110816/painting.html#FillRuleProperty) for details.

## Examples

This example uses the SVG `clip-rule` property to show the difference in values for overlapping circles. With `nonzero`, the default, the overlapping area is filled in. With `evenodd` the overlapping area is removed.

``` {.other}
<svg xmlns="http://www.w3.org/2000/svg"
     xmlns:xlink="http://www.w3.org/1999/xlink"
     width="100%" height="100%" viewBox="0 0 140 110">

  <title>'clip-rule' example</title>

  <style>
    .nonzero {
      clip-rule: nonzero;
    }

    .evenodd {
      clip-rule: evenodd;
    }
  </style>

  <defs>
    <path id="circles"
          d="M25,10 A20,20 0,1 0 25,50 A20,20 1,1 0 25,10 M45,10 A20,20 0,1 0 45,50 A20,20 1,1 0 45,10" />

    <clipPath id="clip-nonzero">
      <use class="nonzero"
           xlink:href="#circles" />
    </clipPath>

    <clipPath id="clip-evenodd">
      <use class="evenodd"
           xlink:href="#circles" y="50"/>
    </clipPath>
  </defs>

  <!-- non-zero clip-rule -->
  <rect clip-path="url(#clip-nonzero)"
        x="0" y="5" width="70" height="50"
        fill="cornflowerblue"/>

  <!-- equivalent non-zero fill-rule -->
  <use fill-rule="nonzero"
       xlink:href="#circles" x="70" y="0"
       stroke="cornflowerblue" />


  <!-- even-odd clip-rule -->
  <rect clip-path="url(#clip-evenodd)"
        x="0" y="55" width="70" height="50"
        fill="goldenrod"/>

  <!-- equivalent even-odd fill-rule -->
  <use fill-rule="evenodd"
       xlink:href="#circles" x="70" y="50"
       stroke="goldenrod" />
</svg>
```

[View live example](http://code.webplatform.org/gist/7037715)

## Usage

     The clip-rule property only applies to graphics elements that are contained within a clipPath element.

## Related specifications

Specification
:   Status
[CSS Masking](http://dev.w3.org/fxtf/masking/)
:   Editor's Draft
[SVG 1.1](http://www.w3.org/TR/SVG/)
:   Recommendation

