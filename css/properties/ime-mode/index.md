---
title: 'ime-mode'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: ime-mode
  topic: css
notes:
  - 'Add summery, specifications, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': ''
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': ''
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'In Progress'
tags:
  - CSS_Properties
  - CSS
  - Needs_Summary
uri: css/properties/ime-mode

---
## Overview table

[Initial value](/css/concepts/initial_value)
:

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

## Syntax

-   `ime-mode: active`
-   `ime-mode: auto`
-   `ime-mode: disabled`
-   `ime-mode: inactive`

## Values

auto
:   Default. IME is not affected. This is the same as not specifying the **-ms-ime-mode** attribute.

active
:   All characters are entered through the IME. Users can still deactivate the IME.

inactive
:   All characters are entered without IME. Users can still activate the IME.

disabled
:   IME is completely disabled. Users cannot activate the IME if the control has focus.

## Examples

This example uses the **-ms-ime-mode** attribute.

``` html
<INPUT TYPE = text STYLE = "ime-mode:active" >
```

## Notes

### Remarks

Windows Internet Explorer 8. The **-ms-ime-mode** attribute is an extension to CSS, and can be used as a synonym for **ime-mode** in IE8 Standards mode. An IME allows users to enter and edit Chinese, Japanese, and Korean characters. The IME is an essential component for writing Chinese, Japanese, and Korean scripts. These writing systems have more characters than can be encoded for a regular keyboard. The IMEs for these languages use sequences of base characters that describe an individual character or group of characters to enter a larger set of characters. Base characters can be component letters from Hangul syllables, phonetic components for Japanese Kanji characters, or various combinations for Chinese characters. To compose text with an IME, the user generally uses dictionary lookup and contextual analysis, especially in languages where homonyms are frequent, as in Japanese. A user typically starts by entering a few component characters, optionally selecting from various choices, and a confirmation command. Input Method Editors have two principle states:

-   Inactive mode. The keyboard acts like a regular keyboard and input is limited to a small set of characters.
-   Active mode. The IME accepts component characters or processing commands.

HTML authors can provide users with some control by specifying an IME mode for a specific text entry. For example, if Japanese users enter information in a registration form, they might be required to enter their names in Kanji and Roman characters. By default, the users would have to make sure that the IME is inactive when entering their names in the Latin alphabet. The user would activate the IME to enter Kanji letters, then deactivate the IME to complete the form in the Latin alphabet. By controlling the IME mode, the HTML author prevents the user from having to activate and deactivate the IME.

### Syntax

`-ms-ime-mode: auto | active | inactive | disabled`

## See also

### Related articles

#### Text

-   [block-progression](/css/properties/block-progression)

-   [font-language-override](/css/properties/font-language-override)

-   [font-size](/css/properties/font-size)

-   [hyphenate-limit-chars](/css/properties/hyphenate-limit-chars)

-   [hyphenate-limit-lines](/css/properties/hyphenate-limit-lines)

-   [hyphenate-limit-zone](/css/properties/hyphenate-limit-zone)

-   [hyphens](/css/properties/hyphens)

-   **ime-mode**

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
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
