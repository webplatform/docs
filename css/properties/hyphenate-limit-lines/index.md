---
title: hyphenate-limit-lines
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Add description, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`no-limit`'
  'Applies to': 'block containers'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'specified value'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`hyphenateLimitLines`'
  Percentages: N/A
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
summary: 'Indicates the maximum number of successive hyphenated lines in an element. The ‘no-limit’ value means that there is no limit.'
tags:
  - CSS
  - Properties
uri: css/properties/hyphenate-limit-lines

---
## <span>Summary</span>

Indicates the maximum number of successive hyphenated lines in an element. The ‘no-limit’ value means that there is no limit.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `no-limit`

Applies to
:   block containers

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   specified value

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `hyphenateLimitLines`

Percentages
:   N/A

## <span>Syntax</span>

-   `hyphenate-limit-lines: integer`
-   `hyphenate-limit-lines: no-limit`

## <span>Values</span>

no-limit
:   Indicates that hyphenation is not limited based on the number of consecutive hyphenated lines. In the flow above the consecutive hyphenated lines limit would be an infinitely large positive number.

[integer](/css/data_types/integer)
:   Indicates the maximum number of successive hyphenated lines.

For instance, if `2`, then no more than 2 successive lines may end with a hyphenated word. If `0` then no lines may end with a hyphenated word. (Hyphenation is effectively disabled.)

Negative values are not allowed.

## <span>Examples</span>

``` css
/* Do not allow more than 2 successive hyphenated lines */
hyphenate-limit-lines: 2;
```

## <span>Related specifications</span>

[CSS Text Level 4](http://dev.w3.org/csswg/css-text-4/#hyphenate-line-limits)
:   W3C Editor’s Draft

## <span>See also</span>

### <span>Related articles</span>

#### <span>Text</span>

-   [block-progression](/css/properties/block-progression)

-   [font-language-override](/css/properties/font-language-override)

-   [font-size](/css/properties/font-size)

-   [hyphenate-limit-chars](/css/properties/hyphenate-limit-chars)

-   **hyphenate-limit-lines**

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

### <span>Related pages (MSDN)</span>

-   `CSSStyleDeclaration`
