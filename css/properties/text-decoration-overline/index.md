---
title: text-decoration-overline
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
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
uri: css/properties/text-decoration-overline

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

-   `text-decoration-overline: VARIANT_FALSE`
-   `text-decoration-overline: VARIANT_TRUE`

## Values

VARIANT\_TRUE
:   A line is drawn over the text.

VARIANT\_FALSE
:   A line is not drawn over the text.

## Examples

This example uses the **textDecorationOverline** property to draw a line over the text when the user moves the mouse over the text.

``` html
<P onmouseover="this.style.textDecorationOverline=true;">
Mouse over this text for an overline.
</P>
```

### Syntax

`textDecorationOverline: VARIANT_TRUE | VARIANT_FALSE`

### Requirements

{

## See also

### Related pages

-   `defaultSelected`
-   `runtimeStyle`
-   `style`
-   `textDecoration`
