---
title: 'text-decoration-underline'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: text-decoration-underline
  topic: css
notes:
  - 'Needs summary, spec reference, standardization status, fix table coding in Notes, fix broken link'
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
uri: css/properties/text-decoration-underline

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

-   `text-decoration-underline: VARIANT_FALSE`
-   `text-decoration-underline: VARIANT_TRUE`

## Values

VARIANT\_TRUE
:   Apply the underline.

VARIANT\_FALSE
:   Prevent the underline.

## Examples

This example uses the **textDecorationUnderline** property to underline the text when the user clicks the text with the mouse.

``` html
<P onclick="this.style.textDecorationUnderline=true;">
Click this if you think it's important.
</P>
```

### Syntax

`textDecorationUnderline: VARIANT_TRUE | VARIANT_FALSE`

### Requirements

{

## See also

### Related pages

-   defaultSelected[defaultSelected](/dom/HTMLOptionElement/defaultSelected)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
-   textDecoration[textDecoration](/css/properties/text-decoration)
