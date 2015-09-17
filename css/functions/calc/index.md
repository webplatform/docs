---
title: 'calc'
code_samples:
  - 'http://gist.github.com/d3322a08edaaaef9adaf'
compatibility:
  feature: calc
  topic: css
notes:
  - 'Can be used as-is, though out of style with the rest of the function pages as it doesn''t list the others in related links.'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The calc() function can be used anywhere in a length is required by a CSS properties. calc() allows mathematical expressions with addition (‘+’), subtraction (‘-’), multiplication (‘*’), and division (‘/’) to be used as component values. The values themselves can be a mixture of percentages, integers, numbers, lengths such as em or cm, angles or even time values ( seconds, milliseconds). Calc is useful for computing certain values that are not known at the development time or to set formulated values rather that arbitrary ones.'
tags:
  - CSS_Functions
  - CSS
uri: css/functions/calc

---
## Summary

The calc() function can be used anywhere in a length is required by a CSS properties. calc() allows mathematical expressions with addition (‘+’), subtraction (‘-’), multiplication (‘\*’), and division (‘/’) to be used as component values. The values themselves can be a mixture of percentages, integers, numbers, lengths such as em or cm, angles or even time values ( seconds, milliseconds). Calc is useful for computing certain values that are not known at the development time or to set formulated values rather that arbitrary ones.

## Examples

This is an example of how can you use **calc** in CSS

``` css
/* CSS calc function example */

.header {
     position:relative;
     margin: 0px auto;
     width: 80%; /* fallback for browsers without support for calc() */
     width: calc(100% - 100px); /* CSS3 compliant implementation; Firefox 16 and IE 9, and above */
     border: solid black 1px;
     box-shadow: 5px 5px #999;
     margin-top: 40px;
     padding: 10px;
     text-align: center;
}

.header:hover {
     width: calc(100% / 3 - 2 * 1em); /* complex calculation on hover */
     width: 25%; /* fallback */
}
```

[View live example](http://gist.github.com/d3322a08edaaaef9adaf)

## Notes

If you divide by zero it will cause an error in the HTML parser. Also the return value that will be computed must comply within the range of the relevant CSS target. For example width or height cannot be negative so it will be reverted to 0;

## Related specifications

[W3C CSS Values and Units Module Level 3: Mathematical Expressions: "calc"](http://www.w3.org/TR/css3-values/#calc-notation)
:   Candidate Reccomendation
