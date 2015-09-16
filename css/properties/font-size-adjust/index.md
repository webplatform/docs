---
title: 'font-size-adjust'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: font-size-adjust
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`fontSizeAdjust`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The font-size-adjust property adjusts the font-size of the fallback fonts defined with font-family, so that the x-height is the same no matter what font is used. This preserves the readability of the text when fallback happens.'
tags:
  - CSS
  - Properties
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected
uri: css/properties/font-size-adjust

---
## Summary

The font-size-adjust property adjusts the font-size of the fallback fonts defined with font-family, so that the x-height is the same no matter what font is used. This preserves the readability of the text when fallback happens.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `none`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   as specified

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `fontSizeAdjust`

Percentages
:   N/A

## Syntax

-   `font-size-adjust: auto`
-   `font-size-adjust: none`
-   `font-size-adjust: number`

## Values

none
:   Only use the font-size value to determine the size of the font.

number
:   The value used in calculating the size of the fallback fonts. For the adjusted font size calculation, see [Notes](/css/properties/font-size-adjust#Notes).

auto
:   The aspect value is calculated by the browser for the first font in the font-family list, and used for every font in that list.

## Examples

The popular font "Verdana" has an aspect value of 0.58. For comparison, Times New Roman has an aspect value of 0.45. Verdana will be more readable at smaller sizes than Times New Roman. Conversely, Verdana will often look 'too big' if substituted for Times New Roman.

``` html
<table>
  <tr>
    <td class="demoblock">
      <p class="verdana">Normal "Verdana" font text. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed tempus mattis lorem sed fringilla. Duis eu nulla dolor. Donec tempor risus sem, vitae sollicitudin nulla sagittis sit amet. Nulla laoreet augue in libero posuere lobortis. </p>
    </td>
    <td class="demoblock">
      <p class="times">Normal "Times New Roman" font text. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed tempus mattis lorem sed fringilla. Duis eu nulla dolor. Donec tempor risus sem, vitae sollicitudin nulla sagittis sit amet. Nulla laoreet augue in libero posuere lobortis.</p>
    <td class="demoblock">
      <p class="adjust">"Times New Roman" with font-size-adjust of 0.58. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed tempus mattis lorem sed fringilla. Duis eu nulla dolor. Donec tempor risus sem, vitae sollicitudin nulla sagittis sit amet. Nulla laoreet augue in libero posuere lobortis.</p>
    </td>
  </tr>
</table>
```

``` css
.demoblock {
    width: 33%;
}

p {
    font-size: 8px;
}

p.verdana {
    font-family: Verdana,"Times New Roman", serif;
}

p.times {
    font-family: "Times New Roman";
}

p.adjust {
    font-family: hoge, "Times New Roman", serif;
    font-size-adjust: 0.58;
}
```

## Notes

In script types that distinguish between uppercase and lowercase letters, such as the Latin script used for English, the height of the lowercase letters relative to the height of the uppercase letters impacts readability at smaller type sizes. This relation is called the **aspect value**, which is calculated by dividing a font's **[x-height](/x_height)** by the font's size.

The **font-size-adjust** property preserves the readability of text when the first specified font is not available and a fallback or replacement font is used. It adjusts the [font-size](/css/properties/font-size) so the **[x-height](/x_height)** of the fallback or replacement is similar to the **[x-height](/x_height)** of the font it's replacing.

Specify a value of **auto** to have the browser calculate the **aspect value** of the primary font and apply it to fallback or replacement fonts. When specifying a **number** value, use the preferred **aspect value** and the browser will apply it to fallback or replacement fonts using the following formula:

c = (p / a) \* s

Where:

-   c = adjusted font size
-   p = preferred **aspect value**
-   a = **aspect value** of the replacement or fallback
-   s = the font size

As an abstract example, assume you specify a font-size-adjust value of 0.5, your fallback font's **aspect value** is .4, and the [font-size](/css/properties/font-size) is 8px. The fallback font is rendered at 10px ((.5 /.4) \* 8).

## Related specifications

[CSS Fonts Module Level 3](http://www.w3.org/TR/css3-fonts/#propdef-font-size-adjust)
:   W3C Working Draft

## See also

### Related articles

#### CSS Font

-   [font-family](/css/properties/font-family)

-   [font-kerning](/css/properties/font-kerning)

-   [font-language-override](/css/properties/font-language-override)

-   [font-size](/css/properties/font-size)

-   **font-size-adjust**

-   [font-style](/css/properties/font-style)

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

-   **font-size-adjust**

-   [font-stretch](/css/properties/font-stretch)

-   [font-style](/css/properties/font-style)

-   [font-variant](/css/properties/font-variant)

-   [user-modify](/css/properties/user-modify)

-   [size](/html/attributes/size)

-   [font](/html/elements/font)

### External resources

-   MDN: [font-size-adjust](https://developer.mozilla.org/en-US/docs/Web/CSS/font-size-adjust)

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   style[style](/css/cssom/style)
-   defaults[defaults](/w/index.php?title=dom/defaultSelected&action=edit&redlink=1)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   font-stretch[font-stretch](/css/properties/font-stretch)
