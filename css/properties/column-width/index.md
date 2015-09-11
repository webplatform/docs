---
title: column-width
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5305475'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'non-replaced block-level elements (except table elements), table cells, and inline-block elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'the absolute length, zero or larger'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`columnWidth`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Specifies the width of columns in multi-column elements.'
tags:
  - CSS
  - Properties
uri: css/properties/column-width

---
## <span>Summary</span>

Specifies the width of columns in multi-column elements.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `auto`

Applies to
:   non-replaced block-level elements (except table elements), table cells, and inline-block elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   the absolute length, zero or larger

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `columnWidth`

Percentages
:   N/A

## <span>Syntax</span>

-   `column-width: auto`
-   `column-width: length`

## <span>Values</span>

length
:   A floating-point number, followed by either an absolute units designator

(`cm`, `mm`, `in`, `pt`, or `pc`) or a relative units designator (`rem`, `em`, `ex`, or `px`), that indicates the optimal width. For more information about the supported length units, see CSS Length Units Reference.

auto
:   Default. The optimal column width is determined through other property values of the multi-column element, such as [**columnCount**](/css/properties/column-count).

## <span>Examples</span>

Makes as many columns that are 100px as there is space in the browser.

``` css
/*
Makes as many columns that are 100px as there is space in the browser.
*/

#column {
  /* Prefix free example below, use vendor prefixes where needed */
  column-width: 100px;
}
```

[View live example](http://code.webplatform.org/gist/5305475)

## <span>Notes</span>

### <span>Remarks</span>

The actual column width may vary from the value specified due to available space. To ensure that the exact value specified for this property is used, all property values of the multi-column element that pertain to length (such as width, column-width, column-gap, and column-rule-width) must be specified.

## <span>Related specifications</span>

[CSS Multi-column Layout Module](http://www.w3.org/TR/css3-multicol/)
:   Candidate Recommendation

## <span>See also</span>

### <span>Related articles</span>

#### <span>Multi-Column</span>

-   [break-after](/css/properties/break-after)

-   [break-before](/css/properties/break-before)

-   [break-inside](/css/properties/break-inside)

-   [column-count](/css/properties/column-count)

-   [column-gap](/css/properties/column-gap)

-   [column-rule](/css/properties/column-rule)

-   [column-rule-color](/css/properties/column-rule-color)

-   [column-rule-style](/css/properties/column-rule-style)

-   [column-rule-width](/css/properties/column-rule-width)

-   [column-span](/css/properties/column-span)

-   **column-width**

-   [content](/css/properties/content)
