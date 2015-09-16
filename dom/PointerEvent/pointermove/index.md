---
title: 'pointermove'
attributions:
  - 'Microsoft Developer Network: [[pointermove Event](http://msdn.microsoft.com/en-us/library/ie/hh771911(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Dispatched when a pointer changes coordinates, button state, pressure, tilt, or contact geometry (e.g. width and height).'
tags:
  - Events
  - DOM
uri: dom/PointerEvent/pointermove

---
## Summary

Dispatched when a pointer changes coordinates, button state, pressure, tilt, or contact geometry (e.g. width and height).

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
Varies: when the pointer is primary, all default actions of the [mousemove](/dom/MouseEvent/mousemove) event

</td>
</tr>
</table>
## Examples

``` js
element.addEventListener("pointermove", handler, useCapture) ;
```

## Related specifications

[Pointer Events](http://www.w3.org/TR/pointerevents)
:   Working Draft
