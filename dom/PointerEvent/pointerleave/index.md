---
title: 'pointerleave'
attributions:
  - 'Microsoft Developer Network: [[pointerleave Event](http://msdn.microsoft.com/en-us/library/ie/dn254945(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Dispatched when a pointing device is moved off of the hit test boundaries of an element and all of its descendants, including as a result of a pointerup event from a device that does not support hover.'
tags:
  - Events
  - DOM
uri: dom/PointerEvent/pointerleave

---
## Summary

Dispatched when a pointing device is moved off of the hit test boundaries of an element and all of its descendants, including as a result of a pointerup event from a device that does not support hover.

## Overview Table

<table class="wikitable">
<tr>
<th>
Synchronous

</th>
<td>
Yes

</td>
</tr>
<tr>
<th>
Bubbles

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Target

</th>
<td>
dom/Element

</td>
</tr>
<tr>
<th>
Cancelable

</th>
<td>
Yes

</td>
</tr>
<tr>
<th>
Default action

</th>
<td>
Varies: when the pointer is primary, all default actions of the [mouseleave](/dom/MouseEvent/mouseleave) event.

</td>
</tr>
</table>
This event type is similar to [pointerout](/dom/PointerEvent/pointerout), but differs in that it does not bubble and that it is not dispatched until the pointing device has left the boundaries of the element and the boundaries of all its children.

## Examples

``` js
element.addEventListener("pointerleave", handler, useCapture) ;
```

## Notes

There are similarities between this event type, the [mouseleave](/dom/MouseEvent/mouseleave) event described in [DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/) and the CSS :hover pseudo-class described in [CSS 2.1](http://www.w3.org/TR/CSS2/). See also the [pointerenter](/dom/PointerEvent/pointerenter) event.

## Related specifications

[Pointer Events](http://www.w3.org/TR/pointerevents)
:   Working Draft
