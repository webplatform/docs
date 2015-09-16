---
title: 'font'
code_samples:
  - 'http://gist.github.com/6947832'
  - 'http://gist.github.com/5586740'
compatibility:
  feature: font
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`normal for font-style, font-variant and font-weight. medium for font-size. normal for line-height. font-family initial value differs depending on the user agent.`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'See the individual properties'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`font`'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The font property is shorthand that allows you to do one of two things: you can either set up six of the most mature font properties in one line, or you can set one of a choice of keywords to adopt a system font setting.'
tags:
  - CSS
  - Properties
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected
uri: css/properties/font

---
## Summary

The font property is shorthand that allows you to do one of two things: you can either set up six of the most mature font properties in one line, or you can set one of a choice of keywords to adopt a system font setting.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `normal for font-style, font-variant and font-weight. medium for font-size. normal for line-height. font-family initial value differs depending on the user agent.`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   See the individual properties

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `font`

## Syntax

-   `font: font-weight font-style font-variant font-size/line-height font-family`
-   `font: system font`

## Values

font-weight font-style font-variant font-size/line-height font-family
:   `font` can take up to six separate parts in its value, which set six different longhand property values. The options are as follows:

-   `font-weight`: Sets boldness of font; can take values of `normal` (default), `bold` (standard bold weight), `lighter` or `bolder` (supposed to be a slightly lighter or bolder weight that standard `bold`), inherit, or various numerical values to indicate different degrees of boldness: `100`, `200`, `300`, `400`, `500`, `600`, `700`, `800`, or `900`.
-   `font-style`: Allows an italic or oblique font face to be applied; values options are `normal` (default), italic, oblique, or inherit.
-   `font-variant`: Allows a small caps font variant to be set. Value options are `normal` (default), `small-caps`, or `inherit`.
-   `font-size`: Sets a size for the font. Options are absolute size keywords (`xx-small`, `x-small`, `small`, `medium` (the default value), `large`, `x-large` or `xx-large`), relative size keywords (`smaller` or `larger`, which indicate a keyword size smaller or larger than the parent element's font size), length values (for example `12px`, or `5rem`), percentage values (for example `80%`), or `inherit`.
-   `line-height`: Sets the height of the line the font is sat on. Value options include `normal` (the default), unitless values (for example `1.7`), length values (for example `20px` or `3.5rem`), percentage values (for example `120%`), or `inherit`.
-   `font-family`: Allows one or more font family names and/or generic family names to be specified for usage on the selected element(s)' text. The browser then goes through the list; for each character in the selection it applies the first font family that has an available glyph for that character.

system font
:   Alternatively, you can set the value to be a single keyword that corresponds to a system font used to style a certain feature of the system the browser is running on (some browsers offer more, proprietary options. For more, see the links at the bottom of the document):

-   `caption`: User-preference font used in objects that have captions—buttons, labels, and so on.
-   `icon`: User-preference font used in icon labels.
-   `menu`: User-preference font used in menus.
-   `message-box`: User-preference font used in dialog boxes.
-   `small-caption`: User-preference font used in small controls.
-   `status-bar`: User-preference font used in small controls.

## Examples

A selection of examples showing some typical uses of the `font` property.

``` css
.example-one {
  /*    size  family    */
  font: 1.5em sans-serif;
}

.example-two {
  /*    style  variant    weight size/line-height family    */
  font: italic small-caps bold   1em/1.5em        sans-serif;
}

.example-three {
  /*    weight size/line-height family                         */
  font: bold   1em/2em          "Times New Roman", Times, serif;
}
```

[View live example](http://code.webplatform.org/gist/6947832)

A couple of theoretical font examples, showing first a `font` property value with all possible longhand values included, and second, a system default font being used.

``` css
.one {
  font: bold italic small-caps 18px/24px georgia;
}

.two {
  font: status-bar;
}
```

[View live example](http://code.webplatform.org/gist/5586740)

## Notes

-   The **font-style**, **font-variant**, and **font-weight** values may appear in any order before **font-size**. However, the **font-size**, **line-height**, and **font-family** properties must appear in the order listed. Setting the **font** property also sets the component properties. In this case, the string must be a combination of valid values for the component properties; only **font-family** may have more than one value.

If the string does not contain a value for a component property, that property is set to its default, regardless of prior settings for that component property.

-   Read <https://developer.mozilla.org/en-US/docs/Web/CSS/font> for more information on Firefox's additional proprietary system font settings.

## Related specifications

[CSS Fonts Module Level 3](http://www.w3.org/TR/css3-fonts/#font-prop)
:   W3C Working Draft

## See also

### Related articles

#### Fonts

-   [@font-face](/css/atrules/@font-face)

-   [Font related properties](/css/fonts)

-   [font-variant](/css/fonts/font-variant)

-   **font**

-   [font-family](/css/properties/font-family)

-   [font-feature-settings](/css/properties/font-feature-settings)

-   [font-kerning](/css/properties/font-kerning)

-   [font-language-override](/css/properties/font-language-override)

-   [font-size](/css/properties/font-size)

-   [font-size-adjust](/css/properties/font-size-adjust)

-   [font-stretch](/css/properties/font-stretch)

-   [font-style](/css/properties/font-style)

-   [font-variant](/css/properties/font-variant)

-   [user-modify](/css/properties/user-modify)

-   [size](/html/attributes/size)

-   [font](/html/elements/font)

### External resources

-   MDN: [font @ MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/font)

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   defaults[defaults](/w/index.php?title=dom/defaultSelected&action=edit&redlink=1)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
