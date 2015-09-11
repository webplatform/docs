---
title: mask-size
notes:
  - "Add specification and compatibility.\nAs of time of writing, this property is not yet implemented in most browsers."
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'All elements. It applies to container elements without the \<defs\> and graphics elements in SVG.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified, but with lengths made absolute.'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: 'See text.'
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
summary: 'Specifies the size of the mask images, similar to the CSS background-size property.'
tags:
  - CSS
  - Properties
uri: css/properties/mask-size

---
## <span>Summary</span>

Specifies the size of the mask images, similar to the CSS background-size property.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `auto`

Applies to
:   All elements. It applies to container elements without the \<defs\> and graphics elements in SVG.

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As specified, but with lengths made absolute.

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   See text.

## <span>Syntax</span>

-   `mask-size: auto`
-   `mask-size: contain`
-   `mask-size: cover`
-   `mask-size: length`
-   `mask-size: percentage`

## <span>Values</span>

auto
:   The intrinsic height/width of the mask image is used.

contain
:   Scale the image, while preserving its intrinsic aspect ratio (if any), to the largest size such that both its width and height can fit inside the background positioning area.

cover
:   Scale the image, while preserving its intrinsic aspect ratio (if any), to the smallest size such that both its width and height can completely cover the background positioning area.

length
:   A floating-point number, followed by an absolute units designator (cm, mm, in, pt, or pc) or a relative units designator (em, ex, or px).

percentage
:   An integer, followed by a percent (%). A percentage value is relative to the background positioning area.

## <span>Examples</span>

``` css
/* contain */
body {
        background-color: white;
        mask-image: url(big-black-dot.jpg);
        mask-position: bottom right;
        mask-repeat: no-repeat;
        mask-size: contain;
    }
```

## <span>Related specifications</span>

[CSS Masking Level 1](https://dvcs.w3.org/hg/FXTF/raw-file/default/masking/index.html)
:   W3C Editor's Draft
