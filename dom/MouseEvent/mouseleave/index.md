---
title: mouseleave
tags:
  - Events
readiness: 'Ready to Use'
summary: 'Fires when the user moves the mouse pointer outside the boundaries of the object.'
code_samples:
  - 'http://result.dabblet.com/gist/eaba649bc760d5831769/40c8a5bde01f6ac7896353103b65313d550aed40'
uri: dom/MouseEvent/mouseleave

---
# mouseleave

## Summary

Fires when the user moves the mouse pointer outside the boundaries of the object.

## Overview Table

Synchronous
:   No
Bubbles
:   No
Target
:   dom/Element
Cancelable
:   No
Default action
:   none

## Examples

The following example illustrates the difference between mouseout and mouseleave events.

``` {.js}
var el = document.getElementById("test");
  function domouseleave(evt){
  if(!evt)evt=window.event;
  var el=(evt.target)?evt.target:evt.srcElement;
  el.style.color='purple';
  setTimeout(function(){
    el.style.color=;
    },500);
  }
  function domouseout(evt){
  if(!evt)evt=window.event;
  var el=(evt.target)?evt.target:evt.srcElement;
  el.style.color='orange';
  setTimeout(function(){
    el.style.color=;
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

## Usage

     Could be used, for example to play a sound as the user hovers over a menu list.

## Notes

### Remarks

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

### Syntax

### Standards information

There are no standards that apply here.

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[mouseleave event](https://developer.mozilla.org/en-US/docs/Web/Events/mouseleave) Article]

Portions of this content come from the Microsoft Developer Network: [[mouseleave event](http://msdn.microsoft.com/en-us/library/ie/ms536946(v=vs.85).aspx) Article]

