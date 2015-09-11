---
title: mouseenter
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[mouseenter event](https://developer.mozilla.org/en-US/docs/Web/Events/mouseenter) Article]'
  - 'Microsoft Developer Network: [[mouseenter event](http://msdn.microsoft.com/en-us/library/ie/ms536945(v=vs.85).aspx) Article]'
code_samples:
  - 'http://result.dabblet.com/gist/acdd7a0b0ebdfaf3699d/a7e519705e7c6bf677b92d98ceaeb513ff37425a'
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onmouseoverEX.htm'
readiness: 'Ready to Use'
summary: 'Fires when the user moves the mouse pointer into the object.'
tags:
  - Events
uri: dom/MouseEvent/mouseenter

---
## <span>Summary</span>

Fires when the user moves the mouse pointer into the object.

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
none

</td>
</tr>
</table>
## <span>Examples</span>

The event handler bigImg() is triggered when the user moves the mouse pointer over the image. The event handler normalImg() is triggered when the mouse pointer is moved out of the image.

``` js
function bigImg(evt){
if(!evt)evt=window.event;
var el=(evt.target)?evt.target:evt.srcElement;
el.style.height="64px";
el.style.width="64px";
}
function normalImg(evt){
if(!evt)evt=window.event;
var el=(evt.target)?evt.target:evt.srcElement;
el.style.height="32px";el.style.width="32px";
}
if(window.addEventListener){
document.getElementById('imgSmiley').addEventListener('mouseover',bigImg,false);
document.getElementById('imgSmiley').addEventListener('mouseout',normalImg,false);
}
else{
document.getElementById('imgSmiley').attachEvent('onmouseover',bigImg);
document.getElementById('imgSmiley').attachEvent('onmouseout',normalImg);
}
```

[View live example](http://result.dabblet.com/gist/acdd7a0b0ebdfaf3699d/a7e519705e7c6bf677b92d98ceaeb513ff37425a)

MSDN Example using the mouseover event attribute.

``` html
<p>
    onmouseover="this.style.color='red'"
    onmouseout="this.style.color='black'">
        Move the mouse pointer over this text to change its color. Move the pointer off the text
        to change the color back.
</p>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onmouseoverEX.htm)

## <span>Usage</span>

     Use to perform an action when the mouse cursor is moved over an element.

Alternatively, for CSS2 compliant userAgents use the :hover pseudo class.

## <span>Notes</span>

### <span>Remarks</span>

The event fires only if the mouse pointer is outside the boundaries of the object and the user moves the mouse pointer inside the boundaries of the object. If the mouse pointer is currently inside the boundaries of the object, for the event to fire, the user must move the mouse pointer outside the boundaries of the object and then back inside the boundaries of the object. Unlike the [**onmouseover**](/dom/MouseEvent/mouseover) event, the **onmouseenter** event does not bubble. In other words, the **onmouseenter** event does not fire when the user moves the mouse pointer over elements contained by the object, whereas **onmouseover** does fire. Initiates any action associated with this event. To invoke this event, do one of the following:

-   Move the mouse pointer inside the boundaries of an object.

The *pEvtObj* parameter is required for the following interfaces:

-   **HTMLAnchorEvents2**
-   **HTMLAreaEvents2**
-   **HTMLButtonElementEvents2**
-   **HTMLControlElementEvents2**
-   **HTMLDocumentEvents2**
-   **HTMLElementEvents2**
-   **HTMLFormElementEvents2**
-   **HTMLImgEvents2**
-   **HTMLFrameSiteEvents2**
-   **HTMLInputFileElementEvents2**
-   **HTMLInputImageEvents2**
-   **HTMLInputTextElementEvents2**
-   **HTMLLabelEvents2**
-   **HTMLLinkElementEvents2**
-   **HTMLMapEvents2**
-   **HTMLMarqueeElementEvents2**
-   **HTMLObjectElementEvents2**
-   **HTMLOptionButtonElementEvents2**
-   **HTMLScriptEvents2**
-   **HTMLSelectElementEvents2**
-   **HTMLStyleElementEvents2**
-   **HTMLTableEvents2**
-   **HTMLTextContainerEvents2**
-   **HTMLWindowEvents2**

### <span>Syntax</span>

### <span>Standards information</span>

There are no standards that apply here.

### <span>Event handler parameters</span>

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

