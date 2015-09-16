---
title: 'tab-size'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/Web/CSS/tab-size)'
code_samples:
  - 'http://gist.github.com/5673098'
compatibility:
  feature: tab-size
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`8`'
  'Applies to': 'block containers'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'the specified integer or an absolute length'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The tab-size CSS property is used to customise the width of a tab (U+0009) character.'
tags:
  - CSS
  - Properties
uri: css/properties/tab-size

---
## Summary

The tab-size CSS property is used to customise the width of a tab (U+0009) character.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `8`

Applies to
:   block containers

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   the specified integer or an absolute length

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

## Syntax

-   `tab-size: <integer>`
-   `tab-size: inherit`

## Values

\<integer\>
:   The number of spaces in a tab. Must be positive.

inherit
:   Inherits from the parent element.

## Examples

Example of using different tab-size.

``` css
/**
Examples of using the tab-size prop
*/

.tab--size4 {
    tab-size: 4;
}

.tab--size8 {
    tab-size: 8;
}

.tab--size12 {
    tab-size: 12;
}

.tab--size0 {
    tab-size: 0;
}
```

[View live example](http://code.webplatform.org/gist/5673098)

## Notes

The tab character (unicode U+0009) is converted to space characters (unicode U+0020) by the white space rule (default is normal) which collapses multiple white space characters. Therefor this rule only makes sense inside a parent that cancels the white-space rule. For example the pre tag (which does this by default, setting it to pre-wrap) . See the example.

## Related specifications

[CSS Text Module Level 3](http://dev.w3.org/csswg/css-text/)
:   Editor's draft
