---
title: unicode-range
tags:
  - CSS
  - Properties
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'unicode-range allows you to set a specific range of characters to be downloaded from a font (embedded using @font-face) and made available for use on the current page.'
code_samples:
  - 'http://gist.github.com/6366676'
uri: css/properties/unicode-range

---
# unicode-range

## Summary

unicode-range allows you to set a specific range of characters to be downloaded from a font (embedded using @font-face) and made available for use on the current page.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `U+0-10FFFF`
Applies to
:   The `@font-face` block the property is included inside.
[Inherited](/css/concepts/inherited)
:   No
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   Same as the inputted value
Animatable
:   No
[CSS Object Model Property](/css/concepts/cssom)
:   `unicodeRange`

## Syntax

-   `unicode-range: codepoint range`
-   `unicode-range: multiple value declarations`
-   `unicode-range: single codepoint`
-   `unicode-range: wildcard range`

## Values

single codepoint
:   A single unicode character codepoint, for example `unicode-range: U+26`.

codepoint range
:   A range of unicode codepoints. So for example, `unicode-range: U+0025-00FF` means "include all characters in the range U+0025 to U+00FF."

wildcard range
:   You can specify wildcard characters using the "?" character, so for example `unicode-range: U+4??` would mean "include all characters in the range U+400 to U+4FF."

multiple value declarations
:   You can specify multiple single codepoints and/or codepoint groups, delimiting them using commas. For example, `unicode-range: U+00-FF, U+980-9FF`.

## Examples

A single paragraph of HTML, including an ampersand. We have wrapped the ampersand in a `<span>` element because we want to use a different ampersand from a different font.

``` {.html}
<p>Me & You = Us</p>
```

[View live example](http://code.webplatform.org/gist/6366676)

The CSS for the example above: you can see that we are in effect defining a completely separate `@font-face` that only includes a single character in it, meaning that we don't need to download the entire font to get what we want if it is a hosted font, and if it is a local font as in this example, we can at least cut down on extra markup and styles (we could also do this by wrapping the ampersand in a `<span>` and applying a different font just to that, but that is an extra element and ruleset!)

Be aware that Firefox does not yet support `unicode-range` properly, hence the reason for the second `@font-face` block. Here we are pointing to an obscure unicode codepoint that will likely never be used in our document, causing Firefox to stop applying the posh Eccentric font to the whole paragraph (definitely not what we want.) — just helvetica is a better fallback.

``` {.css}
@font-face {
  font-family: 'Ampersand';
  src: local('Eccentric STD');
  unicode-range: U+26;
}

@font-face {
    /* Ampersand fallback font */
    font-family: 'Ampersand';
    src: local('helvetica');
    unicode-range: U+270C;
}

p {
    color: #faf;
    letter-spacing: -0.05em;
    font-size: 64px;
    font-family: Ampersand, helvetica, sans-serif;
}
```

## Usage

     * As the examples above show, you can use unicode-range to create a custom @font-face that contains only the characters you need to be downloaded, saving on bandwidth.

-   You should always include a fallback font that is acceptable in case your `unicode-range @font-face` is not supported.
-   Support for `unicode-range` is currently limited; Chrome and Safari supports it well, Internet Explorer supports is as of version 9, Opera supports it, Firefox *doesn't* support it.

## Related specifications

Specification
:   Status
[CSS Fonts Module Level 3](http://www.w3.org/TR/css-fonts-3/#descdef-unicode-range)
:   Candidate Recommendation

## See also

### External resources

-   [Creating custom font stacks with unicode-range](http://24ways.org/2011/creating-custom-font-stacks-with-unicode-range/)
-   [Unicode code converter](http://www.rishida.net/tools/conversion/)
-   [UniView](http://rishida.net/scripts/uniview/) web-based tool for viewing and working with Unicode codepoints
-   [Using unicode-range in @font-face in CSS](http://rishida.net/blog/?p=760)
-   [List of Unicode Characters](http://en.wikipedia.org/wiki/List_of_Unicode_characters)

