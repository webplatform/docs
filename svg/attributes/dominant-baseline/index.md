---
title: 'dominant-baseline'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: dominant-baseline
  topic: svg
notes:
  - 'Needs all content'
readiness: 'Not Ready'
tags:
  - Markup_Attributes
  - SVG
  - Needs_Summary
  - Needs_Examples
uri: svg/attributes/dominant-baseline

---
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
## Notes

### Remarks

A *scaled-baseline-table* is a compound value that has three components: a baseline identifier for the dominant baseline, a baseline table, and a baseline table font-size. Some values of the property redetermine all three values; others only re-establish the baseline table font-size. When the default value, auto, gives an undesired result, this property can be used to explicitly set the desire scaled-baseline table.

### Syntax

    dominant-baseline: auto | use-script | no-change | reset-size | ideographic | alphabetic | hanging | mathematical | central | middle | text-after-edge | text-before-edge | inherit

### Standards information

-   [Scalable Vector Graphics: Text](http://go.microsoft.com/fwlink/p/?linkid=199818), Section 10.9.2

## See also

### Related pages

-   [**CSSStyleDeclaration**](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   [**currentStyle**](/css/cssom/currentStyle)
-   [**style**](/css/cssom/style)
-   [**SVGTSpanElement**](/svg/elements/tspan)
-   [**SVGTextPathElement**](/svg/elements/textPath)
-   [**SVGTextElement**](/svg/elements/text)
-   [**baselineShift**](/svg/attributes/baseline-shift)
