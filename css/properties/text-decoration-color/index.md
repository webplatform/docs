---
title: text-decoration-color
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration-color)'
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/gg721748(v=expression.40).aspx)'
code_samples:
  - 'http://gist.github.com/7281842'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`currentColor`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'The computed color'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`textDecorationColor`'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Sets the color of any text decoration, such as underlines, overlines, and strike throughs.'
tags:
  - CSS
  - Properties
uri: css/properties/text-decoration-color

---
## <span>Summary</span>

Sets the color of any text decoration, such as underlines, overlines, and strike throughs.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `currentColor`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   The computed color

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `textDecorationColor`

## <span>Syntax</span>

-   `text-decoration-color: color`

## <span>Values</span>

color
:   The color data type value can be a named color keyword, or in hexadecimal, RGB, RGBa, HSL or HSLa notation. See the [CSS color values](/css/color) page for more details.

## <span>Examples</span>

Example using the text-decoration-color

``` css
.text-decoration-color {
  text-decoration: line-through;
  text-decoration-color: lime;
}

.text-decoration-color:hover {
  text-decoration: underline;
  text-decoration-color: #ff0;
}
```

[View live example](http://code.webplatform.org/gist/7281842)

## <span>Related specifications</span>

[CSS Text Decoration Module Level 3](http://www.w3.org/TR/css-text-decor-3/)
:   W3C Candidate Recommendation
