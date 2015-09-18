---
title: 'font-family'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://code.webplatform.org/gist/5496591'
compatibility:
  feature: font-family
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`depends on user agent`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`fontFamily`'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The font-family property allows one or more font family names and/or generic family names to be specified for usage on the selected element(s)'' text. The browser then goes through the list; for each character in the selection it applies the first font family that has an available glyph for that character.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/font-family

---
## Summary

The font-family property allows one or more font family names and/or generic family names to be specified for usage on the selected element(s)' text. The browser then goes through the list; for each character in the selection it applies the first font family that has an available glyph for that character.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `depends on user agent`

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
:   `fontFamily`

## Syntax

-   `font-family: family-name`
-   `font-family: family-name, family-name, generic-family`
-   `font-family: generic-family`

## Values

family-name
:   The name of a font family, such as `courier` or `arial`. You can reference fonts available on the user's system, or external fonts imported using [@font-face](/css/atrules/@font-face). When the family name contains more than one word, it should be enclosed in quotes, for example `'Comic Sans'`.

generic-family
:   generic families are not specific fonts, but a reference to fallback fonts of a general type that can be used when specific fonts are not available. The actual fonts used for each fallback type may differ between operating systems. The following generic family keywords are defined: `serif`, `sans-serif`, `cursive`, `fantasy` and `monospace`.

family-name, family-name, generic-family
:   You can specify a comma-separated list of multiple font family names and/or generic family names, although it rarely makes sense to specify more than one generic family. This list is called a **font-stack**. The browser goes down the list and uses the first available font that it can find available on the system. Generic font families are used as a fallback when none of the fonts specified in the stack are available. It is always the last alternative in the list of font family names.

## Examples

It is simple to define built-in fonts to use in your CSS content.

``` css
h1 { font-family: Helvetica, Arial, sans-serif; }
p { font-family: "Times New Roman", serif; }
```

[View live example](http://code.webplatform.org/gist/5496591)

The following example imports a web font into your CSS using `@font-face` and then assigns it to an element using font-family

``` css
/*
Defines the font and its location. font-family in this case assigns a name to the font
*/
@font-face {
  font-family: 'VeraSe';
  src: url("../_fonts/VeraSe.eot");
  src: local("☺"),
  url("../_fonts/VeraSe.woff") format("woff"),
  url("../_fonts/VeraSe.ttf") format("truetype"),
  url("../_fonts/VeraSe.svg") format("svg");
  font-weight: normal;
  font-style: normal;
}

/*
We now use the name in defining the fonts for a h1 element
*/

h1 {
  font-family: VeraSe, Georgia, serif;
  margin-top: 15px;
  margin-bottom: 15px;
}
```

## Usage

     * If a font family name contains whitespace, digits or punctuation characters (other than hyphens), you should place quotes around the font family name to avoid mistakes in escaping those characters

-   Generic font family names are values (keywords) and cannot appear in quotation marks

## Related specifications

[CSS 2.1, section 15.3](http://www.w3.org/TR/CSS21/fonts.html#font-family-prop)
:   W3C Recommendation 07 June 2011

[CSS Fonts Module Level 3](http://www.w3.org/TR/css3-fonts/)
:   W3C Working Draft 12 February 2013

[CSS3 module: Web Fonts](http://www.w3.org/TR/2002/WD-css3-webfonts-20020802/)
:   W3C Working Draft 2 August 2002

## See also

### Related articles

#### CSS Font

-   **font-family**

-   [font-kerning](/css/properties/font-kerning)

-   [font-language-override](/css/properties/font-language-override)

-   [font-size](/css/properties/font-size)

-   [font-size-adjust](/css/properties/font-size-adjust)

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

-   **font-family**

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

-   [Unquoted font family names in CSS](http://mathiasbynens.be/notes/unquoted-font-family)
-   [Basic Font Properties](http://dev.w3.org/csswg/css3-fonts/#font-family-prop)
-   [font-family @ MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/font-family)
