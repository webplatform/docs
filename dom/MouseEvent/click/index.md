---
title: click
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onclickEX.htm'
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onclickEX1.htm'
notes:
  - 'compatibility, clean-up of MSDN sections to fit WPD headers'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'The click event is triggered for an element when it is activated by a mouse click or by another user action that normally has the same effect as a mouse click.'
tags:
  - Events
  - DOM
uri: dom/MouseEvent/click

---
## Summary

The click event is triggered for an element when it is activated by a mouse click or by another user action that normally has the same effect as a mouse click.

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
</td>
</tr>
</table>
## Examples

This example uses the **event** object to gain information about the origin of the click. In addition, it cancels the default action to prevent navigation of [**anchor**](/html/elements/a) elements, unless the SHIFT key is pressed. Normally a Shift+Click opens the target of a link in a new window; however, the script replaces the current document by setting the [**location**](/dom/Location) of the **window** object.

``` html
<script type="text/javascript">
/* This code cancels the event. If the click occurs in an anchor
   and the SHIFT key is down, the document is navigated. */
function clickIt()
{
    var e = window.event.srcElement
    txtName.value = e.tagName;
    txtType.value = e.type;
    if ((e.tagName == "A") &&
        (window.event.shiftKey)) {
        window.location.href = e.href;
    }

    window.event.returnValue = false;
}
</script>
<body onclick="clickIt()">
<p>To follow a link, click while pressing the SHIFT key.</p>
<a href="about:blank">Click Here</a>
<textarea name="txtName"></textarea> <textarea name="txtType"></textarea>
</body>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onclickEX.htm)

This example shows how to bind the **onclick** event to grouped controls.

``` html
<head>
<script type="text/javascript">
function CookieGroup()
{
txtOutput.value = window.event.srcElement.value;
}
</script>
</head>
<body>
<!-- Controls are grouped by giving them the same NAME but unique IDs. -->
<p>Grouped Radio Buttons<br>
<input type="radio"
    name="rdoTest"
    id="Cookies"
    value="accept_cookies"
    checked
    onclick="CookieGroup()"><br>
<input type="radio"
    name="rdoTest"
    id="NoCookies"
    value="refuse_cookies"
    onclick="CookieGroup()"><br>
</p>
<p>Ungrouped Radio Button<br>
<input type="radio"
    name="rdoTest1"
    value="chocolate-chip_cookies"
    onclick="CookieGroup()"><br>
</p>
<p>Value of control on which the onclick event has fired<br>
<textarea name="txtOutput" style="width: 250px"></textarea> </p>
</body>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onclickEX1.htm)

## Notes

### Remarks

If the user clicks the left mouse button, the **onclick** event for an object occurs only if the mouse pointer is over the object and an [**onmousedown**](/dom/MouseEvent/mousedown) and an [**onmouseup**](/dom/MouseEvent/mouseup) event occur in that order. For example, if the user clicks the mouse on the object but moves the mouse pointer away from the object before releasing, no **onclick** event occurs. The **onclick** event changes the value of a control in a group. This change initiates the event for the group, not for the individual control. For example, if the user clicks a radio button or check box in a group, the **onclick** event occurs after the [**onbeforeupdate**](/dom/Event/beforeupdate) and [**onafterupdate**](/dom/Event/afterupdate) events for the control group. If the user clicks an object that can receive the input focus but does not already have the focus, the [**onfocus**](/dom/HTMLElement/focus) event occurs for that object before the **onclick** event. If the user double-clicks the left mouse button in a control, an [**ondblclick**](/dom/MouseEvent/dblclick) event occurs immediately after the **onclick** event. Although the **onclick** event is available on a large number of HTML elements, if a document is to be accessible to keyboard users, you should restrict its use to the [**a**](/html/elements/a), **input**, **area**, and **button** elements. These elements automatically allow keyboard access through the TAB key, making documents that use the elements accessible to keyboard users. For more information, please see the section on writing accessible Dynamic HTML. Initiates any action associated with the object. For example, if the user clicks an [**a**](/html/elements/a) object, the client loads the document specified by the [**href**](/html/attributes/href) property. To cancel the default behavior, set the [**returnValue**](/dom/BeforeUnloadEvent/returnValue) property to FALSE. To invoke this event, do one of the following:

-   Click the object.
-   Invoke the ****click**** method.
-   Press the ENTER key in a form.
-   Press the access key for a control.
-   Select an item in a combo box or list box by clicking the left mouse button or by pressing the arrow keys and then pressing the ENTER key.

### Compatibility

#### Internet Explorer 8 & 9

Internet Explorer 8 & 9 suffer from a bug where elements with a computed `background-color` of `transparent` that are overlaid on top of other element(s) won't receive **click** events. Any **click** events will be fired at the underlying element(s) instead. See [this live example](http://jsfiddle.net/YUKma/show/) for a demonstration.

Known workarounds for this bug:

-   For IE9 only:
    -   Set [`background-color`](/css/properties/background-color)`: rgba(0,0,0,0)`
    -   Set [`opacity`](/css/properties/opacity)`: 0` and an explicit `background-color` other than `transparent`
-   For IE8 and IE9
    -   Set [`filter`](http://msdn.microsoft.com/en-us/library/ms532847(v=vs.85).aspx)`: alpha(opacity=0);` and an explicit `background-color` other than `transparent`

#### iOS Safari

iOS Safari suffers from a bug where **click** events aren't fired on elements that aren't typically interactive (e.g. [`div`](/html/elements/div)) and which also don't have event listeners directly attached to the elements themselves (i.e. event delegation is being used). See [this live example](http://jsfiddle.net/cvrhulu/k9t0sdnf/show/) for a demonstration. Safari considers the following elements to be typically interactive (and thus they aren't affected by this bug): [`a`](/html/elements/a), [`button`](/html/elements/button), [`img`](/html/elements/img), [`input`](/html/elements/input), [`label`](/html/elements/label) (but it must be associated with a form control), [`textarea`](/html/elements/textarea)

Known workarounds for this bug:

-   Set [`cursor`](/css/properties/cursor)`: pointer;` on the element.
-   Add a dummy `onclick=""` attribute to the element.
-   Use a typically interactive element (e.g. [`a`](/html/elements/a)) instead instead of one that isn't typically interactive (e.g. [`div`](/html/elements/div)).
-   Stop using **click** event delegation.

### Syntax

### Standards information

-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 18.2.3

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****
