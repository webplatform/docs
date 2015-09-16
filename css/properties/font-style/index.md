---
title: font-style
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/CSS/font-style)'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5628297'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`normal`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`fontStyle`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The font-style property allows normal, italic, or oblique faces to be selected. Italic forms are generally cursive in nature while oblique faces are typically sloped versions of the regular face. Oblique faces can be simulated by artificially sloping the glyphs of the regular face.'
tags:
  - CSS
  - Properties
uri: css/properties/font-style

---
## Summary

The font-style property allows normal, italic, or oblique faces to be selected. Italic forms are generally cursive in nature while oblique faces are typically sloped versions of the regular face. Oblique faces can be simulated by artificially sloping the glyphs of the regular face.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `normal`

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
:   `fontStyle`

Percentages
:   N/A

## Syntax

-   `font-style: italic`
-   `font-style: normal`
-   `font-style: oblique`

## Values

normal
:   Selects a face that is classified as a normal face (one that is neither italic or oblique).

italic
:   Selects a font that is labeled as 'italic' (cursive). If no font labeled 'italic' is available, a font that is labeled as 'oblique' is selected.

oblique
:   Selects a font that is labeled as 'oblique' (sloped version of the regular face). If no italic or oblique font is available, the browser slopes the normal version of the font to produce an oblique approximation.

## Examples

A selection of examples showing uses of the font-style property.

``` html
<p>Regular ol' P</p>
<p class="normal">Normal P, no different from the regular ol' P</p>
<p class="italic">Italic P, the cursive version of the font</p>
<p class="oblique">Oblique P, the sloped version of the font</p>
```

``` css
p { font-family: "Trebuchet MS", "Gill sans", serif; }
p.normal { font-style: normal; }
p.italic { font-style: italic; }
p.oblique { font-style: oblique; }
```

[View live example](http://code.webplatform.org/gist/5628297)

## Usage

     According to the specs, 'oblique' is a sloped version of the regular font. The example shows that browsers actually use the 'italic' version for the 'oblique' variant as well. In the example, the bottom of a regular 'f' aligns with the bottom of the surrounding text. In the oblique line this should be the case as well, but instead it shows a cursive 'f' that extends below the surrounding letters--proving that the browser is using the italic version instead of oblique.

![screenshot-font-style-example.png](/assets/public/e/ea/screenshot-font-style-example.png)

## Notes

If no italic or oblique face is available, oblique faces can be synthesized by rendering non-obliqued faces with an artificial obliquing operation. The use of these artificially obliqued faces can be disabled using the ‘font-synthesis’ property.

Authors should also be aware that synthesized approaches may not be suitable for scripts like Cyrillic, where italic forms are very different in shape. It is always better to use an actual italic font rather than rely on a synthetic version.

## Related specifications

[CSS Fonts Module Level 3](http://www.w3.org/TR/css3-fonts/#font-style-prop)
:   W3C Candidate Recommendation

## See also

### Related articles

#### CSS Font

-   [font-family](/css/properties/font-family)

-   [font-kerning](/css/properties/font-kerning)

-   [font-language-override](/css/properties/font-language-override)

-   [font-size](/css/properties/font-size)

-   [font-size-adjust](/css/properties/font-size-adjust)

-   **font-style**

-   [font-variant](/css/properties/font-variant)

-   [text-rendering](/css/properties/text-rendering)

-   [text-underline](/css/properties/text-underline)

-   [user-modify](/css/properties/user-modify)

#### Fonts

-   [@font-face](/css/atrules/@font-face)

-   [Font related properties](/css/fonts)

-   [font-variant](/css/fonts/font-variant)

-   [font](/css/properties/font)

-   [font-family](/css/properties/font-family)

-   [font-feature-settings](/css/properties/font-feature-settings)

-   [font-kerning](/css/properties/font-kerning)

-   [font-language-override](/css/properties/font-language-override)

-   [font-size](/css/properties/font-size)

-   [font-size-adjust](/css/properties/font-size-adjust)

-   [font-stretch](/css/properties/font-stretch)

-   **font-style**

-   [font-variant](/css/properties/font-variant)

-   [user-modify](/css/properties/user-modify)

-   [size](/html/attributes/size)

-   [font](/html/elements/font)

### Related pages

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `runtimeStyle`
-   `style`
-   `font`
