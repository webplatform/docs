---
title: mask-image
notes:
  - "Add description and compatibility.\nAs of time of writing, this property is not yet implemented in most browsers."
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'All elements. In SVG, it applies to container elements without the \<defs\> element and all graphics elements.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified, but with URIs made absolute.'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
summary: 'This property sets the mask image or the mask source of an element.'
tags:
  - CSS
  - Properties
uri: css/properties/mask-image

---
## <span>Summary</span>

This property sets the mask image or the mask source of an element.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `none`

Applies to
:   All elements. In SVG, it applies to container elements without the \<defs\> element and all graphics elements.

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As specified, but with URIs made absolute.

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   N/A

## <span>Syntax</span>

-   `mask-image: <child-selector>`
-   `mask-image: <image>`
-   `mask-image: <url>`
-   `mask-image: child`
-   `mask-image: none`

## <span>Values</span>

none
:   Counts as an image layer but does not mask the element.

\<image\>
:   A CSS image.

\<url\>
:   A URL reference to a \<mask\> element, e.g., `url(commonmasks.svg#mask)`, or to a CSS image.

child
:   A keyword indicating that the last direct child \<mask\> element of the element the mask-image property is applied to should be used as the mask source. It is equivalent to `select(mask:last-of-type)`.

\<child-selector\>
:   A functional notation accepting a comma-separated list of compound selectors that represents the first matching child \<mask\> element in DOM tree order.

## <span>Examples</span>

``` css
/* CSS gradient */
body { mask-image: linear-gradient(black 0%, transparent 100%) }

/* none */
p { mask-image: none }

/* URL */
div { mask-image: url(dot-mask.png) }
```

## <span>Related specifications</span>

[CSS Masking Level 1](https://dvcs.w3.org/hg/FXTF/raw-file/default/masking/index.html)
:   W3C Editor's Draft
