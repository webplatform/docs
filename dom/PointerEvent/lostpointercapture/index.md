---
title: lostpointercapture
tags:
  - Events
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs example'
summary: 'Dispatched after pointer capture is released for a pointer.'
uri: dom/PointerEvent/lostpointercapture

---
# lostpointercapture

## Summary

Dispatched after pointer capture is released for a pointer.

## Overview Table

Synchronous
:   No
Bubbles
:   Yes
Target
:   dom/Element
Cancelable
:   No
Default action
:   None

This event is dispatched prior to any subsequent events for the pointer after capture was released. This event is dispatched to the element from which pointer capture was removed. Subsequent events for that pointer follow normal hit testing mechanisms for determining the event target. See [releasePointerCapture](/dom/Element/releasePointerCapture).

**Needs Examples**: This section should include examples.

## Notes

Note As of Internet Explorer 11, the Microsoft vendor prefixed version of this event (MSLostPointerCapture) is no longer supported and may be removed in a future release. Instead, use the non-prefixed lowercase name, lostpointercapture, which is better for standards compliance and future compatibility.

## Related specifications

Specification
:   Status
[Pointer Events](http://www.w3.org/TR/pointerevents)
:   Working Draft

## See also

### Other articles

[code.MSDN Pointers and Gestures Example](http://code.msdn.microsoft.com/ie/Pointers-and-Gestures-ae95918f)

[Feature Detection and Touch Support Testing](http://msdn.microsoft.com/en-us/library/ie/dn433244(v=vs.85).aspx#feature_detection_and_touch_support_testing)

[Hand.js - A polyfill for supporting pointer events on every browser.](http://blogs.msdn.com/b/eternalcoding/archive/2013/01/16/hand-js-a-polyfill-for-supporting-pointer-events-on-every-browser.aspx)

[PointerEvents Polyfill on Github](https://github.com/toolkitchen/PointerEvents)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[lostPointerCapture Event](http://msdn.microsoft.com/en-us/library/ie/hh771907(v=vs.85).aspx) Article]

