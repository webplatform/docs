---
title: 'ruby-align'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rubyAlign.htm'
compatibility:
  feature: ruby-align
  topic: css
notes:
  - 'Needs summary, spec reference, standardization status'
overview_table:
  '[Initial value](/css/concepts/initial_value)': ''
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': ''
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'In Progress'
tags:
  - CSS_Properties
  - CSS
  - Needs_Summary
uri: css/properties/ruby-align

---
## Overview table

[Initial value](/css/concepts/initial_value)
:

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

## Syntax

-   `ruby-align: auto`
-   `ruby-align: center`
-   `ruby-align: distribute-letter`
-   `ruby-align: distribute-space`
-   `ruby-align: left`
-   `ruby-align: line-edge`
-   `ruby-align: right`

## Values

auto
:   Default. Browser determines how the ruby text is aligned. The recommended behavior for an ideographic (Asian character) ruby is to be aligned in the `distribute-space` mode. The recommended behavior for a Latin character ruby is to be aligned in the `center` mode.

left
:   Ruby text is left-aligned with the base.

center
:   Ruby text is centered within the width of the base. If the length of the base is smaller than the length of the ruby text, the base is centered within the width of the ruby text.

right
:   Ruby text is right-aligned with the base.

distribute-letter
:   Ruby text is evenly distributed across the width of the base if the width of the ruby text is smaller than the width of the base. If the width of the ruby text is at least the width of the base, the ruby text is center-aligned.

distribute-space
:   Ruby text is evenly distributed across the width of the base if the width of the ruby text is smaller than the width of the base. White space precedes the first and follows the last character in the ruby text, equal to half the kerning of the ruby text. If the width of the ruby text is at least the width of the base, the ruby text is centered.

line-edge
:   Ruby text is centered if it is not adjacent to a line edge. If it is adjacent to a line edge, the side of the ruby text lines up with the side of the base text.

## Examples

This example uses the **ruby-align** attribute and the **ruby-align** property to set the alignment of the ruby text. It uses an inline style sheet to set the **ruby-align** attribute to `right`.

``` html
<RUBY ID=oRuby STYLE = "ruby-align: right">
Ruby base.
<RT>Ruby text.
</RUBY>
<INPUT
TYPE=button VALUE="Center"
onclick="oRuby.style.rubyAlign='center';"
>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rubyAlign.htm)

## Notes

### Remarks

The **ruby-align** property specifies the alignment of the ruby text defined by the **rt** object, and is set on the **ruby** object.

### Syntax

`ruby-align: auto | left | center | right | distribute-letter | distribute-space | line-edge`

### Standards information

-   [CSS3 Ruby Module](http://go.microsoft.com/fwlink/p/?linkid=203763), Section 4.2

## See also

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
-   `Reference`
-   ruby-position[ruby-position](/css/properties/ruby-position)
-   ruby-overhang[ruby-overhang](/css/properties/ruby-overhang)
