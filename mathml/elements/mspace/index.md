---
title: mspace
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/MathML/Element/mspace)'
overview_table:
  '[DOM Interface](/dom/interface)': '[mathml](/mathml)'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The MathML mspace element is used to display a blank space, whose size is set by its attributes.'
tags:
  - Markup
  - Elements
  - MathML
uri: mathml/elements/mspace

---
## Summary

The MathML mspace element is used to display a blank space, whose size is set by its attributes.

## Overview Table

[DOM Interface](/dom/interface)
:   [mathml](/mathml)

## Examples

This example demonstrates a simple usage of the mspace element:

``` html


<math>

  <mspace depth="40px" height="20px" />

  <mspace width="100px" />

</math>
```

</pre>

## Related specifications

[MathML 3.0](http://www.w3.org/TR/MathML3/chapter3.html#presm.mspace)
:   W3C Recommendation

## Attributes

 depth
:   The desired depth (below the baseline) of the space (see length for values and units).
 height
:   The desired height (above the baseline) of the space (see length for values and units).
 linebreak
:   Indicates a line-break at the space. Possible values: `auto` (default value), `newline`, `nobreak`, `goodbreak`, `badbreak`.
     Starting with MathML 3, it is preferred to use [mo](/mathml/elements/mo) to control linebreaking.
 width
:   The desired width of the space (see length for values and units).
