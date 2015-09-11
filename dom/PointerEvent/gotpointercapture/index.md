---
title: gotpointercapture
attributions:
  - 'Microsoft Developer Network: [[gotpointercapture Event](http://msdn.microsoft.com/en-us/library/ie/hh771904(v=vs.85).aspx) Article]'
  - 'Portions of this content come from HTML5Rocks! [[Using touch and mouse](http://www.html5rocks.com/en/mobile/touchandmouse/) article]'
notes:
  - "example required\nunsure about CSS DOM values\n-ms-touch-action:none;\n\ntouch-action:none;"
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
summary: 'Dispatched prior to the dispatch of the first event after pointer capture is set for a pointer. See the PointerEvent object.'
tags:
  - Events
  - DOM
uri: dom/PointerEvent/gotpointercapture

---
## <span>Summary</span>

Dispatched prior to the dispatch of the first event after pointer capture is set for a pointer. See the PointerEvent object.

## <span>Overview Table</span>

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
This event is dispatched to the element that is receiving pointer capture. Subsequent events for that pointer will be dispatched to this element. See [setPointerCapture](/dom/Element/setPointerCapture).

**Needs Examples**: This section should include examples.

## <span>Related specifications</span>

[Pointer Events](http://www.w3.org/TR/pointerevents)
:   Working Draft

## <span>See also</span>

### <span>Other articles</span>

[code.MSDN Pointers and Gestures Example](http://code.msdn.microsoft.com/ie/Pointers-and-Gestures-ae95918f)

[Feature Detection and Touch Support Testing](http://msdn.microsoft.com/en-us/library/ie/dn433244(v=vs.85).aspx#feature_detection_and_touch_support_testing)

[Hand.js - A polyfill for supporting pointer events on every browser.](http://blogs.msdn.com/b/eternalcoding/archive/2013/01/16/hand-js-a-polyfill-for-supporting-pointer-events-on-every-browser.aspx)

[PointerEvents Polyfill on Github](https://github.com/toolkitchen/PointerEvents)