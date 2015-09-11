---
title: pointerdown
attributions:
  - 'Microsoft Developer Network: [[pointerdown Event](http://msdn.microsoft.com/en-us/library/ie/hh771909(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Dispatched when a pointer enters the state of having a non-zero value for the buttons property.'
tags:
  - Events
  - DOM
uri: dom/PointerEvent/pointerdown

---
## <span>Summary</span>

Dispatched when a pointer enters the state of having a non-zero value for the buttons property.

## <span>Overview Table</span>

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
Varies: when the pointer is primary, all default actions of the [mousedown](/dom/MouseEvent/mousedown) event

</td>
</tr>
</table>
For mouse, this is when the device has at least one button depressed. For touch, this is when there is physical contact with the digitizer. For pen, this is when the pen has physical contact with the digitizer.

For input devices that do not support hover, the user agent also fires a pointerover event preceding the pointerdown event.

## <span>Examples</span>

``` js
element.addEventListener("pointerdown", handler, useCapture)
```

## <span>Notes</span>

Some pointer devices, such as mouse or pen, support multiple buttons. In the [DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/) Mouse Event model, each button press produces a mousedown and mouseup event.

Pointer Events do not fire overlapping pointerdown and pointerup events when an additional button is depressed while another button on the pointer device is already depressed. For detecting these cases, see [Chorded Button Interactions](http://www.w3.org/TR/pointerevents/#chorded-button-interactions) in the PointerEvents specification.

## <span>Related specifications</span>

[Pointer Events](http://www.w3.org/TR/pointerevents)
:   Working Draft
