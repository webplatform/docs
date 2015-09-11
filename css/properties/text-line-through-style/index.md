---
title: text-line-through-style
notes:
  - 'Obsolete; deletion candidate'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'all elements with and generated content with textual content'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'specified value (except for initial and inherit)'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`N/A`'
  Percentages: N/A
readiness: 'Not Ready'
standardization_status: 'W3C Working Draft'
summary: "Specifies the line style for line-through text decoration.\n"
tags:
  - CSS
  - Properties
uri: css/properties/text-line-through-style

---
## <span>Summary</span>

Specifies the line style for line-through text decoration.

(Considered obsolete; use [text-decoration-style](/css/properties/text-decoration-style) instead.)

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `none`

Applies to
:   all elements with and generated content with textual content

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   specified value (except for initial and inherit)

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `N/A`

Percentages
:   N/A

## <span>Syntax</span>

-   `text-line-through-style: dashed`
-   `text-line-through-style: dot-dash`
-   `text-line-through-style: dot-dot-dash`
-   `text-line-through-style: dotted`
-   `text-line-through-style: double`
-   `text-line-through-style: none`
-   `text-line-through-style: solid`
-   `text-line-through-style: wave`

## <span>Values</span>

none
:   Produces no line

solid
:   Produces a solid line

double
:   Produces a double line.

dotted
:   Produces a dotted line

dashed
:   Produces a dashed line

dot-dash
:   Produces a line that repeats a pattern where a dot is followed by a dash.

dot-dot-dash
:   Produces a line that repeats a pattern where two dots are followed by a dash.

wave
:   Produces a wavy line.

## <span>Notes</span>

This property is obsolete and has been replaced by the [text-decoration-style](/css/properties/text-decoration-style) property.

Originally defined in an earlier draft of the [CSS3 Text Module specification](http://www.w3.org/TR/2003/CR-css3-text-20030514/), the functionality controlled by this property is now defined in the [CSS Text Decoration Level 3](http://www.w3.org/TR/css-text-decor-3) module. Sites (and apps) relying on the earlier behavior should be updated accordingly.

## <span>Related specifications</span>

[CSS3 Text Module](http://www.w3.org/TR/2003/CR-css3-text-20030514/)
:   Candidate Recommendation

[CSS Text Module Level 3](http://dev.w3.org/csswg/css-text/)
:   Editor's Draft
