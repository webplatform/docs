---
title: 'text-align-last'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://code.webplatform.org/gist/5664996'
compatibility:
  feature: text-align-last
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'block containers'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'specified value'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`textAlignLast`'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The text-align-last CSS property describes how the last line of a block element or a line before line break is aligned in its parent block element.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/text-align-last

---
## Summary

The text-align-last CSS property describes how the last line of a block element or a line before line break is aligned in its parent block element.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `auto`

Applies to
:   block containers

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   specified value

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `textAlignLast`

## Syntax

-   `text-align-last: auto`
-   `text-align-last: center`
-   `text-align-last: end`
-   `text-align-last: justify`
-   `text-align-last: left`
-   `text-align-last: right`
-   `text-align-last: start`

## Values

auto
:   Default. Text is aligned like the other lines in the object, using the value of the [**text-align**](/css/properties/text-align) property.

start
:   The same as `left` if direction is left-to-right and `right` if direction is right-to-left.

end
:   The same as `right` if direction is left-to-right and `left` if direction is right-to-left.

left
:   Text is aligned to the left.

right
:   Text is aligned to the right.

center
:   The text is centered within the line box.

justify
:   Text is justified if ‘text-justify’ is ‘distribute’, and the same as `start` value if otherwise.

## Examples

The following example shows an embedded style rule that justifies all the lines in the document's **p** elements. This is sometimes found in East Asian typography.

``` html
<p class="normal">Simple example with "auto" value of text-align-last property. This paragraph needs to be really long in order to show how to work with text-align-last property. It only works because we set a width for this paragraph though.</p>

<p class="justified">Simple example with "justify" value of text-align-last property. In this case, the last line is also justified. This paragraph needs to be really long in order to show how to work with text-align-last property.</p>
```

[View live example](http://code.webplatform.org/gist/5664996)

``` css
.normal {
    width: 300px;
    text-align: justify;
    text-align-last: auto;
}

.justified {
    width: 300px;
    text-align: justify;
    text-align-last: justify;
}
```

## Related specifications

[CSS Text Module Level 3](http://www.w3.org/TR/css3-text/#text-align-last)
:   W3C Working Draft

## See also

### Other articles

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
