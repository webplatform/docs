---
title: mouseover
tags:
  - Events
  - DOM
readiness: 'Ready to Use'
summary: 'Fires when the user moves the mouse pointer into the object.'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onmouseoverEX.htm'
uri: dom/MouseEvent/mouseover

---
# mouseover

## Summary

Fires when the user moves the mouse pointer into the object.

## Overview Table

Synchronous
:   No
Bubbles
:   Yes
Target
:   dom/Element
Cancelable
:   Yes
Default action
:   none

## Examples

This example uses the **onmouseover** event to apply a new style to an object.

    <p
        onmouseover="this.style.color='red'"
        onmouseout="this.style.color='black'">
            Move the mouse pointer over this text to change its color. Move the pointer off the text
            to change the color back.
    </p>

This example shows how to change the value of a text area in response to mouse events.

    <p>Move the mouse pointer into the text area to fire the onmouseover event. Move
    it out to clear the text.
    <textarea name="txtMouseTrack"
        onmouseover="this.value='onmouseover fired'"
        onmouseout="this.value=">
    </textarea></p>

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

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[mouseover event](https://developer.mozilla.org/en-US/docs/Web/Events/mouseover) Article]

Portions of this content come from the Microsoft Developer Network: [[mouseover event](http://msdn.microsoft.com/en-us/library/ie/ms536949(v=vs.85).aspx) Article]

Portions of this content come from HTML5Rocks! [[mouseover event samples](http://www.html5rocks.com/en/search?q=mouseover+event) article]

