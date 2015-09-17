---
title: 'column-rule'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/6288958'
compatibility:
  feature: column-rule
  topic: css
notes:
  - 'Add description, specifications, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`see individual properties`'
  'Applies to': 'multi-column elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': ''
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`columnRule`'
  Percentages: N/A
readiness: 'In Progress'
summary: 'Sets the width, style, and color of the rule between columns.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/column-rule

---
## Summary

Sets the width, style, and color of the rule between columns.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `see individual properties`

Applies to
:   multi-column elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `columnRule`

Percentages
:   N/A

## Syntax

-   `column-rule: column-rule-color`
-   `column-rule: column-rule-style`
-   `column-rule: column-rule-width`
-   `column-rule: transparent`

## Values

column-rule-width
:   Value of the [**column-rule-width**](/css/properties/column-rule-width) property.

column-rule-style
:   Value of the [**column-rule-style**](/css/properties/column-rule-style) property.

column-rule-color
:   Value of the [**column-rule-color**](/css/properties/column-rule-color) property.

transparent
:   Indicates rule is transparent.

## Examples

Makes 3 columns with 4px dashed green column-rule.

``` css
#columns {
  column-count: 3;
  column-rule: 4px dashed green;
}
```

[View live example](http://gist.github.com/6288958)

### Syntax

`column-rule: column-rule-width || column-rule-style || [ column-rule-color | transparent ]`

## See also

### Related articles

#### Multi-Column

-   [break-after](/css/properties/break-after)

-   [break-before](/css/properties/break-before)

-   [break-inside](/css/properties/break-inside)

-   [column-count](/css/properties/column-count)

-   [column-gap](/css/properties/column-gap)

-   **column-rule**

-   [column-rule-color](/css/properties/column-rule-color)

-   [column-rule-style](/css/properties/column-rule-style)

-   [column-rule-width](/css/properties/column-rule-width)

-   [column-span](/css/properties/column-span)

-   [column-width](/css/properties/column-width)

-   [content](/css/properties/content)

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   style[style](/css/cssom/style)
-   `address`
-   `blockQuote`
-   `div`
-   `dl`
-   `fieldSet`
-   `form`
-   `noFrames`
-   `noScript`
-   `ol`
-   `p`
-   `pre`
-   table[table](/html/elements/table)
-   `ul`
-   `dd`
-   `dt`
-   `li`
-   `tBody`
-   `td`
-   `tFoot`
-   `th`
-   `tHead`
-   `tr`
-   `button`
-   `del`
-   `ins`
-   `map`
-   `object`
-   `script`
