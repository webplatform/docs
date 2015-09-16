---
title: merror
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/MathML/Element/merror)'
overview_table:
  '[DOM Interface](/dom/interface)': '[mathml](/mathml)'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The MathML merror element is used to display contents as error messages. In Firefox this error message is rendered similar to the typical XML error message. Note that this error is not thrown when your MathML markup is wrong or not well-formed XML. You will still get an XML parsing error (in case of the XHTML notation of MathML), which has nothing to do with merror.'
tags:
  - Markup
  - Elements
  - MathML
uri: mathml/elements/merror

---
## Summary

The MathML merror element is used to display contents as error messages. In Firefox this error message is rendered similar to the typical XML error message. Note that this error is not thrown when your MathML markup is wrong or not well-formed XML. You will still get an XML parsing error (in case of the XHTML notation of MathML), which has nothing to do with merror.

## Overview Table

[DOM Interface](/dom/interface)
:   [mathml](/mathml)

## Examples

This example demostrates a simple usage of the merror element:

``` html


<math>

<merror>
  <mrow>
    <mtext> Division by zero: </mtext>
    <mfrac>
      <mn> 1 </mn>
      <mn> 0 </mn>
    </mfrac>
  </mrow>
</merror>

</math>
```

</pre>

## Related specifications

[MathML 3.0](http://www.w3.org/TR/MathML3/chapter3.html#presm.merror)
:   W3C Recommendation
