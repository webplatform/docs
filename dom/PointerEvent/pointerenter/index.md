---
title: pointerenter
attributions:
  - 'Microsoft Developer Network: [[pointerenter Event](http://msdn.microsoft.com/en-us/library/ie/dn254944(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Dispatched when a pointing device is moved into the hit test boundaries of an element or one of its descendants, including as a result of a pointerdown event from a device that does not support hover.'
tags:
  - Events
  - DOM
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/objects/PointerEvent/pointerleave
uri: dom/PointerEvent/pointerenter

---
## <span>Summary</span>

Dispatched when a pointing device is moved into the hit test boundaries of an element or one of its descendants, including as a result of a pointerdown event from a device that does not support hover.

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
Varies: when the pointer is primary, all default actions of the [mouseenter](/dom/MouseEvent/mouseenter) event.

</td>
</tr>
</table>
This event type is similar to [pointerover](/dom/PointerEvent/pointerover), but differs in that it does not bubble.

## <span>Examples</span>

``` js
element.addEventListener("pointerenter", handler, useCapture) ;
```

## <span>Notes</span>

There are similarities between this event type, the [mouseenter](/dom/MouseEvent/mouseenter) event described in [DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/) and the CSS :hover pseudo-class described in [CSS 2.1](http://www.w3.org/TR/CSS2/). See also the [pointerleave](/w/index.php?title=dom/objects/PointerEvent/pointerleave&action=edit&redlink=1) event.

## <span>Related specifications</span>

[Pointer Events](http://www.w3.org/TR/pointerevents)
:   Working Draft
