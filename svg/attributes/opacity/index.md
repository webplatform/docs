---
title: opacity
notes:
  - 'Needs parent'
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
summary: 'The opacity attribute specifies the transparency of an object or of a group of objects.'
tags:
  - Markup
  - Attributes
  - SVG
uri: svg/attributes/opacity

---
## Summary

The opacity attribute specifies the transparency of an object or of a group of objects.

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
### Syntax

    opacity: opacity-value | inherit

**opacity-value** is a number between 0.0 (fully transparent) and 1.0 (fully opaque).

## Examples

This example shows how to draw a circle with 50% opacity.

``` html


<svg width="400" height="400">
  <circle cx="100" cy="100" r="50" fill="tomato" opacity="0.5" />
</svg>
```

</pre>

## Related specifications

[SVG 1.1](http://www.w3.org/TR/SVG11/masking.html#OpacityProperty)
:   W3C Recommendation
