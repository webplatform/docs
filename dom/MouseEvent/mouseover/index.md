---
title: 'mouseover'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[mouseover event](https://developer.mozilla.org/en-US/docs/Web/Events/mouseover) Article]'
  - 'Microsoft Developer Network: [[mouseover event](http://msdn.microsoft.com/en-us/library/ie/ms536949(v=vs.85).aspx) Article]'
  - 'Portions of this content come from HTML5Rocks! [[mouseover event samples](http://www.html5rocks.com/en/search?q=mouseover+event) article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onmouseoverEX.htm'
readiness: 'Ready to Use'
summary: 'Fires when the user moves the mouse pointer into the object.'
tags:
  - Events
  - DOM
uri: dom/MouseEvent/mouseover

---
## Summary

Fires when the user moves the mouse pointer into the object.

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
none

</td>
</tr>
</table>
## Examples

This example uses the **onmouseover** event to apply a new style to an object.

``` html
<p
    onmouseover="this.style.color='red'"
    onmouseout="this.style.color='black'">
        Move the mouse pointer over this text to change its color. Move the pointer off the text
        to change the color back.
</p>
```

This example shows how to change the value of a text area in response to mouse events.

``` html
<p>Move the mouse pointer into the text area to fire the onmouseover event. Move
it out to clear the text.
<textarea name="txtMouseTrack"
    onmouseover="this.value='onmouseover fired'"
    onmouseout="this.value=''">
</textarea></p>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onmouseoverEX.htm)

## Notes

### Remarks

The event occurs when the user moves the mouse pointer into the object, and it does not repeat unless the user moves the mouse pointer out of the object and then back into it. Initiates any action associated with this event. To invoke this event, do one of the following:

-   Move the mouse pointer into an object.

### Syntax

### Standards information

-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 18.2.3

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****
