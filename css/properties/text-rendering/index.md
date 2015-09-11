---
title: text-rendering
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'text elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': auto
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`text-rendering`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Last Call Working Draft'
summary: 'The text-rendering CSS property provides information to the browser about how to optimize when rendering text. Options are: legibility, speed or geometric precision.'
tags:
  0: CSS
  1: Properties
  3: Graphics
  4: SVG
uri: css/properties/text-rendering

---
## <span>Summary</span>

The text-rendering CSS property provides information to the browser about how to optimize when rendering text. Options are: legibility, speed or geometric precision.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `auto`

Applies to
:   text elements

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   auto

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `text-rendering`

Percentages
:   N/A

## <span>Syntax</span>

-   `text-rendering: auto`
-   `text-rendering: geometricPrecision`
-   `text-rendering: optimizeLegibility`
-   `text-rendering: optimizeSpeed`

## <span>Values</span>

auto
:   Indicates that the browser should choose the most appropriate method between speed, legibility and geometric precision, but favors legibility over speed and geometric precision.

optimizeSpeed
:   Indicates that the browser should favor rendering speed over legibility and geometric precision. Browsers usually disable kerning and ligatures and sometimes turn off anti-aliasing.

optimizeLegibility
:   Indicates that the browser should favor legibility over rendering speed and geometric precision. Browsers usually apply anti-aliasing or font hinting to display the most legible text.

geometricPrecision
:   Indicates that the browser should favor geometric precision over rendering speed and legibility. Usually, this option causes the browser to not use hinting. Instead glyph outlines are drawn with comparable geometric precision to the rendering of path data.

This setting can be helpful when using kerning, which does often not scale linearly and can make text using such fonts look good.

## <span>Examples</span>

``` css
/* The user agent will decide how to optimize text for speed, legibility and geometric precision. */
body {
    text-rendering: auto;
}

/* The user agent will prioritize the rendering speed of text. */
body {
    text-rendering: optimizeSpeed;
}

/* The user agent will prioritize the legibility of text. */
body {
    text-rendering: optimizeLegibility;
}

/* The user agent will prioritize the geometric precision of text. */
body {
    text-rendering: optimizePrecision;
}
```

## <span>Usage</span>

     Gecko note:

In Gecko browsers there is a way to set the threshold value for the auto keyword by changing the preference in browser.display.auto\_quality\_min\_font\_size. By default it is set to 20px. On Gecko 2.0 (Firefox 4 / Thunderbird 3.3 / SeaMonkey 2.1) the optimizeSpeed option has no effect because there is no faster way of rendering text than the standard code already does. See bug [bug 595688](https://bugzilla.mozilla.org/show_bug.cgi?id=595688) for more details on that.

## <span>Notes</span>

The property is a SVG property not specified in any CSS standard yet. However, user agents including Gecko and WebKit browsers let you apply this property to HTML and XML content on Windows, Mac OS X and Linux via CSS.

## <span>Related specifications</span>

[CSS Text Module Level 3](http://www.w3.org/TR/css3-text/)
:   W3C Last Call Working Draft

## <span>See also</span>

### <span>Related articles</span>

#### <span>CSS Font</span>

-   [font-family](/css/properties/font-family)

-   [font-kerning](/css/properties/font-kerning)

-   [font-language-override](/css/properties/font-language-override)

-   [font-size](/css/properties/font-size)

-   [font-size-adjust](/css/properties/font-size-adjust)

-   [font-style](/css/properties/font-style)

-   [font-variant](/css/properties/font-variant)

-   **text-rendering**

-   [text-underline](/css/properties/text-underline)

-   [user-modify](/css/properties/user-modify)

#### <span>CSS Attributes</span>

-   [background-blend-mode](/css/properties/background-blend-mode)

-   [background-position](/css/properties/background-position)

-   [break-before](/css/properties/break-before)

-   [height](/css/properties/height)

-   [list-style](/css/properties/list-style)

-   [list-style-position](/css/properties/list-style-position)

-   [text-overflow-ellipsis](/css/properties/text-overflow-ellipsis)

-   [text-overflow-mode](/css/properties/text-overflow-mode)

-   **text-rendering**

-   [user-select](/css/properties/user-select)

-   [equality](/css/selectors/attributes/equality)

-   [Attribute selector](/css/selectors/attributes/existence)

-   [hyphen](/css/selectors/attributes/hyphen)

-   [prefix](/css/selectors/attributes/prefix)

-   [substring](/css/selectors/attributes/substring)

-   [suffix](/css/selectors/attributes/suffix)

-   [baseline-shift](/svg/attributes/baseline-shift)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

#### <span>Text</span>

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

-   [layout-grid-type](/css/properties/layout-grid-type)

-   [letter-spacing](/css/properties/letter-spacing)

-   [text-overflow-ellipsis](/css/properties/text-overflow-ellipsis)

-   [text-overflow-mode](/css/properties/text-overflow-mode)

-   **text-rendering**

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
