---
title: 'text-transform'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/).'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5651013'
  - 'http://gist.github.com/5651033'
compatibility:
  feature: text-transform
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: 'no'
readiness: 'Ready to Use'
standardization_status: 'W3C Last Call Working Draft'
summary: 'This property transforms text for styling purposes. (It has no effect on the underlying content.)'
tags:
  - CSS
  - Properties
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected
uri: css/properties/text-transform

---
## Summary

This property transforms text for styling purposes. (It has no effect on the underlying content.)

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
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   no

## Syntax

-   `text-transform: capitalize`
-   `text-transform: full-width`
-   `text-transform: lowercase`
-   `text-transform: none`
-   `text-transform: uppercase`

## Values

none
:   Default. Text is not transformed.

capitalize
:   Transforms the first character of each word to uppercase.

uppercase
:   Transforms all the characters to uppercase.

lowercase
:   Transforms all the characters to lowercase.

full-width
:   Puts all characters in fullwidth form. If the character does not have a corresponding fullwidth form, it is left as is. This value is typically used to typeset Latin characters and digits like ideographic characters.

## Examples

Examples using different values for text-transform

``` css
/*
    - text-transform property examples
    - explanations inline
*/

body {
    padding:50px;
    font-size:22px;
}

.text--uppercase {
    text-transform:uppercase; /* all uppercase characters */
}

.text--lowercase{
    text-transform: lowercase; /* all lowercase characters */
}

.text--capitalize{
    text-transform: capitalize; /* _first_ letter of each word is capitalized  */
}

.text--no-transform {
    text-transform: none; /* disables any other inherited text-transform */
}
```

[View live example](http://code.webplatform.org/gist/5651013)

Using text-transform also works on greek or german letters

``` css
/*
    - text-transform property examples
    - explanations inline
*/

body {
    padding:50px;
    font-size:22px;
}

.text--uppercase {
    text-transform:uppercase; /* works on non-latin characters as well */
}
```

[View live example](http://code.webplatform.org/gist/5651033)

## Notes

When using text-transform: capitalize; authors should not expect capitalize to follow language-specific titlecasing conventions (such as skipping articles in English).

## Related specifications

[CSS Text Module Level 3](http://www.w3.org/TR/css3-text/)
:   W3C Last Call Working Draft

## See also

### External resources

<http://www.w3.org/TR/CSS2/text.html#caps-prop>

<http://www.w3.org/wiki/CSS/Properties/text-transform>

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   defaults[defaults](/w/index.php?title=dom/defaultSelected&action=edit&redlink=1)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
