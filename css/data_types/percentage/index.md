---
title: '<percentage>'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The &lt;percentage&gt; CSS data type represents a number of measurement relative to another value.  It consists of a decimal or integer number immediately followed (without whitespace) by the percent sign, %.'
tags:
  - Data_Type
  - CSS
uri: 'css/data types/percentage'

---
## Summary

The &lt;percentage&gt; CSS data type represents a number of measurement relative to another value. It consists of a decimal or integer number immediately followed (without whitespace) by the percent sign, %.

 Percentages are expressed relative to other measurements, such as an element's dimensions, and can fall outside the 0-100% range. What percentages are relative to is different for every property and is specified in the “Percentages” row of its definition.

## Examples

``` css
.box {
    width: 80%;
          /* relative to the parent container's
              content width */

    border-radius: 50%;
          /* relative to this box's height or width;
              the computed value will be different
              in the x and y directions, creating an
              ellipse. */

    font-size: 120%;
          /* relative to the inherited font size */
}
```

## Related specifications

[CSS Values and Units Module Level 3](http://www.w3.org/TR/css3-values/#percentage-value)
:   W3C Candidate Recommendation

[CSS 2.1](http://www.w3.org/TR/CSS21/about.html#percentage-wrt)
:   W3C Recommendation
