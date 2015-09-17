---
title: 'font-size'
code_samples:
  - 'http://gist.github.com/5628042'
  - 'http://gist.github.com/5628240'
compatibility:
  feature: font-size
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`medium`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified, but with relative lengths converted into absolute pixel values.'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`fontSize`'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'font-size sets the font size of the text inside the element to which it is applied, and that of its descendants. You can size text using absolute measurements, or measurements relative to the affected element''s parent or root elements. CSS Text Styling Fundamentals provides an overview.'
tags:
  - CSS_Properties
  - CSS
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'css/concepts/CSS pixels'
    - css/properties/text-size-adjust
uri: css/properties/font-size

---
## Summary

font-size sets the font size of the text inside the element to which it is applied, and that of its descendants. You can size text using absolute measurements, or measurements relative to the affected element's parent or root elements. CSS Text Styling Fundamentals provides an overview.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `medium`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   as specified, but with relative lengths converted into absolute pixel values.

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `fontSize`

## Syntax

-   `font-size: absolute keywords`
-   `font-size: inherit`
-   `font-size: length`
-   `font-size: percentage`
-   `font-size: relative keywords`

## Values

absolute keywords
:   A set of keywords indicating predefined font sizes that scale according to font setting preferences or each browser's default values. From smallest to largest, possible values are **xx-small**, **x-small**, **small**, **medium**, **large**, **x-large**, and **xx-large**.

relative keywords
:   A set of keywords interpreted relative to the parent element's **font-size** — either **smaller** or **larger**.

length
:   An absolute unit value: any of the standard [css length units](/css/data_types/length) are allowed. Negative lengths are illegal.

percentage
:   A percentage value specifies an absolute font size relative to the parent element's **font-size**.

inherit
:   The `inherit` keyword causes the element to adopt its parent element's font size.

## Examples

A selection of examples showing some typical uses of the font-size property.

``` html
<p class="example-one">Example One: We ♥ WebPlatform Docs!</p>
<p class="example-two">Example Two: Lorem ipsum dolor sit amet, consectetur adipisicing elit. Officiis, eos, dicta nihil aliquid quia dolores labore nesciunt unde consectetur blanditiis ex eius consequatur qui incidunt voluptatem inventore fugit quos amet!</p>
<p class="example-three">Example Three: Eius, earum unde eum distinctio ex accusamus rem eligendi optio mollitia deleniti? Iure, accusamus, fuga ipsa quas doloremque enim velit sed est earum pariatur ab optio quia molestiae repellendus non.</p>
```

``` css
.example-one {
    font-size: 1.2em;
}

.example-two {
    font-size: small;
}

.example-three {
    font-size: 28px;
}
```

[View live example](http://gist.github.com/5628042)

A redefinition of the typical **16px** browser default font size **medium** value as **10px**, followed by a resizing of the text that follows proportionate to that.

``` css
html { font-size: 62.5%; }
/*
16 * 62.5% == 10
*/

.example-one { font-size: 3.6rem }   /* 36px */
.example-two { font-size: 2.4rem }   /* 24px */
.example-three  { font-size: 1.4rem }   /* 14px */
```

[View live example](http://gist.github.com/5628240)

## Usage

     Keywords such as large and medium, or relative em or percentage units, are generally safer to use than pixel measurements, especially for mobile web browsers that adjust their set of default font sizes for legibility. Use of percentage values, or values in  ems, leads to more robust and cascadable style sheets.

Otherwise, pixels offer the safest way to specify measurements, since [CSS pixels](/w/index.php?title=css/concepts/CSS_pixels&action=edit&redlink=1) are adjusted for variations in display pixel density.

While the initial **medium** size applies widely, browsers apply a default style sheet that modifies it for various semantic elements, boosting the size of headings, for example. Browsers also automatically resize fonts when zooming the page, stepping by values that may not correspond exactly to the zoom factor. Unless disabled using [**text-size-adjust**](/w/index.php?title=css/properties/text-size-adjust&action=edit&redlink=1), fonts also resize when tipping between portrait and landscape orientations on mobile browsers. For an overview of the issue, see [The Mobile Viewport and Orientation](/tutorials/mobile_viewport).

The value of **font-size** also affects the value of [**line-height**](/css/properties/line-height) when using its default or relative measurements.

Along with many other CSS properties, **font-size** can also be applied directly as an SVG attribute:

``` xml
<text x="12px" y="12px" font-family="sans-serif" font-size="120%"/>
```

## Related specifications

[CSS Fonts Module Level 3](http://www.w3.org/TR/css3-fonts/#font-size-prop)
:   Working Draft

[CSS Values and Units Module Level 3](http://www.w3.org/TR/css3-values/)
:   Candidate Recommendation

[Cascading Style Sheets Level 2 Revision 1 (CSS 2.1) Specification](http://www.w3.org/TR/CSS2/)
:   W3C Recommendation

## See also

### Related articles

#### CSS Font

-   [font-family](/css/properties/font-family)

-   [font-kerning](/css/properties/font-kerning)

-   [font-language-override](/css/properties/font-language-override)

-   **font-size**

-   [font-size-adjust](/css/properties/font-size-adjust)

-   [font-style](/css/properties/font-style)

-   [font-synthesis](/css/properties/font-synthesis)

-   [font-variant](/css/properties/font-variant)

-   [kerning-mode](/css/properties/kerning-mode)

-   [kerning-pair-threshold](/css/properties/kerning-pair-threshold)

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

-   **font-size**

-   [font-size-adjust](/css/properties/font-size-adjust)

-   [font-stretch](/css/properties/font-stretch)

-   [font-style](/css/properties/font-style)

-   [font-synthesis](/css/properties/font-synthesis)

-   [font-variant](/css/properties/font-variant)

-   [max-font-size](/css/properties/max-font-size)

-   [min-font-size](/css/properties/min-font-size)

-   [user-modify](/css/properties/user-modify)

-   [size](/html/attributes/size)

-   [font](/html/elements/font)

#### Text

-   [block-progression](/css/properties/block-progression)

-   [font-language-override](/css/properties/font-language-override)

-   **font-size**

-   [font-synthesis](/css/properties/font-synthesis)

-   [hanging-punctuation](/css/properties/hanging-punctuation)

-   [hyphenate-limit-chars](/css/properties/hyphenate-limit-chars)

-   [hyphenate-limit-lines](/css/properties/hyphenate-limit-lines)

-   [hyphenate-limit-zone](/css/properties/hyphenate-limit-zone)

-   [hyphens](/css/properties/hyphens)

-   [ime-mode](/css/properties/ime-mode)

-   [layout-flow](/css/properties/layout-flow)

-   [layout-grid](/css/properties/layout-grid)

-   [layout-grid-char](/css/properties/layout-grid-char)

-   [layout-grid-line](/css/properties/layout-grid-line)

-   [layout-grid-mode](/css/properties/layout-grid-mode)

-   [layout-grid-type](/css/properties/layout-grid-type)

-   [letter-spacing](/css/properties/letter-spacing)

-   [line-break](/css/properties/line-break)

-   [max-font-size](/css/properties/max-font-size)

-   [min-font-size](/css/properties/min-font-size)

-   [text-overflow-ellipsis](/css/properties/text-overflow-ellipsis)

-   [text-overflow-mode](/css/properties/text-overflow-mode)

-   [text-rendering](/css/properties/text-rendering)

-   [text-underline-position](/css/properties/text-underline-position)

-   [text-underline-style](/css/properties/text-underline-style)

-   [text-underline-width](/css/properties/text-underline-width)

-   [user-input](/css/properties/user-input)

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

### Other articles

-   [CSS text styling fundamentals](/guides/css_text_styling_fundamentals)

### External resources

-   Smashing: [16 Pixels: For Body Copy. Anything Less Is a Costly Mistake](http://www.smashingmagazine.com/2011/10/07/16-pixels-body-copy-anything-less-costly-mistake)
-   HTML5 Boilerplate: [Reasoning behind default font-size and line-height](https://github.com/h5bp/html5-boilerplate/issues/724)
-   A List Apart: [How to Size Text in CSS](http://www.alistapart.com/articles/howtosizetextincss)
-   Mozilla: [default style sheet](http://mxr.mozilla.org/mozilla/source/layout/style/html.css)
-   WebKit: [default style sheet](http://trac.webkit.org/browser/trunk/Source/WebCore/css/html.css)
-   CSS-Tricks: [Font size keywords](http://css-tricks.com/css-font-size/)
-   MDN: [font-size](https://developer.mozilla.org/en-US/docs/Web/CSS/font-size)
