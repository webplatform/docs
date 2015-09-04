---
title: opacity
tags:
  - Markup
  - Attributes
  - SVG
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs parent'
summary: 'The opacity attribute specifies the transparency of an object or of a group of objects.'
uri: svg/attributes/opacity

---
# opacity

## Summary

The opacity attribute specifies the transparency of an object or of a group of objects.

Applies to
:    ?

### Syntax

    opacity: opacity-value | inherit

**opacity-value** is a number between 0.0 (fully transparent) and 1.0 (fully opaque).

## Examples

This example shows how to draw a circle with 50% opacity.



    <svg width="400" height="400">
      <circle cx="100" cy="100" r="50" fill="tomato" opacity="0.5" />
    </svg>

</pre>

## Related specifications

Specification
:   Status
[SVG 1.1](http://www.w3.org/TR/SVG11/masking.html#OpacityProperty)
:   W3C Recommendation

