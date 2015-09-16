---
title: 'mousedown'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[mousedown](https://developer.mozilla.org/en-US/docs/Web/Events/mousedown) Article]'
  - 'Microsoft Developer Network: [[event.mousedown](http://msdn.microsoft.com/en-us/library/ie/ms536944(v=vs.85).aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onmousedownEX.htm'
readiness: 'Ready to Use'
summary: 'Fires when the user clicks the object with either mouse button or taps the mouse pad.'
tags:
  - Events
uri: dom/MouseEvent/mousedown

---
## Summary

Fires when the user clicks the object with either mouse button or taps the mouse pad.

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
 ?

</td>
</tr>
</table>
## Examples

This example shows how to determine the origin of the **onmousedown** event when event bubbling is used.

``` html
<body onmousedown="(event.target)?alert(event.target.tagName):alert(event.srcElement.tagName);">
<table style="table-layout:fixed; cell-collapse:collapse">
<tr>
  <th>Click the items below with your mouse.</th>
</tr>
  <tr><td><button type="button">Click Me</button></td></tr>
  <tr><td><input type="text" value="Click Me"/></td></tr>
  <tr><td>Click Me</td></tr>
</table>
<p>This code retrieves the tagName of the object on which
   the onmousedown event has fired.</p>
</body>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onmousedownEX.htm)

## Usage

     Determine the properties of the DOM element that a user clicks on.

## Notes

### Remarks

Use the **button** property to determine which mouse button is clicked. Initiates actions associated with the event and with the object being clicked. To invoke this event, do one of the following:

-   Click a mouse button.

### Syntax

### Standards information

-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 18.2.3

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

