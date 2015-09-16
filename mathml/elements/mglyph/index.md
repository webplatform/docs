---
title: 'mglyph'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/MathML/Element/mglyph)'
compatibility:
  feature: mglyph
  topic: mathml
overview_table:
  '[DOM Interface](/dom/interface)': '[mathml](/mathml)'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The MathML mglyph element is used to display non-standard symbols where existing Unicode characters are not available. It may be used within token elements.'
tags:
  - Markup
  - Elements
  - MathML
uri: mathml/elements/mglyph

---
## Summary

The MathML mglyph element is used to display non-standard symbols where existing Unicode characters are not available. It may be used within token elements.

## Overview Table

[DOM Interface](/dom/interface)
:   [mathml](/mathml)

## Examples

This example demonstrates a simple usage of the mglyph element:

``` html


<math>
  <mi><mglyph src="my-glyph.png" alt="my glyph"/></mi>
</math>
```

</pre>

## Related specifications

[MathML 3.0](http://www.w3.org/TR/MathML3/chapter3.html#presm.mglyph)
:   W3C Recommendation
