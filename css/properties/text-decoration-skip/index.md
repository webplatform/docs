---
title: text-decoration-skip
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/gg721763(v=expression.40).aspx)'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`objects`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`textDecorationSkip`'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Specifies what parts of an element’s content are  skipped over when applying any text decoration.'
tags:
  - CSS
  - Properties
uri: css/properties/text-decoration-skip

---
## <span>Summary</span>

Specifies what parts of an element’s content are skipped over when applying any text decoration.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `objects`

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
:   `textDecorationSkip`

## <span>Syntax</span>

-   `text-decoration-skip: box-decoration`
-   `text-decoration-skip: edges`
-   `text-decoration-skip: ink`
-   `text-decoration-skip: none`
-   `text-decoration-skip: object`
-   `text-decoration-skip: spaces`

## <span>Values</span>

none
:   Will not skip anything; the text decoration will be drawn for all text content

object
:   Will skip the element (including it’s margin) if it’s atomic inline

spaces
:   Will skip white space, including:

-   regular spaces - U+0020
-   tabs - U+0009
-   nbsp - U+00A0
-   ideographic space - U+3000
-   all fixed width spaces - examples: U+2000 to U+200A, U+202F and U+205F
-   any adjacent letter-spacing or word-spacing

ink
:   Will skip over where any glyphs are drawn. It will interrupt the decoration line so that the text will show through where otherwise the decoration would cross through the text. This commonly includes ascenders and descenders of glyphs.

Note: The UA also may skip over small distances on the right or the left side of the glyph outline

box-decoration
:   Will skip over the box's margin, border, and padding areas.

Note: It is not known yet if this is a needed value

edges
:   The text decoration will be inset slightly, so that two side by side elements do not appear to have a single continuous decoration. This is important for Chinese content, where underlining is a form of punctuation.

## <span>Examples</span>

Skip ascenders and descenders, allowing text to show through any decoration.

``` css
p {
   text-decoration-skip: ink;
}
```

## <span>Notes</span>

This property inherits so the descendent elements can have different setting.

## <span>Related specifications</span>

[CSS Text Decoration Module Level 3](http://www.w3.org/TR/css-text-decor-3/)
:   Candidate Recommendation
