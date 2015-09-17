---
title: 'maction'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/MathML/Element/maction)'
compatibility:
  feature: maction
  topic: mathml
overview_table:
  '[DOM Interface](/dom/interface)': '[mathml](/mathml)'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: "The MathML maction element provides a possibility to bind actions to (sub-) expressions.\nThe action itself is specified by the actiontype attribute, which accepts several values. To specify which child elements are addressed by the action, you can make use of the selection attribute.\n"
tags:
  - Markup_Elements
  - MathML
uri: mathml/elements/maction

---
## Summary

The MathML maction element provides a possibility to bind actions to (sub-) expressions. The action itself is specified by the actiontype attribute, which accepts several values. To specify which child elements are addressed by the action, you can make use of the selection attribute.

## Overview Table

[DOM Interface](/dom/interface)
:   [mathml](/mathml)

## Examples

This example demonstrates a simple usage of maction:

``` html


<math>

<maction actiontype="toggle">

  <mfrac>
    <mn>6</mn>
    <mn>8</mn>
  </mfrac>

  <mfrac>
    <mrow>
      <mn>3</mn>
      <mo>⋅</mo>
      <mn>2</mn>
    </mrow>
    <mrow>
      <mn>4</mn>
      <mo>⋅</mo>
      <mn>2</mn>
    </mrow>
  </mfrac>

  <mfrac>
    <mn>3</mn>
    <mn>4</mn>
  </mfrac>

</maction>

</math>
```

</pre>

## Related specifications

[MathML 3.0](http://www.w3.org/TR/MathML3/chapter2.html#interf.toplevel)
:   W3C Recommendation

## Attributes

 actiontype
:   The action which specifies what happens for this element. Possible values are:
    -   **statusline**: If there is a click on the *expression* or the reader moves the pointer over it, the *message* is sent to the browser's status line. The syntax is: \<maction actiontype="statusline"\> *expression* *message* \</maction\>.

    -   **toggle**: When there is a click on the subexpression, the rendering alternates the display of selected subexpressions. Therefore each click increments the **selection** value.

    The syntax is: \<maction actiontype="toggle" selection="*positive-integer*" \> *expression1 expression2 expressionN* \</maction\>.
    -   **tooltip**: When the pointer moves over the *expression*, a tooltip box with a *message* is displayed near the expression.

    The syntax is: \<maction actiontype="tooltip"\> *expression* *message* \</maction\>.
 selection
:   The child element which is addressed by the action. The default value is *1* which is the first child element.
