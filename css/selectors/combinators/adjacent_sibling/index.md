---
title: 'adjacent sibling'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/8928240'
compatibility:
  feature: 'adjacent sibling'
  topic: css
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'This is referred to as an adjacent selector. It will select only the element that is immediately preceded by the former element.'
tags:
  - CSS
  - Selectors
uri: 'css/selectors/combinators/adjacent sibling'

---
## Summary

This is referred to as an adjacent selector. It will select only the element that is immediately preceded by the former element.

 An adjacent sibling combinator selects an element that appears directly after a specified sibling element. It is created by placing a plus sign (+) between two simple selectors. For example [li](/html/elements/li) + [li](/html/elements/li) will select a [list item](/html/elements/li) directly following another, sibling [list item](/html/elements/li).

## Examples

``` css
li + li {
  border-left: 1px solid #333;
}
```

[View live example](http://code.webplatform.org/gist/8928240)

## Notes

### Remarks

The adjacent sibling combinator is a "plus sign" (+) character that separates two simple selectors. Whitespace is not significant. A selector of the form "E+F" matches element F when it immediately follows sibling element E in the document tree, ignoring non-element nodes (such as text nodes and comments). Element E and F must share the same parent and E must immediately precede F. To match the first child of the parent, use the :first-child pseudo-class. **Note**  Requires Windows Internet Explorer 7 or later. **Note**  Combinators are not supported in webpages that are displayed in the Microsoft Internet Explorer 5 document mode (also known as "Quirks" mode). To use attribute selectors, add a [!DOCTYPE](/html/elements/!DOCTYPE) directive that specifies a standards-based document. For more information, see [Defining Document Compatibility](http://go.microsoft.com/fwlink/p/?LinkID=125785).

### Syntax

`first+second { ... }`

### Parameters

*first*
:   A CSS simple selector.
*second*
:   A CSS simple selector.

### Standards information

-   [CSS 2.1](http://go.microsoft.com/fwlink/p/?linkid=203757), Section 5.7

## Related specifications

[CSS Level 2 Specification](http://www.w3.org/TR/CSS2/)
:   W3C Recommendation
