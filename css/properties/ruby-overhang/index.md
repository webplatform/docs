---
title: ruby-overhang
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rubyoverhang.htm'
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
  - CSS
  - Properties
uri: css/properties/ruby-overhang

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

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

-   `ruby-overhang: auto`
-   `ruby-overhang: none`
-   `ruby-overhang: whitespace`

## Values

auto
:   Default. Ruby text overhangs any other text adjacent to the base text.

whitespace
:   Ruby text overhangs only white-space characters.

none
:   Ruby text overhangs only text adjacent to its base.

## Examples

This example uses the **ruby-overhang** attribute and the **ruby-overhang** property to set the overhang of the ruby text. It uses an inline style sheet to set the **ruby-overhang** attribute to **none**.

``` html
<RUBY ID=oRuby STYLE = "ruby-overhang: none">
Ruby base.
<RT>Ruby text.
</RUBY>
<INPUT
TYPE=button VALUE="Whitespace"
onclick="oRuby.style.rubyOverhang='whitespace';"
>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rubyoverhang.htm)

## Notes

### Remarks

The **ruby-overhang** property specifies the overhang of the ruby text defined by the **rt** object, and is set on the **ruby** object.

### Syntax

`ruby-overhang: auto | whitespace | none`

### Standards information

-   [CSS3 Ruby Module](http://go.microsoft.com/fwlink/p/?linkid=203763), Section 4.3

## See also

### Related pages (MSDN)

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `runtimeStyle`
-   `style`
-   `Reference`
-   `ruby-align`
-   `ruby-position`
