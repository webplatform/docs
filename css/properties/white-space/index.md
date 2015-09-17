---
title: 'white-space'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/Web/CSS/white-space)'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/7284477'
compatibility:
  feature: white-space
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`normal`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`whiteSpace`'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The white-space property controls whether and how white space inside the element is collapsed, and whether lines may wrap at unforced &quot;soft wrap&quot; opportunities.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/white-space

---
## Summary

The white-space property controls whether and how white space inside the element is collapsed, and whether lines may wrap at unforced &quot;soft wrap&quot; opportunities.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `normal`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   as specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `whiteSpace`

## Syntax

-   `white-space: normal`
-   `white-space: nowrap`
-   `white-space: pre`
-   `white-space: pre-line`
-   `white-space: pre-wrap`

## Values

normal
:   This value prevents user agents from collapsing sequences of white space. Segment breaks such as line feeds and carriage returns are preserved as forced line breaks. Lines only break at forced line breaks; content that does not fit within the block container overflows it.

nowrap
:   Like `normal`, but content does not wrap to the next line.

pre
:   Line breaks and other whitespace are preserved.

pre-line
:   Like `normal`, this value collapses consecutive spaces and allows wrapping, but preserves segment breaks in the source as forced line breaks.

pre-wrap
:   Like `pre`, but allows wrapping (like `normal`'s wrapping).

## Examples

See the live example that has all the properties implemented side by side for comparison.

``` css
/**
 * white-space
 * CSS3 property
 * http://docs.webplatform.org/wiki/css/properties/white-space
 */

.white-space--nowrap {
  white-space:nowrap;
}

.white-space--normal {
  white-space:normal;
}

.white-space--pre {
  white-space:pre;
}

.white-space--pre-wrap {
  white-space:pre-wrap;
}

.white-space--pre-line {
  white-space:pre-wrap;
}

body {
  font-size: large;
  width: 500px;
}

p {
  background-color: #ddd;
}
```

[View live example](http://gist.github.com/7284477)

## Notes

Whitespace, such as line breaks, spaces, and tabs, is collapsed by default in HTML documents. You can use the nonbreaking space entity `(&nbsp;)` to add extra spaces to an object when the **white-space** property is set to **normal** or **nowrap**. You can add extra line breaks using the **br** element.

## Related specifications

[CSS Text Module Level 3](http://www.w3.org/TR/css3-text/#white-space-property)
:   Working Draft

## See also

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   style[style](/css/cssom/style)
-   `Reference`
-   `pre`
-   -ms-word-wrap[-ms-word-wrap](/css/properties/word-wrap)
-   `Other Resources`
-   `CSS Enhancements in Internet Explorer 6`
