---
title: 'pointerover'
attributions:
  - 'Microsoft Developer Network: [[pointerover Event](http://msdn.microsoft.com/en-us/library/ie/hh771913(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Dispatched when a pointing device is moved into the hit test boundaries of an element. Also dispatched prior to a pointerdown event for devices that do not support hover.'
tags:
  - Events
  - DOM
uri: dom/PointerEvent/pointerover

---
## Summary

Dispatched when a pointing device is moved into the hit test boundaries of an element. Also dispatched prior to a pointerdown event for devices that do not support hover.

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
Yes

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
Varies: when the pointer is primary, all default actions of the [mouseover](/dom/MouseEvent/mouseover) event

</td>
</tr>
</table>
## Examples

``` js
element.addEventListener("pointerover", handler, useCapture);
```

## Related specifications

[Pointer Events](http://www.w3.org/TR/pointerevents)
:   Working Draft
