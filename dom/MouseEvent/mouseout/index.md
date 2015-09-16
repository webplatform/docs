---
title: 'mouseout'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[mouseout event](https://developer.mozilla.org/en-US/docs/Web/Events/mouseout) Article]'
  - 'Microsoft Developer Network: [[mouseout event](http://msdn.microsoft.com/en-us/library/ie/ms536948(v=vs.85).aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onmouseoutEX.htm'
readiness: 'Ready to Use'
summary: 'Fires when the user moves the mouse pointer outside the boundaries of the object.'
tags:
  - Events
  - DOM
uri: dom/MouseEvent/mouseout

---
## Summary

Fires when the user moves the mouse pointer outside the boundaries of the object.

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

This example uses the **onmouseout** event to apply a new style to an object.

``` html
<body>
<p onmouseout="this.style.color='black';"
    onmouseover="this.style.color='red';">
Move the mouse pointer over this text to change its color.
Move the pointer off the text to change the color back.
</p>
</body>
```

This example shows how to swap images on mouse events.

``` html
<head>
<script type="text/javascript">
function flipImage(url)
{
    if (window.event.srcElement.tagName == "img" )
    {
        window.event.srcElement.src = url;
    }
}
</script>
</head>
<body>
<p>Move the mouse over the image to see it switch.</p>
<p>
<img src="/workshop/graphics/prop_ro.png"
    onmouseover="flipImage('/workshop/graphics/prop_rw.png');"
    onmouseout="flipImage('/workshop/graphics/prop_ro.png');">
</p>
</body>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onmouseoutEX.htm)

## Notes

### Remarks

When the user moves the mouse over an object, one [**onmouseover**](/dom/MouseEvent/mouseover) event occurs, followed by one or more [**onmousemove**](/dom/MouseEvent/mousemove) events as the user moves the mouse pointer within the object. One **onmouseout** event occurs when the user moves the mouse pointer out of the object. Initiates any action associated with this event. To invoke this event, do one of the following:

-   Move the mouse pointer out of an object.

### Syntax

### Standards information

-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 18.2.3

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****
