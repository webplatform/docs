---
title: text-overflow
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](http://dev.w3.org/csswg/css3-ui/#text-overflow)'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://dabblet.com/gist/4744956'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`not defined for shorthand properties`'
  'Applies to': 'block-level and inline-block elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'see individual properties'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`<''text-overflow-mode''>`'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The text-overflow shorthand CSS property determines how overflowed content that is not displayed is signaled to the users. It can be clipped, display an ellipsis (''…'', U+2026 HORIZONTAL ELLIPSIS) or a Web author-defined string. It covers the two long-hand properties text-overflow-mode and text-overflow-ellipsis'
tags:
  - CSS
  - Properties
uri: css/properties/text-overflow

---
## Summary

The text-overflow shorthand CSS property determines how overflowed content that is not displayed is signaled to the users. It can be clipped, display an ellipsis ('…', U+2026 HORIZONTAL ELLIPSIS) or a Web author-defined string. It covers the two long-hand properties text-overflow-mode and text-overflow-ellipsis

## Overview table

[Initial value](/css/concepts/initial_value)
:   `not defined for shorthand properties`

Applies to
:   block-level and inline-block elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   see individual properties

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `<'text-overflow-mode'>`

## Syntax

-   `text-overflow: clip`
-   `text-overflow: ellipsis`
-   `text-overflow: ellipsis-word`

## Values

clip
:   Default. Simply clips the content and does not display ellipsis for text-overflow.

ellipsis
:   Display ellipsis (...) for text overflow after the last letter that entirely fits into a line.

ellipsis-word
:   Display ellipsis (...) for text overflow after the last word that entirely fits into a line.

## Examples

The following example shows how to use **ellipsis**, **ellipsis-word** and **clip** values for the **text-overflow** property.

``` html
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

[View live example](http://dabblet.com/gist/4744956)

``` css
.overflowed > p{
    width: 10em;
    height: 5em;
    white-space: nowrap;
    overflow: hidden;
}

.overflowed-clip {
    text-overflow: clip;
}

.overflowed-ellipsis > p {
    text-overflow: ellipsis;
}

.overflowed-ellipsis-word > p {
    text-overflow: ellipsis-word;
}
```

[View live example](http://dabblet.com/gist/4744956)

## Notes

### Remarks

This property only applies to text overflow in the inline direction (horizontal, in normal Western text). Inline overflow occurs when the text in a line overflows the available width without a breaking opportunity. To force overflow to occur and ellipses to be applied, the author must apply the *nowrap* value to the [**white-space**](/css/properties/white-space) property on the element, or wrap the content in a \<NOBR\> tag. If there is no breaking opportunity (for example, the width is narrow or there is a long word that does not break well), then overflow may occur without *nowrap* being applied. This property on the element must be set to something other than *visible*, the default, in order for ellipses to be rendered. The best choice is to set [**overflow**](/css/properties/overflow) to *hidden*. Setting **overflow** to *scroll* or *auto* will also work, but will show scrollbars. The hidden text can be selected by selecting the ellipses. When selected, the ellipses will disappear and be replaced by the text to the extent of the layout area. This property offers an efficient alternative to building ellipses in Dynamic HTML (DHTML). As ellipses may be rendered many times on a single page, using this property can significantly speed up performance.

### Syntax

`text-overflow: ellipsis | clip`

## See also

### Related pages

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `runtimeStyle`
-   `style`
