---
title: position
tags:
  - Data
  - Type
  - CSS
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The <position> CSS data type represents information for positioning an element in horizontal and vertical directions using a mix of keywords, percentage, and length values.'
code_samples:
  - 'http://gist.github.com/10612218'
uri: 'css/data types/position'

---
# \<position\>

## Summary

The \<position\> CSS data type represents information for positioning an element in horizontal and vertical directions using a mix of keywords, percentage, and length values.

 The syntax for the `<position>` data type was initially developed specifically for the [`background-position`](/css/properties/background-position) property, but has since been adopted in other CSS standards, such as the [`radial-gradient()`](/css/functions/radial-gradient) function.

The position is specified using one or two tokens, either of which may be a keyword, length or percentage. The first token represents the *horizontal* position and the second represents the *vertical* position, *unless* both values are specified using keywords (in which case the order is irrelevant, since the keywords specify the dimension). If only one token is specified, the second token is treated as the keyword "center".

### Numerical position values

If positions are given using [`<length>`](/css/data_types/length) values, the length represents the distance from the top or left side of the positioning container (the element box or viewport) to the top or left side of the object being positioned.

If positions are given using [`<percentage>`](/css/data_types/percentage) values, the computed length is relative to the *difference* in length (height or width) between the object being positioned and the container it is positioned within. That means that:

-   a value of 0% means that the object is positioned flush against the left or top side of the container;
-   a value of 50% means that the object is centered within the container (in the horizontal or vertical direction as applicable);
-   a value of 100% means that the object is positioned flush against the right or bottom side of the container.

More generally, for an object of width *x1* and height *y1* positioned within a container of width *x2* and height *y2*, a position value of *h% v%* means that the top-left corner is positioned at *( (x2-x1)\*h%, (y2-y1)\*v%)*.

If the object being positioned is a single point (e.g., the center point of a radial gradient), it is treated as if has zero height and width and therefore the percentages are just simple percentages of the container's height and width.

### Keyword position values

The keyword values are:

-   **left**, equivalent to a horizontal position of 0%;
-   **right**, equivalent to a horizontal position of 100%;
-   **top**, equivalent to a vertical position of 0%;
-   **bottom**, equivalent to a vertical position of 100%;
-   **center**, equivalent to position of 50% in the applicable direction.

The applicable direction for the **center** keyword is horizontal if its the first token, vertical if it's the second, *unless* the other token is one of the left/right/top/bottom keywords.

Keywords may be combined with length and percentage values, but then the **horizontal vertical** order must be respected.

## Examples

``` {.css}
body{
    height:100%;
    background-color:#222;
    background-image:
       radial-gradient(circle at center, red, indigo 3em),
       radial-gradient(circle farthest-side at top right, yellow, green 90%, blue),
       radial-gradient(ellipse at left 70%, yellow, orange 30%);
    /* The center point is defined using the position syntax, after the "at" keyword.
    */
    background-size:15em 10em, 30% 70%, 100px 70px;
    background-position: center left,  center calc(100% - 1em), 100% 50%;
    /* Note that the position values are interpretted as horizontal first then vertical
       *unless* one of the values is given with the top/bottom or left/right keywords.
       Also note that percentages are interpretted as the percent of extra space,
       so that 50% is centered and 100% is aligned flush against the far edge.
    */
    background-repeat:no-repeat no-repeat, no-repeat no-repeat, no-repeat no-repeat;
}
```

[View live example](http://code.webplatform.org/gist/10612218)

## Related specifications

Specification
:   Status
[CSS Values and Units Module Level 3](http://www.w3.org/TR/css3-values/#position)
:   W3C Candidate Recommendation
[CSS 2.1](http://www.w3.org/TR/CSS21/colors.html#propdef-background-position)
:   W3C Recommendation

