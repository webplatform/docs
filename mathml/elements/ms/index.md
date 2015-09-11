---
title: ms
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/MathML/Element/ms)'
notes:
  - 'Fix broken link'
overview_table:
  '[DOM Interface](/dom/interface)': '[mathml](/mathml)'
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
summary: 'The MathML ms element represents a string literal meant to be interpreted by programming languages and computer algebra systems.'
tags:
  - Markup
  - Elements
  - MathML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - mathml/elements/malignmark
uri: mathml/elements/ms

---
## <span>Summary</span>

The MathML ms element represents a string literal meant to be interpreted by programming languages and computer algebra systems.

## <span>Overview Table</span>

[DOM Interface](/dom/interface)
:   [mathml](/mathml)

## <span>Examples</span>

This example demonstrates a simple usage of the ms element:

``` html


<math>

  <ms lquote="„" rquote="“"> abc </ms>

</math>
```

</pre>

## <span>Related specifications</span>

[MathML 3.0](http://www.w3.org/TR/MathML3/chapter3.html#presm.ms)
:   W3C Recommendation

By default, string literals are displayed as enclosed by double quotes ("); by using the lquote and rquote attributes, you can set custom characters to display. Note that quotation marks should not be specified unless they are part of the string literal. The content of an \<ms\> element is not an ASCII string per se, but rather a sequence of characters and [mglyph](/mathml/elements/mglyph) and [malignmark](/w/index.php?title=mathml/elements/malignmark&action=edit&redlink=1) elements.

## <span>Attributes</span>

 lquote
:   The opening quote character (depends on `dir`) to enclose the content. The default value is "`&quot;".`
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

 rquote
:   The closing quote mark (depends on `dir`) to enclose the content. The default value is "`&quot;".`
