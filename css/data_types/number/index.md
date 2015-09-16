---
title: <number>
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The &lt;number&gt; CSS data type represents positive or negative decimal or integer values.'
tags:
  - Data
  - Type
  - CSS
uri: 'css/data types/number'

---
## Summary

The &lt;number&gt; CSS data type represents positive or negative decimal or integer values.

 Numbers in the [CSS definition](http://www.w3.org/TR/css3-values/#numbers) can accept ordinary decimal numbers: a series of digits optionally followed by a decimal point (**.**) and more digits, with an optional exponent component (the latter is usually referred to as a scientific notation).

### Notes

-   Due to being a new feature of the CSS Syntax module, the browser support for scientific notations (the optional exponent component) varies and therefore, it should be used with caution. Supporting browsers include Internet Explorer 11, Firefox 29 and Chrome 39.
-   Before the CSS 3 Syntax module was introduced, numbers in CSS differed from the [SVG definition](http://www.w3.org/TR/SVG11/types.html#DataTypeNumber) which always allowed for numbers in attribute properties to be specified using scientific notation (such as **1.3e-5** for **0.000013**). If an SVG presentational attribute were specified using CSS styles, it must have conformed to the CSS data type.

## Examples

``` css
.box {
  /* Flip & enlarge */
  transform: scale(-1.2);
}
```

## Related specifications

[CSS Values and Units Module Level 3](http://www.w3.org/TR/css3-values/#numbers)
:   W3C Candidate Recommendation

[CSS 2.1](http://www.w3.org/TR/CSS21/syndata.html#numbers)
:   W3C Recommendation

[CSS Syntax Module Level 3](http://www.w3.org/TR/css-syntax-3/#number-token-diagram)
:   W3C Candidate Recommendation
