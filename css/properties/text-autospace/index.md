---
title: 'text-autospace'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5842252'
compatibility:
  feature: text-autospace
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'specified value (except for initial and inherit)'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Last Call Working Draft'
summary: 'When non-ideographic characters (such as numbers) are presented alongside ideographic characters, many designers prefer to include spacing to separate it from the surrounding ideographs.  This property automates the creation of that space by introducing an in-line margin, the width of which corresponds to the width of existing ideographs.'
tags:
  - CSS_Properties
  - CSS
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected
uri: css/properties/text-autospace

---
## Summary

When non-ideographic characters (such as numbers) are presented alongside ideographic characters, many designers prefer to include spacing to separate it from the surrounding ideographs. This property automates the creation of that space by introducing an in-line margin, the width of which corresponds to the width of existing ideographs.

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
:   specified value (except for initial and inherit)

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   N/A

## Syntax

-   `text-autospace: ideograph-alpha`
-   `text-autospace: ideograph-numeric`
-   `text-autospace: ideograph-parenthesis`
-   `text-autospace: ideograph-space`
-   `text-autospace: none`

## Values

none
:   Default. No effect takes place—that is, no extra space is added.

ideograph-alpha
:   Creates extra spacing between runs of ideographic and non-ideographic text, such as Latin-based, Cyrillic, Greek, Arabic, or Hebrew text.

ideograph-numeric
:   Creates extra spacing between runs of ideographic text and numeric characters.

ideograph-parenthesis
:   Creates extra spacing between a normal (non-wide) parenthesis and an ideograph.

ideograph-space
:   Extends the width of the space character when it is adjacent to ideographs.

## Examples

By setting the **text-autospace** property to various keywords, one can easily modify the spacing standards of combinations of ideographic and non-ideographic characters.

``` css
/**
 * Using the CSS `text-autospace` property.
 */

tr:nth-child(3) {
    text-autospace: ideograph-numeric;
}

tr:nth-child(4) {
    text-autospace: ideograph-alpha;
}

tr:nth-child(5) {
    text-autospace: ideograph-parenthesis;
}
```

[View live example](http://gist.github.com/5842252)

## Usage

     This property acts in addition to other properties such as css/properties/word-spacing and css/properties/letter-spacing, meaning that you can use both properties and their effects will be compounded.

This property is not currently supported by any major browser.

## Notes

### Remarks

Windows Internet Explorer 8. The **-ms-text-autospace** attribute is an extension to CSS, and can be used as a synonym for **text-autospace** in IE8 Standards mode. An ideograph is a character in an Asian writing system that represents a concept or an idea, but not a particular word or pronunciation.

### Syntax

`-ms-text-autospace: none | ideograph-alpha | ideograph-numeric | ideograph-parenthesis | ideograph-space`

### Standards information

-   [CSS Text Level 3](http://go.microsoft.com/fwlink/p/?linkid=203766), Section 9.4

## Related specifications

[CSS Text Module Level 3](http://www.w3.org/TR/css3-text/)
:   W3C Last Call Working Draft

## See also

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   defaults[defaults](/w/index.php?title=dom/defaultSelected&action=edit&redlink=1)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
-   styleSheet[styleSheet](/css/cssom/styleSheet)
