---
title: transform-origin
tags:
  - CSS
  - Properties
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'This property defines the origin of the transformation axes relative to the element to which the transformation is applied.'
code_samples:
  - 'http://gist.github.com/6983020'
  - 'http://gist.github.com/6983052'
  - 'http://gist.github.com/6983069'
uri: css/properties/transform-origin

---
# transform-origin

## Summary

This property defines the origin of the transformation axes relative to the element to which the transformation is applied.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `50% 50%`
Applies to
:   Transformable elements.
[Inherited](/css/concepts/inherited)
:   No
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   For \<length\>, the absolute value; otherwise a percentage.
Animatable
:   Yes
[CSS Object Model Property](/css/concepts/cssom)
:   ``
Percentages
:   Refer to the size of the element's bounding box.

## Syntax

-   `transform-origin: <named-position>`
-   `transform-origin: length`
-   `transform-origin: percentage`

## Values

percentage
:   A number, followed by a %.

The value is a percentage of the bounding box width (for the X axis) or the bounding box height (for the Y axis, if specified). A percentage cannot be applied to the Z axis.

length
:   A floating-point number, followed by a unit of measurement.

Units of measurement may be absolute (`cm`, `mm`, `in`, `pt`, or `pc`) or relative (`em`, `ex`, or `px`).

\<named-position\>
:   A named position along the specified axis, each of which has a percentage equivalent.

The values `left`, `center`, and `right` are valid for the X axis and are equivalent to 0%, 50%, and 100% respectively. The values `top`, `center`, and `bottom` are valid for the Y axis and are equivalent to 0%, 50%, and 100% respectively. There are no named positions along the Z axis.

## Examples

``` {.css}
/* 25% X offset, 50% Y offset, 0 Z offset */
#mytranselem {
    transform-origin: 25% 50%;
}
```

[View live example](http://code.webplatform.org/gist/6983020)

``` {.css}
/* 20px Y offset, 25px X offset, 30px Z offset */
#mytranselem {
    transform-origin: 20px 25px 30px;
}
```

[View live example](http://code.webplatform.org/gist/6983052)

``` {.css}
/* right X offset, center Y offset, 0 Z offset */
#mytranselem {
    transform-origin: right;
}
```

[View live example](http://code.webplatform.org/gist/6983069)

## Notes

The origin may be moved along all three axes with this single property by specifying the relative position of each axis in X, Y, Z order. The grid complies with the right-hand rule for Cartesian coordinate systems. The x-axis increases from left to right; the y-axis increases from top to bottom; and the z-axis increases away from the user (higher z-values are more distant).

Microsoft deprecated `-ms-transform-origin`, the vendor-prefixed version of this property, with the release of Internet Explorer 10. It should only be included for compatibility with earlier versions.

If the `transform-origin` property is not set, the transform begins in the center at screen level (equal to a `transform-origin` value of `50% 50% 0`).

-   If fewer than three values are provided, the third value (z-axis) is assumed to be `0` (screen level).
-   If only one value is specified, the second value (y-axis) is assumed to be `50%`.

## Related specifications

Specification
:   Status
[CSS Transforms Module Level 3](http://www.w3.org/TR/css3-transforms)
:   W3C Working Draft

## See also

### Related pages (MSDN)

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `style`
-   `transform`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

