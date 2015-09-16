---
title: mpadded
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/MathML/Element/mpadded)'
overview_table:
  '[DOM Interface](/dom/interface)': '[mathml](/mathml)'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The MathML mpadded element is used to add extra padding and to set the general adjustment of position and size of enclosed contents.'
tags:
  - Markup
  - Elements
  - MathML
uri: mathml/elements/mpadded

---
## Summary

The MathML mpadded element is used to add extra padding and to set the general adjustment of position and size of enclosed contents.

## Overview Table

[DOM Interface](/dom/interface)
:   [mathml](/mathml)

## Examples

This example demonstrates a simple usage of the mpadded element:

``` html


<math>

  <mpadded height="+150px" width="100px" lspace="2height">
    <mi> x </mi>
    <mo> + </mo>
    <mi> y </mi>
  </mpadded>

</math>
```

</pre>

## Related specifications

[MathML 3.0](http://www.w3.org/TR/MathML3/chapter3.html#presm.mpadded)
:   W3C Recommendation

## Attributes

 depth
:   Sets or increments the depth. Possible values: Any length or an increment/decrement (a length prefixed with "+" or "-") .
 height
:   Sets or increments the height. Possible values: Any length or an increment/decrement (a length prefixed with "+" or "-") .
 lspace
:   Sets or increments the horizontal position. Possible values: Any length or an increment/decrement (a length prefixed with "+" or "-") .
 voffset
:   Sets or increments the vertical position. Possible values: Any length or an increment/decrement (a length prefixed with "+" or "-") .
 width
:   Sets or increments the width. Possible values: Any length or an increment/decrement (a length prefixed with "+" or "-") .

### Pseudo-units

It is possible to use the keywords `"depth`",` "height"`, and `"width"` as a pseudo-unit for the attributes `depth`, `height`, `lspace`, `voffset`, and `width`. They represent each length of the same-named dimension.
