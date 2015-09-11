---
title: column-rule-color
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/6288958'
notes:
  - 'Add description, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`currentColor (same as for ‘color’ property)`'
  'Applies to': 'multi-column elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`columnRuleColor`'
  Percentages: N/A
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Specifies the color of the rule between columns.'
tags:
  - CSS
  - Properties
uri: css/properties/column-rule-color

---
## <span>Summary</span>

Specifies the color of the rule between columns.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `currentColor (same as for ‘color’ property)`

Applies to
:   multi-column elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   as specified

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `columnRuleColor`

Percentages
:   N/A

## <span>Syntax</span>

-   `column-rule-color: color`

## <span>Values</span>

color
:   One of the color names, RGB, RGBA, HSL, or HSLA values in the [Color Table](/css/color/color_table).

## <span>Examples</span>

Uses the column-rule-color property to set the color of the rule between columns.

``` css
/*
Makes 3 columns with 4px dashed green column-rule
*/

#columns {
  columns: 3;

  /* Prefix free example below, use vendor prefixes where needed */
  column-rule-style: dashed;
  column-rule-color: green;
  column-rule-width: 5px;
}
```

[View live example](http://code.webplatform.org/gist/6288958)

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

-   **column-rule-color**

-   [column-rule-style](/css/properties/column-rule-style)

-   [column-rule-width](/css/properties/column-rule-width)

-   [column-span](/css/properties/column-span)

-   [column-width](/css/properties/column-width)

-   [content](/css/properties/content)
