---
title: abort
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [abort](https://developer.mozilla.org/en-US/docs/Web/Events/abort) Article]'
  - 'Microsoft Developer Network: [[abort Event](http://msdn.microsoft.com/en-us/library/ie/ms536785(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Fires when the user aborts the download.'
tags:
  - Events
  - DOM
uri: dom/UIEvent/abort

---
## Summary

Fires when the user aborts the download.

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
Halts downloading of the designated image, but not due to an error

</td>
</tr>
</table>
## Examples

``` js
<img id="imgLogo" title="Click to view larger image" src="example.com/small.jpg" alt="small logo"/>
<script type="text/javascript">
var myAddEvent=function(el, ev, fn){
    if(el.addEventListener){
        el.addEventListener(ev, fn, false);
    }else if(el.attachEvent){
        el.attachEvent('on'+ev,fn);
    }else{
        el['on'+ ev] = fn;
    }
};
var el=document.getElementById('imgLogo');
function imgAbortHandler(evt){
// code to recover from the abort method.
}
function imgResize(evt){
document.getElementById('imgLogo').src='http://example.com/big.jpj';
document.getElementById('imgLogo').title='big logo';
}
myAddEvent(el,'click',imgResize);
myAddEvent(el,'abort',imgAbortHandler);
```

## Usage

     Used to recover the original resource if the user cancels the download.

## Notes

### Remarks

Halts downloading of the designated image, but not due to an error. To invoke this event, do one of the following:

-   Click an [**anchor**](/html/elements/a) while the document is loading.
-   Stop loading the document.
-   Navigate to another document.
-   Windows Internet Explorer 9. The client stops fetching media data, but not due to an error.

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
-   **HTMLDocumentEvents4**
-   **HTMLElementEvents4**

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 6.1.6.2

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****
