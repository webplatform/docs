---
title: error
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onerrorEX.htm'
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onerrorEX1.htm'
notes:
  - 'Needs spec reference, standardization status'
readiness: 'In Progress'
summary: 'Fires when an error occurs.'
tags:
  - Events
uri: dom/Event/error

---
## Summary

Fires when an error occurs.

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
No

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

The following examples use the **onerror** event to handle run-time script errors and object load errors.

The following example specifies an invalid script entry. The script in the text field is evaluated when the Throw Error button is clicked. The **onerror** event fires because the script is invalid. The error results are inserted at the bottom of the sample page instead of in a dialog box.

``` js
<script>
window.onerror=fnErrorTrap;
function fnErrorTrap(sMsg,sUrl,sLine){
   oErrorLog.innerHTML="<b>An error was thrown and caught.</b><br />";
   oErrorLog.innerHTML+="Error: " + sMsg + "<br />";
   oErrorLog.innerHTML+="Line: " + sLine + "<br />";
   oErrorLog.innerHTML+="URL: " + sUrl + "<br />";
   return false;
}
function fnThrow(){
   eval(oErrorCode.value);
}
</script>
<input type="text" id="oErrorCode" value="someObject.someProperty=true;"/>
<input type="button" value="Throw Error" onclick="fnThrow()"/>
<br />
<div id="oErrorLog"></div>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onerrorEX.htm)

The following example shows how to set the handler for the **onerror** event in script before an image source is specified. When the invalid source is set on the **img** element, the event fires.

``` js
<script>
var sImg='<img style="display: none;" id="oStub" alt="Default Text"/>';
function fnLoadFirst(){
   oContainer.innerHTML=sImg;
   oStub.onerror=fnLoadFail1;
   oStub.src="";
   oStub.style.display="block";
}
function fnLoadFail1(){
   oStub.alt="Image failed to load.";
   return true;
}
</script>
<input type="button" value="Load First Image" onclick="fnLoadFirst()"/>
<div id=oContainer></div>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onerrorEX1.htm)

## Notes

### Remarks

To suppress the default Windows Internet Explorer error message for the **window** event, set the [**returnValue**](/dom/BeforeUnloadEvent/returnValue) property to **true** or simply return `true` in Microsoft JScript. The **onerror** event fires for run-time errors, but not for compilation errors. In addition, error dialog boxes raised by script debuggers are not suppressed by returning `true`. To turn off script debuggers, disable script debugging in Internet Explorer by choosing **Internet Options** from the **Tools** menu. Click the **Advanced** tab and select the appropriate check box(es). Displays the browser error message when a problem occurs and executes any error handling routine associated with the event. To invoke this event, do one of the following:

-   Run-time script error, such as an invalid object reference or security violation.
-   Error while downloading an object, such as an image.
-   Windows Internet Explorer 9. An error occurs while fetching media data.

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

There are no standards that apply here.

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

