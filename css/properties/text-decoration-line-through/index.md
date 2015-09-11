---
title: text-decoration-line-through
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
uri: css/properties/text-decoration-line-through

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## <span>Overview table</span>

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

## <span>Syntax</span>

-   `text-decoration-line-through: VARIANT_FALSE`
-   `text-decoration-line-through: VARIANT_TRUE`

## <span>Values</span>

VARIANT\_TRUE
:   Apply the line-through.

VARIANT\_FALSE
:   Prevent the line-through.

## <span>Examples</span>

This example uses the **textDecorationLineThrough** property to draw a line through the text when the user clicks it with the mouse.

``` html
<P onclick="this.style.textDecorationLineThrough=true;">
Click this if you think it's unimportant.
</P>
```

### <span>Syntax</span>

`textDecorationLineThrough: VARIANT_TRUE | VARIANT_FALSE`

### <span>Requirements</span>

{

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `defaultSelected`
-   `runtimeStyle`
-   `style`
-   `textDecoration`
