---
title: layout-grid-type
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
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
  - CSS
  - Properties
uri: css/properties/layout-grid-type

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

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

-   `layout-grid-type: fixed`
-   `layout-grid-type: loose`
-   `layout-grid-type: strict`

## Values

loose
:   Default. Grid used for Japanese and Korean characters. In this mode, a constant width increment is applied to characters as follows: Wide characters and narrow kana characters are incremented to obtain an exact grid fit, as specified by the [**-ms-layout-grid-char**](/css/properties/layout-grid-char) property. Other narrow characters, except connected and cursive characters, are incremented by half of the increment amount applied to wide characters. Other characters, including connected and cursive characters, are not incremented, and behave as if no character grid is set.

strict
:   Grid used for Chinese, as well as Japanese (Genko) and Korean characters. Only the ideographs, kanas, and wide characters are snapped to the grid. Other characters are rendered as usual, as though the [**-ms-layout-grid-mode**](/css/properties/layout-grid-mode) attribute is set to **none** or **line** for text spans containing these characters. This mode also disables special text justification and character width adjustments normally applied to the element. Finally, if there is no line-break opportunity in a text span that exceeds the line boundary, the text is pushed to the next line and the last part of the previous line is left blank.

fixed
:   Grid used for monospaced layout. The layout rules are as follows: All noncursive characters are treated as equal; every character is centered within a single grid space by default. Runs of cursive characters are treated as strips the same as in a **strict** grid. Justification or any other character-width changing behaviors are disabled.

## Examples

This example uses the **-ms-layout-grid-type** attribute to specify character layout for a block of text.

``` html
<STYLE>
DIV.layout { layout-grid-type: strict }
</STYLE>
<DIV CLASS = "layout">
This is a block element containing a sentence of sample text.
</DIV>
```

## Notes

### Remarks

Windows Internet Explorer 8. The **-ms-layout-grid-type** attribute is an extension to CSS, and can be used as a synonym for **layout-grid-type** in IE8 Standards mode. Web documents in Asian languages, such as Chinese or Japanese, usually create a page layout for characters using a one- or two-dimensional grid. You can use the [**-ms-layout-grid**](/css/properties/layout-grid) attribute to incorporate this layout into Web documents. The **-ms-layout-grid-type** attribute applies only to block-level elements.

### Syntax

`-ms-layout-grid-type: loose | strict | fixed`

### Standards information

There are no standards that apply here.

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

-   [ime-mode](/css/properties/ime-mode)

-   [layout-grid](/css/properties/layout-grid)

-   [layout-grid-char](/css/properties/layout-grid-char)

-   [layout-grid-line](/css/properties/layout-grid-line)

-   [layout-grid-mode](/css/properties/layout-grid-mode)

-   **layout-grid-type**

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

### Related pages (MSDN)

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `runtimeStyle`
-   `style`
