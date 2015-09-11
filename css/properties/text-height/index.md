---
title: text-height
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'Inline elements and parents of elements with display:ruby-text.'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified, except for initial and inherit'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'This property helps determine an inline box''s block-progression dimension, derived from the text-height and font-size properties for non-replaced elements, the height or the width for replaced elements, and the stacked block-progression dimension for inline-block elements. The block-progression dimension determines the position of the padding, border and margin for the element.'
tags:
  - CSS
  - Properties
uri: css/properties/text-height

---
## <span>Summary</span>

This property helps determine an inline box's block-progression dimension, derived from the text-height and font-size properties for non-replaced elements, the height or the width for replaced elements, and the stacked block-progression dimension for inline-block elements. The block-progression dimension determines the position of the padding, border and margin for the element.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `auto`

Applies to
:   Inline elements and parents of elements with display:ruby-text.

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As specified, except for initial and inherit

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   N/A

## <span>Syntax</span>

-   `text-height: <number>`
-   `text-height: auto`
-   `text-height: font-size`
-   `text-height: max-size`
-   `text-height: text-size`

## <span>Values</span>

auto
:   The block-progression dimension is based either on the em square determined by the computed element font-size property value, or the cell-height (ascender + descender) related to the computed element font-size as chosen by the user agent.

font-size
:   The block-progression dimension is based on the em square as determined by the computed element font-size.

text-size
:   The block-progression dimension is based on the cell-height (ascender + descender) related to the computed element font-size.

max-size
:   The block-progression dimension is based on the maximum extents toward the before-edge and after-edge of the box (obtained by considering all child elements located on the same line), ruby annotations (elements with "display:ruby-text"), and baseline shifted elements.

\<number\>
:   The block progression dimension is based on *number* times the em square as determined by the computed font-size.

## <span>Examples</span>

``` css
/* auto */
.inlinebox { text-height: auto; }

/* font-size */
.inlinebox { text-height: font-size; }

/* number */
.inlinebox { text-height: 3; }
```

## <span>Related specifications</span>

[CSS Line Layout Module](http://dev.w3.org/csswg/css-inline/)
:   W3C Editor's Draft
