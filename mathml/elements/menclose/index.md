---
title: menclose
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/MathML/Element/menlose)'
overview_table:
  '[DOM Interface](/dom/interface)': '[mathml](/mathml)'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The MathML menclose element renders its content inside an enclosing notation specified by the notation attribute.'
tags:
  - Markup
  - Elements
  - MathML
uri: mathml/elements/menclose

---
## <span>Summary</span>

The MathML menclose element renders its content inside an enclosing notation specified by the notation attribute.

## <span>Overview Table</span>

[DOM Interface](/dom/interface)
:   [mathml](/mathml)

## <span>Examples</span>

This example shows a simple markup using menclose:

``` html


<math>
  <menclose notation="circle box">
    <mi> x </mi>
    <mo> + </mo>
    <mi> y </mi>
  </menclose>
</math>
```

</pre>

## <span>Related specifications</span>

[MathML 3.0](http://www.w3.org/TR/MathML3/chapter3.html#presm.menclose)
:   W3C Recommendation

## <span>Attributes</span>

notation
:   Multiple values are possible:

    |Value|Description|
    |:----|:----------|
    |longdiv (default)|long division symbol|
    |actuarial|[actuarial symbol](http://en.wikipedia.org/wiki/Actuarial_notation)|
    |radical|square root symbol|
    |box|box|
    |roundedbox|rounded box|
    |circle|circle|
    |left|line to the left of the contents|
    |right|line to the right of the contents|
    |top|line above of the contents|
    |bottom|line below of the contents|
    |updiagonalstrike|strikeout line through contents from lower left to upper right|
    |downdiagonalstrike|strikeout line through contents from upper left to lower right|
    |verticalstrike|vertical strikeout line through contents|
    |horizontalstrike|horizontal strikeout line through contents|
    |madruwb|[Arabic factorial symbol](http://en.wikipedia.org/wiki/Modern_Arabic_mathematical_notation)|



