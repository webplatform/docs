---
title: text-kashida-space
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, example, spec reference, standardization status'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`0%`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': ''
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'Not Ready'
tags:
  - CSS
  - Properties
uri: css/properties/text-kashida-space

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `0%`

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

## Syntax

-   `text-kashida-space: percentage`

## Values

percentage
:   An integer, followed by a %. The value is the ratio of kashida expansion to white space expansion. 100% specifies kashida expansion only, and 0% specifies white space expansion only

**Needs Examples**: This section should include examples.

## Notes

### Remarks

Windows Internet Explorer 8. The **-ms-text-kashida-space** attribute is an extension to CSS, and can be used as a synonym for **text-kashida-space** in IE8 Standards mode. Kashida is a typographic effect that justifies lines of text by elongating characters at carefully chosen points. It is used in Arabic writing systems. The property can be used with any justification style where kashida style expansion is used, such as the **auto**, **distribute**, **kashida**, and **newspaper** values of the [**-ms-text-justify**](/css/properties/text-justify) property. The property is read-only for the . The property applies to block elements only.

### Syntax

`-ms-text-kashida-space: percentage`

### Standards information

-   [CSS Text Level 3](http://go.microsoft.com/fwlink/p/?linkid=203766), Section 8.3

## See also

### Related pages (MSDN)

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `runtimeStyle`
-   `style`
