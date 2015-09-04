---
title: text-overflow-mode
tags:
  - CSS
  - Properties
readiness: 'Not Ready'
standardization_status: Non-Standard
notes:
  - 'Non-standard; deletion candidate'
summary: 'The text-overflow-mode CSS property controls the presence and position of the hint on overflowed content that is not displayed is signaled to the users. The constitution of the hint is controlled with CSS property text-overflow-ellipsis. Shorthand property is text-overflow.'
code_samples:
  - 'http://dabblet.com/gist/4744976'
uri: css/properties/text-overflow-mode

---
# text-overflow-mode

## Summary

The text-overflow-mode CSS property controls the presence and position of the hint on overflowed content that is not displayed is signaled to the users. The constitution of the hint is controlled with CSS property text-overflow-ellipsis. Shorthand property is text-overflow.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `clip`
Applies to
:   block-level and inline-block elements
[Inherited](/css/concepts/inherited)
:   No
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   specified value (except for initial and inherit)
Animatable
:   No
[CSS Object Model Property](/css/concepts/cssom)
:   `text-overflow-mode`

## Syntax

-   `text-overflow-mode: clip`
-   `text-overflow-mode: ellipsis`
-   `text-overflow-mode: ellipsis-word`

## Values

clip
:   Default. Simply clips the content and does not display ellipsis for text-overflow.

ellipsis
:   Display ellipsis (...) for text overflow after the last letter that entirely fits into a line.

ellipsis-word
:   Display ellipsis (...) for text overflow after the last word that entirely fits into a line.

## Examples

``` {.html}
<!-- example showing text-overflow shorthand property -->
<div class="overflowed overflowed-clip">
    <p>This is an example text showing nothing interesting but the truncated content via text-overflow shorthand property.</p>
</div>
<div class="overflowed overflowed-ellipsis">
    <p>This is an example text showing nothing interesting but the truncated content via text-overflow shorthand property.</p>
</div>
<div class="overflowed overflowed-ellipsis-word">
    <p>This is an example text showing nothing interesting but the truncated content via text-overflow shorthand property.</p>
</div>
```

[View live example](http://dabblet.com/gist/4744976)

``` {.css}
.overflowed > p{
    width: 10em;
    height: 5em;
    white-space: nowrap;
    overflow: hidden;
}

.overflowed-clip {
    text-overflow-mode: clip;
}

.overflowed-ellipsis > p {
    text-overflow-mode: ellipsis;
}

.overflowed-ellipsis-word > p {
    text-overflow-mode: ellipsis-word;
}
```

[View live example](http://dabblet.com/gist/4744976)

## Notes

This property only applies to text overflow in the inline direction (horizontal, in normal Western text). Inline overflow occurs when the text in a line overflows the available width without a breaking opportunity. To force overflow to occur and ellipses to be applied, the author must apply the nowrap value to the white-space property on the element, or wrap the content in a \<NOBR\> tag. If there is no breaking opportunity (for example, the width is narrow or there is a long word that does not break well), then overflow may occur without nowrap being applied. This property on the element must be set to something other than visible, the default, in order for ellipsis to be rendered. The best choice is to set overflow to hidden. Setting overflow to scroll or auto will also work, but will show scrollbars. The hidden text can be selected by selecting the ellipses. When selected, the ellipses will disappear and be replaced by the text to the extent of the layout area. This property offers an efficient alternative to building ellipses in Dynamic HTML (DHTML). As ellipses may be rendered many times on a single page, using this property can significantly speed up performance.

## See also

### Related articles

#### CSS Attributes

-   [background-blend-mode](/css/properties/background-blend-mode)

-   [background-position](/css/properties/background-position)

-   [break-before](/css/properties/break-before)

-   [height](/css/properties/height)

-   [list-style](/css/properties/list-style)

-   [list-style-position](/css/properties/list-style-position)

-   [text-overflow-ellipsis](/css/properties/text-overflow-ellipsis)

-   **text-overflow-mode**

-   [text-rendering](/css/properties/text-rendering)

-   [user-select](/css/properties/user-select)

-   [equality](/css/selectors/attributes/equality)

-   [Attribute selector](/css/selectors/attributes/existence)

-   [hyphen](/css/selectors/attributes/hyphen)

-   [prefix](/css/selectors/attributes/prefix)

-   [substring](/css/selectors/attributes/substring)

-   [suffix](/css/selectors/attributes/suffix)

-   [baseline-shift](/svg/attributes/baseline-shift)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

#### Text

-   [block-progression](/css/properties/block-progression)

-   [font-language-override](/css/properties/font-language-override)

-   [font-size](/css/properties/font-size)

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

-   **text-overflow-mode**

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

[http://docs.webplatform.org/wiki/css/properties/text-overflow](http://docs.webplatform.org/wiki/css/properties/text-overflow)

