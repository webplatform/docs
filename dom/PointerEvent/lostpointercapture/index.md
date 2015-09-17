---
title: 'lostpointercapture'
attributions:
  - 'Microsoft Developer Network: [[lostPointerCapture Event](http://msdn.microsoft.com/en-us/library/ie/hh771907(v=vs.85).aspx) Article]'
notes:
  - 'Needs example'
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
summary: 'Dispatched after pointer capture is released for a pointer.'
tags:
  - Events
  - DOM
  - Needs_Examples
uri: dom/PointerEvent/lostpointercapture

---
## Summary

Dispatched after pointer capture is released for a pointer.

## Overview Table

<table class="wikitable">
<tr>
<th>
Synchronous

</th>
<td>
No

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
No

</td>
</tr>
<tr>
<th>
Default action

</th>
<td>
None

</td>
</tr>
</table>
This event is dispatched prior to any subsequent events for the pointer after capture was released. This event is dispatched to the element from which pointer capture was removed. Subsequent events for that pointer follow normal hit testing mechanisms for determining the event target. See [releasePointerCapture](/dom/Element/releasePointerCapture).

## Notes

Note As of Internet Explorer 11, the Microsoft vendor prefixed version of this event (MSLostPointerCapture) is no longer supported and may be removed in a future release. Instead, use the non-prefixed lowercase name, lostpointercapture, which is better for standards compliance and future compatibility.

## Related specifications

[Pointer Events](http://www.w3.org/TR/pointerevents)
:   Working Draft

## See also

### Other articles

[code.MSDN Pointers and Gestures Example](http://code.msdn.microsoft.com/ie/Pointers-and-Gestures-ae95918f)

[Feature Detection and Touch Support Testing](http://msdn.microsoft.com/en-us/library/ie/dn433244(v=vs.85).aspx#feature_detection_and_touch_support_testing)

[Hand.js - A polyfill for supporting pointer events on every browser.](http://blogs.msdn.com/b/eternalcoding/archive/2013/01/16/hand-js-a-polyfill-for-supporting-pointer-events-on-every-browser.aspx)

[PointerEvents Polyfill on Github](https://github.com/toolkitchen/PointerEvents)
