---
title: mouseup
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[mouseup event](https://developer.mozilla.org/en-US/docs/Web/Events/mouseup) Article]'
  - 'Microsoft Developer Network: [[mouseup event](http://msdn.microsoft.com/en-us/library/ie/ms536950(v=vs.85).aspx) Article]'
  - 'Portions of this content come from HTML5Rocks! [[mouseup event samples](http://www.html5rocks.com/en/search?q=mouseup+event) article]'
readiness: 'Ready to Use'
summary: 'Fires when the user releases a mouse button while the mouse is over the object.'
tags:
  - Events
  - DOM
uri: dom/MouseEvent/mouseup

---
## Summary

Fires when the user releases a mouse button while the mouse is over the object.

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
Yes

</td>
</tr>
<tr>
<th>
Default action

</th>
<td>
Invoke a context menu (in combination with the right mouse button, if supported)

</td>
</tr>
</table>
**Needs Examples**: This section should include examples.

## Notes

### Remarks

Use the **button** property to determine which mouse button is pressed. Initiates any action associated with this event. To invoke this event, do one of the following:

-   Press and release a mouse button.

### Syntax

### Standards information

-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 18.2.3

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****
