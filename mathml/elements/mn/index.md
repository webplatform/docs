---
title: mn
tags:
  - Markup
  - Elements
  - MathML
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The MathML mn element represents a numeric literal which is normally a sequence of digits with a possible separator (a dot or a comma). However,  it is also allowed to have arbitrary text in it which is actually a numeric quantity, for example "eleven".'
uri: mathml/elements/mn

---
# mn

## Summary

The MathML mn element represents a numeric literal which is normally a sequence of digits with a possible separator (a dot or a comma). However, it is also allowed to have arbitrary text in it which is actually a numeric quantity, for example "eleven".

## Overview Table

[DOM Interface](/dom/interface)
:   [mathml](/mathml)

## Examples

This example demonstrates a simple usage of the mn element:

``` {.html}


<math>

  <mn> 0 </mn>

  <mn> 1.337 </mn>

  <mn> twelve </mn>

  <mn> XVI </mn>

  <mn> 2e10 </mn>

</math>
```

</pre>

## Related specifications

Specification
:   Status
[MathML 3.0](http://www.w3.org/TR/MathML3/chapter3.html#presm.mn)
:   W3C Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/MathML/Element/mn)

## Attributes

 mathsize
:   The size of the content. Possible values are:
    -   `small:` Font is rendered smaller than the current font size.
    -   `normal:` Equivalent to 100% or 1em.
    -   `big:` Font is rendered larger than the current font size.
    -   or a custom length.

 mathvariant
:   This logical class of the identifier, which varies in typography. That is, although the names suggest the typographic style for the class, semantically, items with the same class are treated "the same" within an expression, which might or might not involve displaying them with the named typography. The following values are allowed:
    -   `normal` (Default value for *more than one character*)
    -   `bold`
    -   `italic` (Default value for *a single character*)
    -   `bold-italic`
    -   `double-struck`
    -   `bold-fraktur`
    -   `script`
    -   `bold-script`
    -   `fraktur`
    -   `sans-serif`
    -   `bold-sans-serif`
    -   `sans-serif-italic`
    -   `sans-serif-bold-italic`
    -   `monospace`
    -   `initial`
    -   `tailed`
    -   `looped`
    -   `stretched`

