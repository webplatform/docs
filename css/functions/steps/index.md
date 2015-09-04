---
title: steps
tags:
  - CSS
  - Functions
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'A timing function that specifies a progression of discrete intervals over the course of a transition or animation keyframe.'
uri: css/functions/steps

---
# steps

## Summary

A timing function that specifies a progression of discrete intervals over the course of a transition or animation keyframe.

 The function's mandatory first argument specifies the number of discrete, equal steps in the progression. An optional second argument accepts keywords **start** or **end** (the default), specifying whether the change should take place at the beginning or end of each new step.

## Examples

Apply an un-smoothed ratchet effect to any font-size transitions:

``` {.css}
p {
    transition: font-size 1s;
    transition-timing-function: steps(5);
}
```

## Related specifications

Specification
:   Status
[CSS Transitions](http://www.w3.org/TR/2013/WD-css3-transitions-20131119/)
:   Working Draft

