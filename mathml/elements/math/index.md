---
title: 'math'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/MathML/Element/math)'
compatibility:
  feature: math
  topic: mathml
overview_table:
  '[DOM Interface](/dom/interface)': '[mathml](/mathml)'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The top-level element in MathML is &lt;math&gt;. Every valid MathML instance must be wrapped in &lt;math&gt; tags. In addition you must not nest a second &lt;math&gt; element in another, but you can have an arbitrary number of other child elements in it.'
tags:
  - Markup_Elements
  - MathML
uri: mathml/elements/math

---
## Summary

The top-level element in MathML is &lt;math&gt;. Every valid MathML instance must be wrapped in &lt;math&gt; tags. In addition you must not nest a second &lt;math&gt; element in another, but you can have an arbitrary number of other child elements in it.

## Overview Table

[DOM Interface](/dom/interface)
:   [mathml](/mathml)

## Examples

This example shows a simple formula written in MathML:

``` html


<!DOCTYPE html>
<html>
  <head>
    <title>MathML in HTML5</title>
  </head>
  <body>

  <math>
    <mrow>
      <mrow>
        <msup>
          <mi>a</mi>
          <mn>2</mn>
        </msup>
        <mo>+</mo>
        <msup>
          <mi>b</mi>
          <mn>2</mn>
        </msup>
      </mrow>
      <mo>=</mo>
      <msup>
        <mi>c</mi>
        <mn>2</mn>
      </msup>
    </mrow>
  </math>

  </body>
</html>
```

</pre>

## Related specifications

[MathML 3.0](http://www.w3.org/TR/MathML3/chapter2.html#interf.toplevel)
:   W3C Recommendation

## Attributes

In addition to the following attributes, the **math** element accepts any attributes of the [mstyle](/mathml/elements/mstyle) element.

display
:   This enumerated attribute specifies how the enclosed MathML markup should be rendered. It can have one of the following values:
    -   **block**, which means that this element will be displayed outside the current span of text, as a block that can be positioned anywhere without changing the meaning of the text;
    -   **inline**, which means that this element will be displayed inside the current span of text, and cannot be moved out of it without changing the meaning of that text.

 mode **(depreacted)**
:   Deprecated in favor of the display attribute.
     Possible values are: **display** (which has the same effect as display="block") and **inline**.
