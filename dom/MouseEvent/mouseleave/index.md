---
title: mouseleave
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[mouseleave event](https://developer.mozilla.org/en-US/docs/Web/Events/mouseleave) Article]'
  - 'Microsoft Developer Network: [[mouseleave event](http://msdn.microsoft.com/en-us/library/ie/ms536946(v=vs.85).aspx) Article]'
code_samples:
  - 'http://result.dabblet.com/gist/eaba649bc760d5831769/40c8a5bde01f6ac7896353103b65313d550aed40'
readiness: 'Ready to Use'
summary: 'Fires when the user moves the mouse pointer outside the boundaries of the object.'
tags:
  - Events
uri: dom/MouseEvent/mouseleave

---
## <span>Summary</span>

Fires when the user moves the mouse pointer outside the boundaries of the object.

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
## <span>Examples</span>

The following example illustrates the difference between mouseout and mouseleave events.

``` js
var el = document.getElementById("test");
  function domouseleave(evt){
  if(!evt)evt=window.event;
  var el=(evt.target)?evt.target:evt.srcElement;
  el.style.color='purple';
  setTimeout(function(){
    el.style.color='';
    },500);
  }
  function domouseout(evt){
  if(!evt)evt=window.event;
  var el=(evt.target)?evt.target:evt.srcElement;
  el.style.color='orange';
  setTimeout(function(){
    el.style.color='';
    },500);
  }
  if(el.addEventListener){
    el.addEventListener('mouseleave',domouseleave,false);
    el.addEventListener('mouseout',domouseout,false);
  }
  else{
    el.attachEvent('onmouseleave',domouseleave);
    el.attachEvent('onmouseout', domouseout);
  }
```

[View live example](http://result.dabblet.com/gist/eaba649bc760d5831769/40c8a5bde01f6ac7896353103b65313d550aed40)

## <span>Usage</span>

     Could be used, for example to play a sound as the user hovers over a menu list.

## <span>Notes</span>

### <span>Remarks</span>

The event fires only if the mouse pointer is inside the boundaries of the object and the user moves the mouse pointer outside the boundaries of the object. If the mouse pointer is currently outside the boundaries of the object, for the event to fire, the user must move the mouse pointer inside the boundaries of the object and then back outside the boundaries of the object. Initiates any action associated with this event. To invoke this event, do one of the following:

-   Move the mouse pointer outside the boundaries of an object.

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

