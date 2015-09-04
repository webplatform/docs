---
title: text-overflow-ellipsis
tags:
  - CSS
  - Properties
readiness: 'Not Ready'
standardization_status: Non-Standard
notes:
  - 'Non-standard; deletion candidate'
summary: 'The text-overflow-ellipsis CSS property controls how the hint on overflowed content that is not displayed is signaled to the users. The presence of the hint is controlled with CSS property text-overflow-mode. Shorthand property is text-overflow.'
code_samples:
  - 'http://dabblet.com/gist/4744982'
uri: css/properties/text-overflow-ellipsis

---
# text-overflow-ellipsis

## Summary

The text-overflow-ellipsis CSS property controls how the hint on overflowed content that is not displayed is signaled to the users. The presence of the hint is controlled with CSS property text-overflow-mode. Shorthand property is text-overflow.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `U+2026`
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
:   `text-overflow-ellipsis`
Percentages
:   N/A

## Syntax

-   `text-overflow-ellipsis: string`

## Values

string
:   The value is defined either as a string like the default UTF-8 character 'U+2026' or a URI and represents the ellipsis of text-overflow-mode property. If the value is defined as a URI it displays the image behind the URL. You can also set both values which then means they determine the overflow visual hint at the end and the hint after the element box. The latter visual hint is only displayed if there is clipped content because of the dimension limitation on the element block.

## Examples

``` {.html}
<!-- example showing text-overflow-ellipsis property -->

<div class="overflowed overflowed-ellipsis">
    <p>This is an example text showing nothing interesting but the truncated content via text-overflow shorthand property.</p>
</div>
<div class="overflowed overflowed-ellipsis-word">
    <p>This is an example text showing nothing interesting but the truncated content via text-overflow shorthand property.</p>
</div>
```

[View live example](http://dabblet.com/gist/4744982)

``` {.css}
.overflowed > p {
    width: 10em;
    height: 5em;
    white-space: nowrap;
    overflow: hidden;
}

.overflowed-ellipsis > p {
    text-overflow-mode: ellipsis;
    text-overflow-ellipsis: '[more]';
}

.overflowed-ellipsis-word > p {
    text-overflow-mode: ellipsis-word;
    text-overflow-ellipsis: '[more]';
}
```

[View live example](http://dabblet.com/gist/4744982)

## Usage

     Currently it is not widely supported in any major browsers.

## Notes

Because the initial value (U+2026) of the overflow visual hint after the element box may not be easily rendered in some situations, the user agent may replace it by a sequence of 3 FULL STOP characters (U+002E).

## See also

### Related articles

#### CSS Attributes

-   [background-blend-mode](/css/properties/background-blend-mode)

-   [background-position](/css/properties/background-position)

-   [break-before](/css/properties/break-before)

-   [height](/css/properties/height)

-   [list-style](/css/properties/list-style)

-   [list-style-position](/css/properties/list-style-position)

-   **text-overflow-ellipsis**

-   [text-overflow-mode](/css/properties/text-overflow-mode)

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

-   **text-overflow-ellipsis**

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

