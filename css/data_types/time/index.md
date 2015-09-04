---
title: time
tags:
  - Data
  - Type
  - CSS
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The <time> CSS data type specifies a duration in time, expressed as a number followed (without whitespace) by one of the time unit abbreviations: s or ms.'
uri: 'css/data types/time'

---
# \<time\>

## Summary

The \<time\> CSS data type specifies a duration in time, expressed as a number followed (without whitespace) by one of the time unit abbreviations: s or ms.

 In CSS3, time units must be either seconds (**s**) or milliseconds (**ms**); milliseconds are one-thousandth of a second. Time values can be used to measure the duration of animation effects, in which case the numeric value must be greater than or equal to zero.

## Examples

``` {.css}
.changeable {
    background-color: #fff;
    transition-property: background-color;
    /* transition takes half a second to complete */
    transition-duration: 0.5s;
}
.changeable:hover {
    background-color: #ff4;
    /* transition to yellow on mouseover */
}
```

## Related specifications

Specification
:   Status
[CSS Values and Units Module Level 3](http://www.w3.org/TR/css3-values/)
:   Candidate Recommendation

