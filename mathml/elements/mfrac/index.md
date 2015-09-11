---
title: mfrac
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/MathML/Element/mfrac)'
overview_table:
  '[DOM Interface](/dom/interface)': '[mathml](/mathml)'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The MathML mfrac element is used to display fractions.'
tags:
  - Markup
  - Elements
  - MathML
uri: mathml/elements/mfrac

---
## <span>Summary</span>

The MathML mfrac element is used to display fractions.

## <span>Overview Table</span>

[DOM Interface](/dom/interface)
:   [mathml](/mathml)

## <span>Examples</span>

This example demonstrates a simple usage of the mfrac element:

``` html


<math>
  <mfrac bevelled="true">
     <mfrac>
        <mi> a </mi>
        <mi> b </mi>
     </mfrac>
     <mfrac>
        <mi> c </mi>
        <mi> d </mi>
     </mfrac>
  </mfrac>
</math>
```

</pre>

## <span>Related specifications</span>

[MathML 3.0](http://www.w3.org/TR/MathML3/chapter3.html#presm.mfrac)
:   W3C Recommendation

## <span>Attributes</span>

 bevelled
:   Specifies the way the fraction is displayed. If `true`, the fraction line is bevelled, which means that numerator and denominator are displayed side by side and separated by a slash (/). Otherwise, if set to `false` (which is the default value), numerator and denominator are on top of each other.
 denomalign
:   The alignment of the denominator under the fraction. Possible values are: `left`, `center` (default), and `right`.
 linethickness
:   The thickness of the horizontal fraction line. The default value is `medium`, but `thin`, `thick`, and other length values can be set.
 numalign
:   The alignment of the numerator over the fraction. Possible values are: `left`, `center` (default), and `right`.
