---
title: border-collapse
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/6948189'
notes:
  - 'Add examples'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`separate`'
  'Applies to': 'Table and inline-table elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': ''
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`borderCollapse`'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'Border-collapse can be used for collapsing the borders between table cells'
tags:
  - CSS
  - Properties
uri: css/properties/border-collapse

---
## <span>Summary</span>

Border-collapse can be used for collapsing the borders between table cells

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `separate`

Applies to
:   Table and inline-table elements

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `borderCollapse`

## <span>Syntax</span>

-   `border-collapse: collapse`
-   `border-collapse: inherit`
-   `border-collapse: separate`

## <span>Values</span>

separate
:   Default. Borders are detached (standard HTML). Each table cell has an individual border, with optional space between the borders.

collapse
:   Adjacent borders and the space between them are collapsed into a single border.

inherit
:   The same specified value as the property for the element's parent will be used.

## <span>Examples</span>

An example of border-collapse 'collapse' and 'seperate' table borders are red, cell borders are blue

``` css
/**
 * @author  Vivienne van Velzen
 * @see     http://code.webplatform.org/gist/6948189
 */

table {
    border-color: #F00;
    border-collapse: seperate; /* default */
}
td {
    border-color: #00F;
}
table.collapse {
    border-collapse: collapse;
}
p {
    margin: 15px 0 3px 0;
}
td p {
    margin: 3px;
}
```

[View live example](http://code.webplatform.org/gist/6948189)

## <span>Related specifications</span>

[CSS 2.1, section 17.6. Borders](http://www.w3.org/TR/CSS2/tables.html#propdef-border-collapse)
:   Recommendation

[CSS 3, section 8. Borders](http://dev.w3.org/csswg/css3-tables/#border-collapse)
:   Editor's Draft

## <span>See also</span>

### <span>Related articles</span>

#### <span>Tables</span>

-   **border-collapse**

-   [border-spacing](/css/properties/border-spacing)

-   [caption-side](/css/properties/caption-side)

-   [empty-cells](/css/properties/empty-cells)

-   [Tables](/css/tables)

-   [col](/html/elements/col)

-   [colgroup](/html/elements/colgroup)

-   [table](/html/elements/table)

-   [tbody](/html/elements/tbody)

-   [td](/html/elements/td)

-   [tfoot](/html/elements/tfoot)

-   [th](/html/elements/th)

### <span>Other articles</span>

-   [css/properties/border](/css/properties/border)
