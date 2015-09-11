---
title: mphantom
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/MathML/Element/mphantom)'
overview_table:
  '[DOM Interface](/dom/interface)': '[mathml](/mathml)'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The MathML mphantom element is rendered invisibly, but dimensions (such as height, width, and baseline position) are still kept.'
tags:
  - Markup
  - Elements
  - MathML
uri: mathml/elements/mphantom

---
## <span>Summary</span>

The MathML mphantom element is rendered invisibly, but dimensions (such as height, width, and baseline position) are still kept.

## <span>Overview Table</span>

[DOM Interface](/dom/interface)
:   [mathml](/mathml)

## <span>Examples</span>

This example demonstrates a simple usage of the mphantom element:

``` html


<math>
<mrow>
  <mi> x </mi>
  <mo> + </mo>
  <mphantom>
    <mi> y </mi>
    <mo> + </mo>
  </mphantom>
  <mi> z </mi>
</mrow>
</math>
```

</pre>

## <span>Related specifications</span>

[MathML 3.0](http://www.w3.org/TR/MathML3/chapter3.html#presm.mphantom)
:   W3C Recommendation
