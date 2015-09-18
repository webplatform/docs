---
title: 'text-align'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/CSS/text-align)'
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ms531162(v=vs.85).aspx)'
code_samples:
  - 'http://code.webplatform.org/gist/5664679'
compatibility:
  feature: text-align
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`start, or a nameless value that acts as left if direction is ltr, right if direction is rtl, if start is not supported by the browser.`'
  'Applies to': 'block containers'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified, except for the match-parent value which is calculated against its parent''s direction value and results in a computed value of either left or right'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`textAlign`'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The text-align CSS property describes how inline content like text is aligned in its parent block element. text-align does not control the alignment of block elements itself, only their inline content.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/text-align

---
## Summary

The text-align CSS property describes how inline content like text is aligned in its parent block element. text-align does not control the alignment of block elements itself, only their inline content.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `start, or a nameless value that acts as left if direction is ltr, right if direction is rtl, if start is not supported by the browser.`

Applies to
:   block containers

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   as specified, except for the match-parent value which is calculated against its parent's direction value and results in a computed value of either left or right

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `textAlign`

## Syntax

-   `text-align: <string>`
-   `text-align: center`
-   `text-align: end`
-   `text-align: justify`
-   `text-align: left`
-   `text-align: match-parent`
-   `text-align: right`
-   `text-align: start`
-   `text-align: start end`

## Values

start
:   The same as *`left`* if direction is left-to-right and *`right`* if direction is right-to-left.

end
:   The same as *`right`* if direction is left-to-right and *`left`* if direction is right-to-left.

left
:   The inline contents are aligned to the left edge of the line box.

right
:   The inline contents are aligned to the right edge of the line box.

center
:   The inline contents are centered within the line box.

\<string\>
:   The first occurrence of the one-char string is the element used for alignment. the keyword that follows or precedes it indicates how it is aligned. This allows to align numeric values on the decimal point, for instance.

justify
:   The text is justified. Text should line up their left and right edges to the left and right content edges of the paragraph.

match-parent
:   Similar to inherit with the difference that the value *`start`* and *`end`* are calculated according the parent's direction and are replaced by the adequate *`left`* or *`right`* value.

start end
:   Specifies *`start`* alignment of the first line and any line immediately after a forced line break; and *`end`* alignment of any remaining lines not affected by [**text-align-last**](/css/properties/text-align-last).

## Examples

This just shows the four possible types of text-alignment.

``` html
<p class="left"> This paragraph is aligned to the left. </p>

<p class="centered"> This paragraph is centered. </p>

<p class="right"> This paragraph is aligned to the right. </p>

<p class="justified">This paragraph needs to be really long in order to show how to justify text. It only works because we set a width for this paragraph though.</p>
```

[View live example](http://code.webplatform.org/gist/5664679)

``` css
.left { text-align: left;}
.cenetered{ text-align: center;}
.right { text-align: right;}
.justified { width: 200px; text-align: justify;}
```

## Notes

The standard-compatible way to center a block itself without centering its inline content is setting the left and right `margin` to auto, e.g.: `margin:auto;` or `margin:0 auto;` or `margin-left:auto; margin-right:auto;`

## Related specifications

[CSS Text Level 3](http://dev.w3.org/csswg/css3-text/#text-align)
:   Working Draft

## See also

### Other articles

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
