---
title: 'hyphens'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/CSS/hyphens)'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/6948199'
compatibility:
  feature: hyphens
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`manual`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'specified value'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Last Call Working Draft'
summary: 'Specifies whether or not words in a sentence can be split by the use of a manual or automatic hyphenation mechanism.'
tags:
  - CSS
  - Properties
uri: css/properties/hyphens

---
## Summary

Specifies whether or not words in a sentence can be split by the use of a manual or automatic hyphenation mechanism.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `manual`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   specified value

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   N/A

## Syntax

-   `hyphens: auto`
-   `hyphens: manual`
-   `hyphens: none`

## Values

none
:   Indicates that all word breaking is suppressed, even when explicitly specified with soft hyphens.

manual
:   Indicates that word breaking is allowed only where word breaking opportunities are suggested. These suggestions may come in the form of soft hyphens or hard hyphens. Soft hyphens (Unicode U+00AD, HTML `&shy;`) can be inserted on the desired place.

auto
:   Indicates that, in addition to suggested word breaking opportunities, word breaking opportunities are allowed where determined by a hyphenation resource (dictionary). Soft hyphens take priority over other hyphenation opportunities, but are still subject to the hyphenation controlled properties. By providing a language for the text (via the HTML `lang` attribute for example), a User Agent can determine the correct place to break a word.

## Examples

Sets the hyphens property different on each of the paragraph elements.

``` css
p:nth-child(1) {
  hyphens: none;
}

p:nth-child(2) {
  hyphens: manual;
}

p:nth-child(3) {
  hyphens: auto;
}
```

[View live example](http://code.webplatform.org/gist/6948199)

## Usage

     When hyphenation is not pre-set in a document, the default value for the hyphens property might not suit all cases. In cases where the language is properly set in the document, the hyphenation dictionaries provided in user agents can be able to break up words on the best possible place for each line.

The overall effect is that sentences run along almost the complete width of the box, and therefor can be slightly less high as end result.

## Notes

Note that not all languages are supported by browsers which support the value `auto` for this property.

### Syntax

`hyphens: none | manual | auto`

## Related specifications

[CSS Text Module Level 3](http://www.w3.org/TR/css3-text/#hyphens-property)
:   W3C Last Call Working Draft

## See also

### Related articles

#### Text

-   [block-progression](/css/properties/block-progression)

-   [font-language-override](/css/properties/font-language-override)

-   [font-size](/css/properties/font-size)

-   [hyphenate-limit-chars](/css/properties/hyphenate-limit-chars)

-   [hyphenate-limit-lines](/css/properties/hyphenate-limit-lines)

-   [hyphenate-limit-zone](/css/properties/hyphenate-limit-zone)

-   **hyphens**

-   [ime-mode](/css/properties/ime-mode)

-   [layout-grid](/css/properties/layout-grid)

-   [layout-grid-char](/css/properties/layout-grid-char)

-   [layout-grid-line](/css/properties/layout-grid-line)

-   [layout-grid-mode](/css/properties/layout-grid-mode)

-   [layout-grid-type](/css/properties/layout-grid-type)

-   [letter-spacing](/css/properties/letter-spacing)

-   [text-overflow-ellipsis](/css/properties/text-overflow-ellipsis)

-   [text-overflow-mode](/css/properties/text-overflow-mode)

-   [text-rendering](/css/properties/text-rendering)

-   [user-modify](/css/properties/user-modify)

-   [Text](/css/text)

-   [size](/html/attributes/size)

-   [b](/html/elements/b)

-   [b](/html/elements/b/ja)

-   [br](/html/elements/br)

-   [br](/html/elements/br/ja)

-   [caption](/html/elements/caption)

-   [cite](/html/elements/cite)

-   [code](/html/elements/code)

-   [del](/html/elements/del)

-   [dfn](/html/elements/dfn)

-   [em](/html/elements/em)

-   [font](/html/elements/font)

-   [hr](/html/elements/hr)

-   [i](/html/elements/i)

-   [ins](/html/elements/ins)

-   [kbd](/html/elements/kbd)

-   [mark](/html/elements/mark)

-   [samp](/html/elements/samp)

-   [strong](/html/elements/strong)

-   [Achieving typographic effects with the canvas tag](/tutorials/canvas_texteffects)

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
