---
title: baseline-shift
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs parent, example'
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
summary: 'The ‘baseline-shift’ property allows repositioning of the dominant-baseline( a baseline-table and a baseline-table font-size which are those of the nearest block-level ancestor element and are applied to its root inline box.) relative to the dominant-baseline.'
tags:
  - Markup
  - Attributes
  - DOM
  - SVG
uri: svg/attributes/baseline-shift

---
## <span>Summary</span>

The ‘baseline-shift’ property allows repositioning of the dominant-baseline( a baseline-table and a baseline-table font-size which are those of the nearest block-level ancestor element and are applied to its root inline box.) relative to the dominant-baseline.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
 ?

</td>
</tr>
</table>
Name: baseline-shift Value: baseline

**Needs Examples**: This section should include examples.

## <span>Notes</span>

### <span>Remarks</span>

The **baseline-shift** property allows repositioning of the dominant baseline relative to the dominant baseline of the parent text content element. The shifted object might be a subscript or superscript. Within the shifted object, the whole baseline table is offset; not just a single baseline. The amount of the shift is determined by one of the following:

-   the parent text content element
-   the subscript or superscript offset from the nominal font of the parent text content element
-   the percent of the **line-height** of the parent text content element
-   an absolute value.

### <span>Syntax</span>

    baseline-shift: baseline | sub | super | percentage | length

### <span>Standards information</span>

-   [Scalable Vector Graphics: Text](http://go.microsoft.com/fwlink/p/?linkid=199818), Section 10.9.2

## <span>Related specifications</span>

[Scalable Vector Graphics (SVG) 1.1](http://www.w3.org/TR/SVG/text.html#BaselineShiftProperty)
:   W3C Recommendation

## <span>See also</span>

### <span>Related articles</span>

#### <span>CSS Layout</span>

-   [Responsive Web Design](/concepts/mobile_web/responsive_design)

-   [@import](/css/atrules/@import)

-   [align-self](/css/properties/align-self)

-   [background](/css/properties/background)

-   [box-decoration-break](/css/properties/box-decoration-break)

-   [box-flex](/css/properties/box-flex)

-   [box-lines](/css/properties/box-lines)

-   [box-orient](/css/properties/box-orient)

-   [box-pack](/css/properties/box-pack)

-   [box-shadow](/css/properties/box-shadow)

-   [break-before](/css/properties/break-before)

-   [flex-align](/css/properties/flex-align)

-   [flex-item-align](/css/properties/flex-item-align)

-   [flex-line-pack](/css/properties/flex-line-pack)

-   [grid-auto-rows](/css/properties/grid-auto-rows)

-   [grid-definition-columns](/css/properties/grid-definition-columns)

-   [grid-definition-rows](/css/properties/grid-definition-rows)

-   [height](/css/properties/height)

-   [max-width](/css/properties/max-width)

-   [user-modify](/css/properties/user-modify)

-   **baseline-shift**

#### <span>CSS Attributes</span>

-   [background-blend-mode](/css/properties/background-blend-mode)

-   [background-position](/css/properties/background-position)

-   [break-before](/css/properties/break-before)

-   [height](/css/properties/height)

-   [list-style](/css/properties/list-style)

-   [list-style-position](/css/properties/list-style-position)

-   [text-overflow-ellipsis](/css/properties/text-overflow-ellipsis)

-   [text-overflow-mode](/css/properties/text-overflow-mode)

-   [text-rendering](/css/properties/text-rendering)

-   [user-select](/css/properties/user-select)

-   [equality](/css/selectors/attributes/equality)

-   [Attribute selector](/css/selectors/attributes/existence)

-   [hyphen](/css/selectors/attributes/hyphen)

-   [prefix](/css/selectors/attributes/prefix)

-   [substring](/css/selectors/attributes/substring)

-   [suffix](/css/selectors/attributes/suffix)

-   **baseline-shift**

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

### <span>Related pages (MSDN)</span>

-   [**CSSStyleDeclaration**](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   [**currentStyle**](/css/cssom/currentStyle)
-   [**style**](/css/cssom/style)
-   [**SVGTSpanElement**](/svg/elements/tspan)
-   [**SVGTextPathElement**](/svg/elements/textPath)
-   [**dominantBaseline**](/svg/attributes/dominant-baseline)
