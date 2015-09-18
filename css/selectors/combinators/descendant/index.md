---
title: 'descendant'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://code.webplatform.org/gist/8413346'
compatibility:
  feature: descendant
  topic: css
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Selects any instance of an element that is a descendant (child, grandchild and beyond) of another element.'
tags:
  - CSS_Selectors
  - CSS
uri: css/selectors/combinators/descendant

---
## Summary

Selects any instance of an element that is a descendant (child, grandchild and beyond) of another element.

 Use a descendant combinator to select every instance of an element under its ancestor. Create a descendant combinator by adding a whitespace between two simple selectors. For example `nav ul` will target every instance of an [unordered list](/html/elements/ul) found inside of a [navigation](/html/elements/nav) element.

For performance considerations, take care to not over-qualify selectors. For instance, html and body are unnecessary in the following example: `html body article a {}`. It's a given that an article will be found in the body which will be found in the html. There is no reason to require that the browser try to match any further than the article—as browsers read selectors from right to left.

## Examples

The following rule defines a text color of red for all instances of unordered lists within navigation elements.

``` css
nav ul { color:red; }
```

[View live example](http://code.webplatform.org/gist/8413346)

## Notes

Descendant combinators were called contextual selectors in Cascading Style Sheets, Level 1 (CSS1).

To skip over a generation of elements and pass styles to descendants beyond child elements, combine the Universal (\*) Selector with the Descendant Combinator. For example, the following selector matches any **p** elements that are not direct descendants (grandchildren or later) of a **div** element. `DIV * P {}`

### Syntax

`first second { ... }`

### Parameters

*first*
:   A CSS simple selector.
*second*
:   A CSS simple selector.

### Standards information

-   [CSS 2.1](http://go.microsoft.com/fwlink/p/?linkid=203757), Section 5.5

## Related specifications

[CSS Level 2 Specification](http://www.w3.org/TR/CSS2/)
:   W3C Recommendation
