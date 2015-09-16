---
title: vertical-align
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/6960125'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`baseline`'
  'Applies to': 'inline-level and ‘table-cell’ elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': ''
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: 'refers to the ‘line-height’ of the element itself'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The vertical-align property controls how inline elements or text are vertically aligned compared to the baseline. If this property is used on table-cells it controls the vertical alignment of content of the table cell.'
tags:
  - CSS
  - Properties
uri: css/properties/vertical-align

---
## Summary

The vertical-align property controls how inline elements or text are vertically aligned compared to the baseline. If this property is used on table-cells it controls the vertical alignment of content of the table cell.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `baseline`

Applies to
:   inline-level and ‘table-cell’ elements

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

Percentages
:   refers to the ‘line-height’ of the element itself

## Syntax

-   `vertical-align: <length>`
-   `vertical-align: <percentage>`
-   `vertical-align: baseline`
-   `vertical-align: bottom`
-   `vertical-align: middle`
-   `vertical-align: sub`
-   `vertical-align: super`
-   `vertical-align: text-bottom`
-   `vertical-align: text-top`
-   `vertical-align: top`

## Values

baseline
:   Default. Vertically aligns the content with the baseline of its parent.

middle
:   Vertically aligns the content to the middle of its parent.

sub
:   Vertically aligns the content to subscript.

super
:   Vertically aligns the content to superscript.

text-top
:   Vertically aligns the content to the top of its parent.

text-bottom
:   Vertically aligns the content to the bottom of its parent.

\<percentage\>
:   Raises or lowers the content by a percentage of the line height. If this is set to a positive number the content is raised compared to the baseline of its parent. If this is set to a negative number the content is lowered compared to the baseline of its parent. If set to `0` it is equivalent to `baseline`.

\<length\>
:   Raises or lowers the content by the specified length. If this is set to a positive number the content is raised compared to the baseline of its parent. If this is set to a negative number the content is lowered compared to the baseline of its parent. If set to `0` it is equivalent to `baseline`.

top
:   Vertically aligns the content and its descendants to the top of the text line.

bottom
:   Vertically aligns the content and its descendants to the bottom of the text line.

## Examples

This example uses the `vertical-align` property to align text within a table cell.

``` html
<table>
  <tr>
    <td style='vertical-align: top;'>Top aligned</td>
    <td style='vertical-align: middle;'>Middle aligned</td>
    <td style='vertical-align: bottom;'>Bottom aligned</td>
  </tr>
</table>
```

[View live example](http://code.webplatform.org/gist/6960125)

## Related specifications

[CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/visudet.html#propdef-vertical-align)
:   Recommendation
