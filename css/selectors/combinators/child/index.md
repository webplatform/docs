---
title: child
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/aa358819%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/8413346'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Selects only the immediate child of a parent element.'
tags:
  - CSS
  - Selectors
uri: css/selectors/combinators/child

---
## Summary

Selects only the immediate child of a parent element.

 Use a child combinator to select the direct children of a parent ancestor. Create a child combinator by placing a "greater-than sign" (\>) between two simple selectors. For example "ol \> li" will target every [list item](/html/elements/li) element that is a direct child of an [ordered list](/html/elements/ol) element. It will not match any further than the child in the document tree. For instance, if there were an [unordered list](/html/elements/ul) nested inside an [ordered list](/html/elements/ol) the [list items](/html/elements/li) in the unordered list would not be matched.

## Examples

The following rule defines the text color of list item elements which are direct children of an ordered list red.

``` css
ol li {color: red;}
```

[View live example](http://code.webplatform.org/gist/8413346)

## Notes

### Remarks

A child combinator is a "greater-than sign" (\>) character that separates two simple selectors. Whitespace is not significant. A selector of the form "E\>F" matches when element F is a direct descendant of element E. **Note**  Requires Windows Internet Explorer 7 or later. **Note**  Combinators are not supported in webpages that are displayed in the Microsoft Internet Explorer 5 document mode (also known as "Quirks" mode). To use attribute selectors, add a [!DOCTYPE](/html/elements/!DOCTYPE) directive that specifies a standards-based document. For more information, see [Defining Document Compatibility](http://go.microsoft.com/fwlink/p/?LinkID=125785).

### Syntax

`first>second { ... }`

### Parameters

*first*
:   A CSS simple selector.
*second*
:   A CSS simple selector.

### Standards information

-   [CSS 2.1](http://www.w3.org/TR/CSS21/selector.html#child-selectors), Section 5.6

## Related specifications

[CSS Level 2 Specification](http://www.w3.org/TR/CSS2/)
:   W3C Recommendation
