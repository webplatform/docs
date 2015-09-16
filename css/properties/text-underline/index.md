---
title: 'text-underline'
code_samples:
  - 'http://gist.github.com/5779274'
compatibility:
  feature: text-underline
  topic: css
notes:
  - "\nDeletion Candidate:   This page is a candidate for deletion because the property was never implemented. To underline text, see http://docs.webplatform.org/wiki/css/properties/text-decoration.\n\n"
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`not defined for shorthand properties`'
  'Applies to': 'all elements with textual content, including generated content'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'specified value (except for initial and inherit)'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`N/A`'
  Percentages: N/A
readiness: 'Not Ready'
standardization_status: Non-Standard
summary: "Unsupported.\n"
tags:
  - CSS
  - Properties
uri: css/properties/text-underline

---
## Summary

Unsupported.

The 'text-underline' property is the shorthand for 'text-underline-style', 'text-underline-width', 'text-underline-color', 'text-underline-mode' and 'text-underline-position'.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `not defined for shorthand properties`

Applies to
:   all elements with textual content, including generated content

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   specified value (except for initial and inherit)

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `N/A`

Percentages
:   N/A

## Syntax

-   `text-underline: text-underline-color`
-   `text-underline: text-underline-mode`
-   `text-underline: text-underline-position`
-   `text-underline: text-underline-style`

## Values

text-underline-style
:   This property specify the line style for underline.

Possible values: none/solid/double/dotted/dashed/dot-dash/dot-dot-dash/wave

text-underline-color
:   This property specifies the line color for the underline.

text-underline-mode
:   This property set the mode for the underline determining whether the text decoration affects the space characters or not. 'Space characters' are all characters classified by the Unicode Standard [UNICODE] as category 'Zs', in addition to the white space characters.

Possible values: continuous/skip-white-space

text-underline-position
:   This property sets the position of the underline. It can appear either 'before' (above in an horizontal flow) or after (below in an horizontal flow) the run of text in relation to its baseline orientation. This property is typically used in vertical writing context where it may be desired to have the underline appear 'before' the run of text. This results in having the underline appearing on the right side of the vertical writing column.

Possible values: auto/before-edge/alphabetic/after-edge

## Examples

``` css

```

[View live example](http://code.webplatform.org/gist/5779274)

## Usage

     The property text-underline is not supported by any of listed new browsers (Chrome/FF/Opera/IE10).

Instead use **text-decoration: underline**.

The possible exception is **text-underline-position**: <http://docs.webplatform.org/wiki/css/properties/text-underline-position>.

## Notes

The 'text-decoration' property has limitations stemming from its syntax, precluding fine control over each of those formatting effects. Specifically, it offers no way to control the color or line style of the underline, overline or line-through. CSS3 extends the model by introducing new properties allowing additional controls over those formatting effects. CSS3 also makes turning these formatting effects on or off possible without affecting any other 'text-decoration' settings.

## See also

### Related articles

#### CSS Font

-   [font-family](/css/properties/font-family)

-   [font-kerning](/css/properties/font-kerning)

-   [font-language-override](/css/properties/font-language-override)

-   [font-size](/css/properties/font-size)

-   [font-size-adjust](/css/properties/font-size-adjust)

-   [font-style](/css/properties/font-style)

-   [font-variant](/css/properties/font-variant)

-   [text-rendering](/css/properties/text-rendering)

-   **text-underline**

-   [user-modify](/css/properties/user-modify)
