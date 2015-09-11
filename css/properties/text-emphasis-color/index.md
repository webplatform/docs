---
title: text-emphasis-color
code_samples:
  - 'http://gist.github.com/5654528'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`currentColor`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`textEmphasisColor`'
  Percentages: 'Not available'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The text-emphasis-color property specifies the foreground color of the emphasis marks.'
tags:
  - CSS
  - Properties
uri: css/properties/text-emphasis-color

---
## <span>Summary</span>

The text-emphasis-color property specifies the foreground color of the emphasis marks.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `currentColor`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   as specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `textEmphasisColor`

Percentages
:   Not available

## <span>Syntax</span>

-   `text-emphasis-color: color`

## <span>Values</span>

color
:   Specify the foreground color of the emphasis marks.

## <span>Examples</span>

``` css
p {
    text-emphasis-color: #000;
    text-emphasis-style: open;
}
```

[View live example](http://code.webplatform.org/gist/5654528)

## <span>Notes</span>

The initial value of the currentColor means that it defaults to match the text color.

## <span>Related specifications</span>

[CSS Text Decoration Module Level 3](http://dev.w3.org/csswg/css-text-decor-3/#emphasis-marks)
:   Editor's Draft
