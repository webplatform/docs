---
title: angle
tags:
  - Data
  - Type
  - CSS
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The <angle> CSS data type describes an amount of rotation; it is expressed with a number followed (without whitespace) by one of the recognized angle unit abbreviations.'
uri: 'css/data types/angle'

---
# \<angle\>

## Summary

The \<angle\> CSS data type describes an amount of rotation; it is expressed with a number followed (without whitespace) by one of the recognized angle unit abbreviations.

 Four angle units are available:

-   **deg** are degrees, of which there are 360 in a full circle.
-   **grad** are grades, of which there are 400 in a full circle.
-   **rad** are radians, of which there are 2π in a full circle.
-   **turn** are turns, of which one comprises a full circle.

Measurements may be positive or negative, and may extend past the limit required to specify a full circle.

If using Javascript to set or manipulate styles requiring angle measurements, it is worth mentioning that the trigonometric [Math functions](/concepts/programming/javascript/core_objects#Math_Object) use radians for angles.

## Examples

``` {.css}
.a[href] {
    display: block;
    transition: transform 0.25s;
    transform: rotateX(0deg);
}
a:hover {
    /* spin link 3 times & return to original orientation */
    transform: rotateX(1080deg);
}
```

## Related specifications

Specification
:   Status
[CSS Values and Units Module Level 3](http://www.w3.org/TR/css3-values/)
:   Candidate Recommendation

