---
title: 'alignment-baseline'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: alignment-baseline
  topic: svg
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Specifies how an element is aligned with respect to its parent; that is, specifies which baseline of the element is to be aligned with the corresponding baseline of the parent. Defaults to the baseline with the same name as the computed value of the alignment-baseline property.'
tags:
  - Markup_Attributes
  - CSS
  - SVG
uri: svg/attributes/alignment-baseline

---
## Summary

Specifies how an element is aligned with respect to its parent; that is, specifies which baseline of the element is to be aligned with the corresponding baseline of the parent. Defaults to the baseline with the same name as the computed value of the alignment-baseline property.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
svg/attributes

</td>
</tr>
</table>
Name: alignment-baseline Value: baseline

## Examples

Using 'middle' for both alignment-baseline and text-anchor is convenient for positioning text centered upon a spot regardless of size and length.

```
<text x="80" y="30" font-size="20"
  text-anchor="middle" alignment-baseline="middle">
    Right in the middle!
</text>
```

## Notes

### Remarks

This property specifies how an object is aligned with respect to its parent. For example, this allows alphabetic baselines in Roman text to stay aligned across font size changes. It defaults to the baseline with the same name as the computed value of the alignment-baseline property. That is, the position of "ideographic" alignment-point in the block-progression-direction is the position of the "ideographic" baseline in the baseline-table of the object being aligned. One of the characteristics of international text is that there are different baselines (different alignment points) for glyphs in different scripts. For example, in horizontal writing, ideographic scripts, such as Han Ideographs, Katakana, Hiragana, and Hangul, alignment occurs with a baseline near the bottoms of the glyphs; alphabetic based scripts, such as Latin, Cyrillic, Hebrew, Arabic, align a point that is the bottom of most glyphs, but some glyphs descend below the baseline; and Indic based scripts are aligned at a point that is near the top of the glyphs. The "EM box" is a relative measure of the height of the glyphs in the font. The "M" character fits in a box 1 EM high and 1 EM wide.

### Syntax

`alignment-baseline: auto | baseline | before-edge | text-before-edge | middle | central | after-edge | text-after-edge | ideographic | alphabetic | hanging | mathematical | inherit`

### Standards information

-   [Scalable Vector Graphics: Text](http://go.microsoft.com/fwlink/p/?linkid=199818), Section 10.9.2

## Related specifications

[SVG 1.1](http://www.w3.org/TR/SVG11/text.html)
:   W3C Recommendation

## See also

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
