---
title: column-span
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/CSS/column-span)'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5306158'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'block-level elements, except floating and absolutely positioned elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`columnSpan`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The column-span CSS property makes it possible for an element to span across all columns when its value is set to all. An element that spans more than one column is called a spanning element.'
tags:
  - CSS
  - Properties
uri: css/properties/column-span

---
## <span>Summary</span>

The column-span CSS property makes it possible for an element to span across all columns when its value is set to all. An element that spans more than one column is called a spanning element.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `none`

Applies to
:   block-level elements, except floating and absolutely positioned elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   as specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `columnSpan`

Percentages
:   N/A

## <span>Syntax</span>

-   `column-span: all`
-   `column-span: none`

## <span>Values</span>

none
:   Default. The content block does not span multiple columns.

all
:   The content block spans all columns on a page. All content that is declared before the content block is shown before the content block.

## <span>Examples</span>

Makes 4 columns and creates a span that crosses through columns

``` css
/*
Makes 4 columns and creates a span that crosses through columns
*/

#column {
  /* Prefix free example below, use vendor prefixes where needed */
  column-count: 4;
  column-gap: 2em;
  padding: 5px;
}

.span-content {
  column-span: all;
}
```

[View live example](http://code.webplatform.org/gist/5306158)

## <span>Notes</span>

An element that spans more than one column is called a spanning element.

## <span>Related specifications</span>

[CSS Multi-column Layout Module](http://www.w3.org/TR/css3-multicol/)
:   W3C Candidate Recommendation

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

-   **column-span**

-   [column-width](/css/properties/column-width)

-   [content](/css/properties/content)
