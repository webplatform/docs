---
title: 'quotes'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5841933'
compatibility:
  feature: quotes
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`depends on user agent/element`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': ''
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Sets the type of quotation marks for embedded quotations.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/quotes

---
## Summary

Sets the type of quotation marks for embedded quotations.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `depends on user agent/element`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   N/A

## Syntax

-   `quotes: [<string>  <string>]+`
-   `quotes: none`

## Values

[\<string\> \<string\>]+
:   The "open-quote" and "close-quote" values are taken from the specified list of pairs of quotation marks. The first (leftmost) pair represents the outermost level of quotation, the second pair the first level of embedding, etc.

none
:   The "open-quote" and "close-quote" values produce no quotation marks.

## Examples

Here we demonstrate nested quotes. Notice the syntax used to declare the quotes. Any character can be used for a quote, but this example uses `'` and `"`. If we wanted to declare `quotes: "«" "»" "!" "@"`, that would work, too. You can also escape the characters (e.g. `quotes: "\""`), if that is your preference.

``` css
q { quotes: '"' '"' "'" "'" }
q:before { content: open-quote }
q:after  { content: close-quote }
```

[View live example](http://gist.github.com/5841933)

The HTML for the example above.

``` html
<p>
  <q>When I die, I'm donating my <q>body</q> to science fiction.</q>
  <em> ~ Stephen Wright</em>
</p>
```

## Notes

Pairs of strings are required if the value is not `none`.

## Related specifications

[CSS 2.1](http://www.w3.org/TR/CSS21/generate.html#quotes)
:   W3C Recommendation

## See also

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
