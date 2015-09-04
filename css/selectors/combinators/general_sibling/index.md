---
title: general sibling
tags:
  - CSS
  - Selectors
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'A general sibling combinator selects instances of an element appearing anywhere after another element within the same parent.'
code_samples:
  - 'http://gist.github.com/5143916'
uri: 'css/selectors/combinators/general sibling'

---
# general sibling

## Summary

A general sibling combinator selects instances of an element appearing anywhere after another element within the same parent.

 A general sibling combinator selects instances of an element appearing anywhere after another sibling element. It's created by placing a tilde (\~) between two simple selectors. For example `p ~ span` will select every [span](/html/elements/span) following a [paragraph](/html/elements/p) as long as they are found within the same parent element. Unlike the [adjacent sibling combinator](/css/selectors/combinators/adjacent_sibling), the selected element can appear anywhere after the first element as long as they share the same parent element.

## Examples

``` {.css}
p ~ span {
    color: red;
}
```

[View live example](http://code.webplatform.org/gist/5143916)

## Notes

### Remarks

The general sibling combinator is a "tilde" (\~) character that separates two simple selectors. Whitespace is not significant. A selector of the form "E\~F" matches element F when it follows sibling element E in the document tree, ignoring non-element nodes (such as text nodes and comments). Element E and F must share the same parent but E does not necessarily precede F directly. To match the first child of the parent, use the [**:first-child**](/css/selectors/pseudo-classes/:first-child) pseudo-class. **Note**  Requires Windows Internet Explorer 7 or later. **Note**  Combinators are not supported in webpages that are displayed in the Microsoft Internet Explorer 5 document mode (also known as "Quirks" mode). To use attribute selectors, add a [!DOCTYPE](/html/elements/!DOCTYPE) directive that specifies a standards-based document. For more information, see [Defining Document Compatibility](http://go.microsoft.com/fwlink/p/?LinkID=125785).

### Syntax

`first~second { ... }`

### Parameters

*first*
:   A CSS simple selector.
*second*
:   A CSS simple selector.

### Standards information

-   [Selectors Level 3](http://go.microsoft.com/fwlink/p/?linkid=199783), Section 6.3

## Related specifications

Specification
:   Status
[CSS Selectors Level 3](http://www.w3.org/TR/css3-selectors/)
:   W3C Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/CSS/General_sibling_selectors)

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

