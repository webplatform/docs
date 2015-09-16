---
title: 'mfenced'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/MathML/Element/mfenced)'
compatibility:
  feature: mfenced
  topic: mathml
overview_table:
  '[DOM Interface](/dom/interface)': '[mathml](/mathml)'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The MathML mfenced element provides the possibility to add custom opening and closing parentheses (such as brackets) and separators (such as commas or semicolons) to an expression. '
tags:
  - Markup
  - Elements
  - MathML
uri: mathml/elements/mfenced

---
## Summary

The MathML mfenced element provides the possibility to add custom opening and closing parentheses (such as brackets) and separators (such as commas or semicolons) to an expression.

## Overview Table

[DOM Interface](/dom/interface)
:   [mathml](/mathml)

## Examples

These examples demonstrate a simple usage of the merror element:

``` html


<math>
  <mfenced open="{" close="}" separators=";;,">
    <mi>a</mi>
    <mi>b</mi>
    <mi>c</mi>
    <mi>d</mi>
    <mi>e</mi>
  </mfenced>
</math>

<math>
  <mfenced open="[" close="]" separators="||||,">
    <mi>a</mi>
    <mi>b</mi>
    <mi>c</mi>
    <mi>d</mi>
    <mi>e</mi>
  </mfenced>
</math>
```

</pre>

## Attributes

close
:   A string for the closing delimiter. The default value is ")" and any white space is trimmed.
 open
:   A string for the opening delimiter. The default value is `"("` and any white space is trimmed.
 separators
:   A sequence of zero or more characters to be used for different separators, optionally divided by white space, which is ignored. The default value is ",". By specifying more than one character, it is possible to set different separators for each argument in the expression. If there are too many separators, all excess is ignored. If there are too few separators in the expression, the last specified separator is repeated.

## Related specifications

[MathML 3.0](http://www.w3.org/TR/MathML3/chapter3.html#presm.mfenced)
:   W3C Recommendation
