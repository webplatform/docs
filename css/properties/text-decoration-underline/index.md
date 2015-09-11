---
title: text-decoration-underline
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
uri: css/properties/text-decoration-underline

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

-   `text-decoration-underline: VARIANT_FALSE`
-   `text-decoration-underline: VARIANT_TRUE`

## <span>Values</span>

VARIANT\_TRUE
:   Apply the underline.

VARIANT\_FALSE
:   Prevent the underline.

## <span>Examples</span>

This example uses the **textDecorationUnderline** property to underline the text when the user clicks the text with the mouse.

``` html
<P onclick="this.style.textDecorationUnderline=true;">
Click this if you think it's important.
</P>
```

### <span>Syntax</span>

`textDecorationUnderline: VARIANT_TRUE | VARIANT_FALSE`

### <span>Requirements</span>

{

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `defaultSelected`
-   `runtimeStyle`
-   `style`
-   `textDecoration`
