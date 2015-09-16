---
title: pointerup
attributions:
  - 'Microsoft Developer Network: [[pointerup Event](http://msdn.microsoft.com/en-us/library/ie/hh771914(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Dispatched when a pointer leaves the state of having a non-zero value for the buttons property.'
tags:
  - Events
  - DOM
uri: dom/PointerEvent/pointerup

---
## Summary

Dispatched when a pointer leaves the state of having a non-zero value for the buttons property.

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
Varies: when the pointer is primary, all default actions of the [mouseup](/dom/MouseEvent/mouseup) event

</td>
</tr>
</table>
For mouse, this is when the device transitions from at least one button depressed to no buttons depressed. For touch, this is when physical contact is removed from the digitizer. For pen, this is when the pen is removed from physical contact with the digitizer.

For input devices that do not support hover, a user agent must also fire a pointerout event after firing the pointerup event.

## Examples

``` js
element.addEventListener("pointerup", handler, useCapture) ;
```

## Notes

Some pointer devices, such as mouse or pen, support multiple buttons. In the [DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/) Mouse Event model, each button press produces a mousedown and mouseup event.

Pointer Events do not fire overlapping pointerdown and pointerup events when an additional button is depressed while another button on the pointer device is already depressed. For detecting these cases, see [Chorded Button Interactions](http://www.w3.org/TR/pointerevents/#chorded-button-interactions) in the PointerEvents specification.

## Related specifications

[Pointer Events](http://www.w3.org/TR/pointerevents)
:   Working Draft
