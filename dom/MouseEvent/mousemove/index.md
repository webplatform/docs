---
title: 'mousemove'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[mousemove event](https://developer.mozilla.org/en-US/docs/Web/Events/mousemove) Article]'
  - 'Microsoft Developer Network: [[mousemove event](http://msdn.microsoft.com/en-us/library/ie/ms536947(v=vs.85).aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onmousemoveEX.htm'
  - 'http://result.dabblet.com/gist/7c3297a000687b42de03/011b604311ed518c148e9d88637ae79f32e7a4f7'
readiness: 'Ready to Use'
summary: 'Fires when the user moves the mouse over the object.'
tags:
  - Events
  - DOM
uri: dom/MouseEvent/mousemove

---
## Summary

Fires when the user moves the mouse over the object.

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
none

</td>
</tr>
</table>
## Examples

This example uses the **onmousemove** event to monitor the location of the mouse cursor on the screen. When the mouse cursor moves over the **div** object, a **span** object is updated with the [**clientX**](/dom/MouseEvent/clientX) and [**clientY**](/dom/MouseEvent/clientY) property values. The **clientX** and **clientY** properties are exposed by the event object.

``` html
<script type="text/javascript">
function fnTrackMouse(){
   oNotice.innerText="Coords: (" + event.clientX + ",
      " + event.clientY + ")";
}
</script>
<div id="oScratch" onmousemove="fnTrackMouse()">
  <span id="oNotice"></span>
</div>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onmousemoveEX.htm)

Add mouse crosshairs to a web page when a checkbox is clicked.

``` js
function moveCrosshairs(evt){
         if(!evt)evt=window.event;
         var posx = 0; var posy = 0;
         if(document.documentMode&&document.documentMode>=9){
         posx+=parseInt(document.documentElement.style.marginLeft+0);
         posy+=parseInt(document.documentElement.style.marginTop+0);
         }
         if (evt.pageX
```

[View live example](http://result.dabblet.com/gist/7c3297a000687b42de03/011b604311ed518c148e9d88637ae79f32e7a4f7)

## Notes

### Remarks

If the user presses a mouse button, use the **button** property to determine which button was pressed. Initiates any action associated with this event. To invoke this event, do one of the following:

-   Move the mouse over the document.

### Syntax

### Standards information

-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 18.2.3

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****
